# LG Coach — Adrián

Dashboard personal de objetivos y ventas para promotor LG en Media Markt.

## Stack
- Frontend: HTML/CSS/JS puro (sin frameworks)
- Backend: Vercel Serverless Functions (Node.js)
- IA: Anthropic Claude API

## Estructura
```
lg-coach/
├── public/
│   └── index.html      # App completa
├── api/
│   └── coach.js        # Proxy serverless → Anthropic
├── vercel.json
├── package.json
└── .gitignore
```

## Deploy en Vercel

### 1. Sube a GitHub
```bash
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/lg-coach.git
git push -u origin main
```

### 2. Conecta en Vercel
1. Ve a [vercel.com](https://vercel.com) → **Add New Project**
2. Importa tu repo de GitHub
3. En **Environment Variables** añade:
   - `ANTHROPIC_API_KEY` = tu API key de Anthropic
4. Pulsa **Deploy**

### 3. Obtener API key de Anthropic
Ve a [console.anthropic.com](https://console.anthropic.com) → API Keys → Create Key

## Datos
Los datos (ventas, objetivos, historial) se guardan en `localStorage` del navegador.
Si accedes siempre desde el mismo dispositivo y navegador, persisten indefinidamente.
