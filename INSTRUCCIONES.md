# WG e Hijos — Guía de instalación con Firebase

## Archivos incluidos

| Archivo | Descripción |
|---|---|
| `index.html` | La app completa con login y sincronización |
| `manifest.json` | Configuración de la app |
| `sw.js` | Service Worker — funciona sin internet |
| `icon-192.png` `icon-512.png` `apple-touch-icon.png` | Íconos WG |

---

## PASO 1 — Crear proyecto Firebase (gratis)

1. Ve a **console.firebase.google.com** → inicia sesión con Google
2. **"Crear un proyecto"** → nombre: `wg-e-hijos` → desactiva Analytics → **"Crear proyecto"**

### Activar login por correo
1. Menú izquierdo → **Build → Authentication → "Get started"**
2. Pestaña **"Sign-in method"** → **"Email/Password"** → activa el switch → **"Save"**

### Crear base de datos Firestore
1. Menú izquierdo → **Build → Firestore Database → "Create database"**
2. Selecciona **"Production mode"** → elige región `us-central1` → **"Enable"**

### Configurar reglas de seguridad
En Firestore → pestaña **"Rules"** → borra todo y pega:

```
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /fincas/{userId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
    match /configs/{userId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
  }
}
```
→ Clic en **"Publish"**

### Obtener credenciales
1. Ícono ⚙️ → **"Project settings"** → sección **"Your apps"**
2. Clic en **"</>"** → nombre: `wg-hijos-web` → **"Register app"**
3. Copia el bloque `firebaseConfig` que aparece

---

## PASO 2 — Pegar credenciales en index.html

Abre `index.html` con Bloc de notas (Windows) o TextEdit (Mac).
Busca este bloque y reemplaza los valores:

```javascript
var FB_CFG = {
  apiKey:            "PEGA_TU_apiKey_AQUI",
  authDomain:        "PEGA_TU_authDomain_AQUI",
  projectId:         "PEGA_TU_projectId_AQUI",
  storageBucket:     "PEGA_TU_storageBucket_AQUI",
  messagingSenderId: "PEGA_TU_messagingSenderId_AQUI",
  appId:             "PEGA_TU_appId_AQUI"
};
```

Guarda el archivo.

---

## PASO 3 — Subir a GitHub

1. github.com → repositorio **WG-e-Hijos** → **"Add file → Upload files"**
2. Arrastra los 6 archivos → **"Commit changes"**

URL de tu app:
```
https://jdguti1985-dotcom.github.io/WG-e-Hijos/
```

---

## PASO 4 — Instalar en iPhone

1. Abre **Safari** → ve a la URL
2. Toca **Compartir ⬆** → **"Agregar a pantalla de inicio"** → **"Agregar"**
3. En la primera apertura: toca **"Registrarse"** y crea tu cuenta

---

## Compartir con familiares

Cada familiar instala la app en su iPhone y se registra con su correo.
Para que **todos compartan los mismos datos**: usar el **mismo correo y contraseña** en todos los dispositivos.

---

## Funciones nuevas

**Botón ⚙️ (engranaje arriba a la derecha):**
- Nombre e información de la finca
- 4 temas de color: Verde, Azul, Café, Gris oscuro
- Modo oscuro para usar de noche
- Tamaño de letra: Normal / Grande / Muy grande
- Estado de sincronización Firebase

**Sincronización automática:**
- Cada cambio se guarda en Firebase al instante
- Todos los dispositivos de la misma cuenta se actualizan en tiempo real
- El punto verde en el tablero indica conexión activa
