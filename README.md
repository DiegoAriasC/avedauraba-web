# AVEDA — Landing page

Sitio web de la Fundación AVEDA, dedicada al rescate y adopción de animales
en situación de calle en la región de Urabá, Antioquia (Colombia).

Es un sitio **estático**: un solo archivo `index.html` sin dependencias ni
proceso de compilación. Se puede abrir con doble clic o publicar en cualquier hosting.

## Estructura

```
index.html          Toda la página (HTML + CSS + JavaScript)
vercel.json         Configuración de despliegue en Vercel
imagenes/           Fotos de la fundación (ver imagenes/LEE-ESTO.txt)
```

## Datos que hay que reemplazar antes de publicar

Abre `index.html` y busca y reemplaza estos valores de ejemplo:

| Buscar | Reemplazar por |
|---|---|
| `+57 300 000 0000` | Teléfono real de la fundación |
| `573000000000` | Número de WhatsApp (57 + celular, sin espacios ni +) |
| `contacto@aveda.org` | Correo real |
| `000-000000-00` | Número de cuenta Bancolombia |
| `3000000000` (en el modal de donación) | Números de Nequi y Daviplata |
| `NIT 000.000.000-0` | NIT real de la fundación |
| `id="btnPaypal"` → `href="#"` | Enlace de PayPal / Wompi / Mercado Pago |
| `href="#"` en las redes del pie | URLs de Facebook, Instagram y TikTok |

También revisa las cifras de la sección de estadísticas (`data-contar`) y las
historias de los animales, que actualmente son texto de ejemplo.

## Publicar en Vercel

### Opción A — desde GitHub (recomendada)

1. Crea un repositorio nuevo y vacío en <https://github.com/new> (por ejemplo `aveda-web`).
2. En esta carpeta ejecuta:

   ```
   git remote add origin https://github.com/TU-USUARIO/aveda-web.git
   git branch -M main
   git push -u origin main
   ```

3. Entra a <https://vercel.com/new>, inicia sesión con GitHub e importa el repositorio.
4. Framework Preset: **Other**. Deja Build Command y Output Directory vacíos.
5. Clic en **Deploy**.

A partir de ahí, cada `git push` actualiza el sitio automáticamente.

### Opción B — con el CLI de Vercel

Requiere Node.js instalado (<https://nodejs.org>).

```
npm i -g vercel
vercel login
vercel --prod
```

## Dominio propio

En Vercel: **Settings → Domains → Add**. Un dominio `.org` o `.com` cuesta
alrededor de USD 12–20 al año. Vercel entrega el certificado HTTPS gratis.
