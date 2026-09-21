# Koraconcept · Presentación de tableros

Presentación interactiva de la colección de tableros para hostelería de **Koraconcept Mobiliario** (Santa Coloma de Farners, Girona). Se abre en el navegador, funciona en móvil y no necesita instalar nada.

**Ver la presentación:** https://USUARIO.github.io/koraconcept-presentacion/

## Qué incluye

- 12 diapositivas: portada, qué hacemos, la colección, una ficha por cada línea de tablero, comparador de medidas, proceso y contacto.
- Navegación con flechas del teclado, deslizando en móvil, o desde el índice lateral.
- Galería ampliable en cada producto.
- Comparador de medidas a escala (Ø60, Ø70, Ø77, Ø80 y formatos cuadrados).
- Selector "Mi selección": el cliente elige tableros y medidas y envía la solicitud de presupuesto por email.
- Español e inglés con el botón ES/EN.

## Antes de publicar

Abre `index.html` y busca el bloque `CONFIG` (al principio del `<script>`):

```js
const CONFIG = {
  email: "",    // destino de las solicitudes de presupuesto
  phone: "",
  web:   "",
  address: "Santa Coloma de Farners, Girona"
};
```

Rellena email, teléfono y web. Sin email, el botón "Enviar solicitud" abre el correo sin destinatario.

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub llamado `koraconcept-presentacion`, **público**, sin README.
2. Sube esta carpeta entera (`index.html` + `assets/`). Puedes arrastrarla en *Add file → Upload files*.
3. En el repositorio: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / carpeta `/ (root)` → Save**.
4. En un par de minutos la web queda publicada en `https://USUARIO.github.io/koraconcept-presentacion/`. Ese es el enlace que se envía a los clientes.

Si prefieres la línea de comandos:

```bash
git init
git add .
git commit -m "Presentación Koraconcept"
git branch -M main
git remote add origin https://github.com/USUARIO/koraconcept-presentacion.git
git push -u origin main
```

## Estructura

```
index.html          La presentación completa (HTML, CSS y JS en un solo archivo)
assets/             Fotografías de los tableros
```

## Editar el contenido

Las líneas de producto están en el array `LINES` dentro de `index.html`: nombre, descripción, especificaciones, medidas e imágenes. Los textos de interfaz, en español e inglés, están en el objeto `T`. Para añadir fotos, guárdalas en `assets/` y añade la ruta al objeto `IMG`.
