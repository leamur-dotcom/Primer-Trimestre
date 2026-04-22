# Guía de Despliegue: GitHub y Vercel 🚀

Este proyecto ha sido optimizado para ser desplegado fácilmente en Vercel desde un repositorio de GitHub.

## 1. Subir a GitHub

Si ya tienes una cuenta de GitHub, sigue estos pasos:

1. **Crear un nuevo repositorio** en GitHub (no lo inicialices con README ni .gitignore).
2. **En tu terminal local** (donde tengas este código):

```bash
# Inicializar git
git init

# Añadir todos los archivos
git add .

# Primer commit
git commit -m "Initial commit: Bar Casa Montjuïc Analytics"

# Conectar con tu repositorio (cambia <USER> y <REPO>)
git remote add origin https://github.com/<USER>/<REPO>.git

# Subir el código
git branch -M main
git push -u origin main
```

## 2. Desplegar en Vercel

Una vez el código esté en GitHub:

1. Ve a [vercel.com](https://vercel.com) e inicia sesión.
2. Haz clic en **"Add New"** > **"Project"**.
3. Importa el repositorio que acabas de subir desde GitHub.
4. En la configuración del proyecto:
   - **Framework Preset:** Vercel detectará automáticamente **Vite**.
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`
5. Haz clic en **"Deploy"**.

### Variables de Entorno (Opcional)
Si en el futuro añades funcionalidades de IA (como el Gemini API key), deberás configurarlas en:
`Vercel Dashboard > Settings > Environment Variables`.

---

## Estructura del Proyecto

- `src/App.tsx`: Contiene todo el dashboard y la lógica de datos.
- `src/lib/utils.ts`: Utilidades para Tailwind CSS.
- `metadata.json`: Metadatos de la aplicación para AI Studio.
- `package.json`: Dependencias (Recharts, Lucide, Motion, Tailwind).
