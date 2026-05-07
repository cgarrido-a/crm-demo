# Demo landing — Bootcamp de Datos

Landing estática para demostrar la integración de formularios del CRM.

## Setup

1. Crea un form en el CRM demo (`/orgs/demo-crm/forms`) con estos campos:
   - `firstname`, `lastname`, `email`, `phone`, `experiencia`
2. Copia el `form_id` de la URL.
3. Editá `index.html` y reemplazá `REPLACE_WITH_FORM_ID` por el ID real.
4. Probá local: abrí `index.html` directamente en el browser, o servilo:
   ```bash
   python3 -m http.server 5500
   # http://localhost:5500
   ```

## Deploy a Vercel

### Opción A — desde el dashboard

1. Hacé un repo en GitHub con esta carpeta.
2. https://vercel.com → "New Project" → importá el repo → Deploy.
3. Te tira `https://<nombre>.vercel.app`.

### Opción B — desde la terminal (más rápido)

```bash
npm install -g vercel        # solo la primera vez
cd demo-landing
vercel                       # te guía por preguntas, deploya y abre URL
vercel --prod                # cuando estés conforme
```

## CORS

El CRM ya permite POST desde cualquier origen al endpoint `/api/form-submit/*`.
No requiere agregar el dominio de Vercel a una allowlist.

## Estructura

- `index.html` — HTML + JS de submit
- `style.css` — estilos
- `vercel.json` — config (opcional, no hace falta para Vercel autodetect)
# crm-demo
