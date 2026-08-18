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

## Datos ya configurados

| Dato | Valor |
|---|---|
| Teléfono y WhatsApp | +57 318 262 6857 (`573182626857` en los enlaces) |
| Correo | aveda@gmail.com |
| Nequi | 301 480 4112 |
| Cifras | 150 rescatados · 130 adopciones · 600+ esterilizaciones · 6 años |

## Pendientes por agregar

- **Fotos reales** en `imagenes/` (ver `imagenes/LEE-ESTO.txt`).
- **Nombres y municipios** de los animales del mosaico: busca `Nombre · Municipio`
  en `index.html` y reemplaza cada uno.
- **Redes sociales**: hay un comentario en el pie de página con el formato listo
  para pegar los enlaces de Facebook e Instagram.
- **NIT y dirección de la sede**, si quieres mostrarlos (buscar "Región de Urabá"
  en la sección de contacto y la línea del copyright).
- **Más medios de donación** (Daviplata, cuenta bancaria, PayPal): el bloque
  `<div class="metodo">` del modal se puede duplicar.

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
