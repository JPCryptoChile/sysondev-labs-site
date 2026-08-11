# SysonDev - Labs — sitio (coming soon)

Página estática de "en construcción" con el branding de SysonDev - Labs. Sin build step: es HTML/CSS puro (`index.html` + `favicon.svg`).

## Desplegar en Vercel (subdominio gratis `.vercel.app`)

### 1. Subir el código a GitHub

```bash
cd sysondev-labs-site
git init
git add -A
git commit -m "Sitio coming soon SysonDev - Labs"
git remote add origin https://github.com/<TU-USUARIO>/sysondev-labs-site.git
git branch -M main
git push -u origin main
```

(Antes crea el repo vacío en https://github.com/new — nómbralo `sysondev-labs-site`, sin README/licencia para no chocar con el push.)

### 2. Importar en Vercel

1. Entra a https://vercel.com/new y conecta tu cuenta de GitHub si aún no lo está.
2. Selecciona el repo `sysondev-labs-site` y dale a **Import**.
3. Framework Preset: **Other** (no necesita build command ni output directory, Vercel sirve `index.html` directo).
4. Click **Deploy**.

### 3. Configurar el subdominio gratuito

Por defecto Vercel asigna `<nombre-del-proyecto>-<tu-usuario>.vercel.app`. Para dejarlo limpio como `sysondev-labs.vercel.app`:

1. En el proyecto en Vercel, ve a **Settings → Domains**.
2. Si `sysondev-labs.vercel.app` está libre, agrégalo ahí directamente. Si no, renombra el proyecto en **Settings → General → Project Name** a `sysondev-labs` — el dominio `.vercel.app` se actualiza automáticamente al nombre del proyecto (si está disponible).

Cada push a `main` vuelve a desplegar automáticamente.

## Actualizar el contenido más adelante

Cuando el negocio tenga producto (reportes diarios, dashboard, etc.), este mismo repo puede evolucionar a una app real (Next.js, etc.) sin perder el dominio ni el histórico de deploys.
