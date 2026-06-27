# API Vehículos

Proyecto con dos partes que se despliegan por separado:

- `front/` → página web (HTML/CSS/JS) → se despliega en **Vercel**
- `back/` → API en Python/FastAPI → se despliega en **Render**

## Antes de subir a GitHub

1. Confirma que el archivo `.env` (dentro de `back/`) **no se suba**. Ya está protegido por `.gitignore`.
2. `back/.env.example` muestra qué variables necesitas, sin valores reales.

## Variables de entorno necesarias (Render)

```
SERP_API_KEY=tu_clave_real
OPENAI_API_KEY=tu_clave_real
```

## Pasos generales

1. Despliega `back/` en Render (Web Service, Python) y copia la URL pública que te da.
2. Pega esa URL + `/specs` en `front/index.html`, en la constante `API_URL`.
3. Despliega `front/` en Vercel.
4. Copia la URL de Vercel y agrégala a la lista `ALLOWED_ORIGINS` en `back/main.py`.
5. Vuelve a desplegar el backend en Render para que tome el cambio de CORS.
