# PadelFit — Guía de despliegue

## Lo que necesitas (todo gratuito)
- Cuenta en github.com
- Cuenta en vercel.com
- Tu API key de Anthropic (console.anthropic.com)

---

## Paso 1 — Sube el proyecto a GitHub

1. Ve a github.com e inicia sesión
2. Pulsa el botón verde "New" para crear un repositorio
3. Ponle el nombre "padelfit", deja todo por defecto y pulsa "Create repository"
4. En la página siguiente verás instrucciones. Pulsa "uploading an existing file"
5. Arrastra todos los archivos de esta carpeta (api/, public/, vercel.json)
6. Pulsa "Commit changes" — ya está en GitHub

---

## Paso 2 — Despliega en Vercel

1. Ve a vercel.com e inicia sesión con tu cuenta de GitHub
2. Pulsa "Add New Project"
3. Selecciona el repositorio "padelfit" que acabas de crear
4. Pulsa "Deploy" — Vercel detecta la configuración automáticamente

---

## Paso 3 — Añade tu API key (importante)

1. En el panel de Vercel, ve a tu proyecto → "Settings" → "Environment Variables"
2. Pulsa "Add New"
3. En "Key" escribe exactamente: ANTHROPIC_API_KEY
4. En "Value" pega tu API key de Anthropic
5. Pulsa "Save"
6. Ve a "Deployments" y pulsa "Redeploy" para aplicar el cambio

---

## Listo

Vercel te dará una URL tipo: https://padelfit-tuusuario.vercel.app

¡Esa URL ya funciona en móvil como una app real!

---

## Estructura del proyecto

padelfit/
├── api/
│   └── chat.js        ← Backend seguro (llama a Claude)
├── public/
│   └── index.html     ← La app completa
└── vercel.json        ← Configuración de despliegue
