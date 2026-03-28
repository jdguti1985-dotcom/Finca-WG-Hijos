# 📱 WG e Hijos — Guía de instalación

## Archivos incluidos

| Archivo | Descripción |
|---|---|
| `index.html` | La aplicación completa |
| `manifest.json` | Configuración de la app (nombre, ícono, color) |
| `sw.js` | Service Worker — permite uso sin internet |
| `icon-192.png` | Ícono WG establo (Android / Chrome) |
| `icon-512.png` | Ícono WG establo (pantalla de carga) |
| `apple-touch-icon.png` | Ícono WG establo (iPhone / iPad) |

---

## PASO 1 — Crear el repositorio en GitHub (solo una vez)

1. Ve a **github.com** e inicia sesión con tu cuenta `jdguti1985-dotcom`
2. Haz clic en el botón verde **"New"** (o el ícono ➕)
3. En *Repository name* escribe: `WG-e-Hijos` (sin espacios)
4. Asegúrate de que esté en **"Public"**
5. Haz clic en **"Create repository"**

---

## PASO 2 — Subir los 6 archivos

1. En el repositorio recién creado, haz clic en **"uploading an existing file"**
2. Arrastra los **6 archivos** de esta carpeta al área de carga
3. En el cuadro de mensaje escribe: `Primera versión WG e Hijos`
4. Haz clic en **"Commit changes"** (botón verde)

---

## PASO 3 — Activar GitHub Pages

1. Ve a la pestaña **Settings** del repositorio
2. En el menú izquierdo busca **"Pages"**
3. En *Source* selecciona **"Deploy from a branch"**
4. En *Branch* selecciona **"main"** y la carpeta **"/ (root)"**
5. Haz clic en **"Save"**

⏳ Espera **2-3 minutos**. Tu app estará disponible en:
```
https://jdguti1985-dotcom.github.io/WG-e-Hijos/
```

---

## PASO 4 — Instalar en iPhone (para cada familiar)

1. **Abre Safari** en el iPhone ⚠️ debe ser Safari, no Chrome
2. Ve a:
   ```
   https://jdguti1985-dotcom.github.io/WG-e-Hijos/
   ```
3. Espera que la app cargue completamente
4. Toca el botón **Compartir** ⬆ (abajo en Safari)
5. Desplázate y toca **"Agregar a pantalla de inicio"**
6. Ponle el nombre que quieras y toca **"Agregar"**

✅ El ícono del establo con las letras **WG** aparecerá en la pantalla de inicio.

---

## PASO 5 — Instalar en Mac

1. Abre **Safari** en tu Mac
2. Ve a la URL de la app
3. Menú Safari → **Archivo → Agregar al Dock** (macOS Sonoma o superior)
4. O: ícono **Compartir** ⬆ → **"Agregar al Dock"**

---

## ¿Cómo funciona sin internet?

Una vez que cada familiar abra la app **al menos una vez** con internet:

- ✅ Funciona completamente sin conexión
- ✅ Los datos se guardan en el dispositivo
- ✅ Con internet se actualiza automáticamente si publicas una versión nueva

---

## Respaldo de datos

En la sección **"Reportes"** puedes:
- **Exportar PDF** — elige la sección o exporta todo
- **Exportar Excel** — descarga un .csv que abre Numbers o Excel
- **Respaldo JSON** — guarda todo en iCloud o WhatsApp
- **Importar JSON** — restaura un respaldo anterior

---

## ❓ Preguntas frecuentes

**¿Los datos se comparten entre los iPhone?**
No automáticamente. Cada iPhone tiene sus propios datos. Para compartir, descarga el JSON en un dispositivo y envíalo por WhatsApp al otro.

**¿Se puede cambiar el nombre "WG e Hijos"?**
Sí. Edita el archivo `index.html` en GitHub y busca "WG e Hijos". Cámbialo y guarda.

**¿Funciona en Android?**
Sí, con Chrome. Menú ⋮ → "Instalar app" o "Agregar a pantalla de inicio".

---

*Desarrollado para WG e Hijos*
