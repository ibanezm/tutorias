# Tutorías de Matemáticas y Física — Valparaíso
**Sitio web estático optimizado para SEO · GitHub Pages**

---

## Estructura de carpetas

```
tutorias-site/
│
├── index.html              ← Página principal (SEO optimizado)
├── robots.txt              ← Instrucciones para Google
├── sitemap.xml             ← Mapa del sitio para Google
│
├── css/
│   └── style.css           ← Estilos completos
│
├── js/
│   └── main.js             ← Interactividad y animaciones
│
├── assets/
│   ├── favicon.svg         ← Ícono del sitio
│   └── foto-tutor.jpg      ← ⚠️ Agrega tu foto aquí (ver instrucciones)
│
└── pdfs/
    ├── guia-integrales-linea-superficie.pdf
    ├── resumen-ecuaciones-maxwell.pdf
    ├── guia-algebra-lineal-espacios-vectoriales.pdf
    ├── guia-ecuaciones-diferenciales-ordinarias.pdf
    ├── resumen-mecanica-cuantica-introductoria.pdf
    └── guia-trigonometria-escolar.pdf
```

---

## Personalización antes de publicar

### 1. Tu número de WhatsApp
En `index.html`, busca el botón de WhatsApp y reemplaza el número:
```html
href="https://wa.me/56900000000?text=Hola%2C..."
```
Cambia `56900000000` por tu número (código de país + número, sin espacios ni +).

### 2. Tu foto
Agrega tu foto en `assets/foto-tutor.jpg` (recomendado: 600×600 px, fondo claro).
Luego descomenta la etiqueta `<img>` en el HTML y elimina el `div.tutor__avatar-placeholder`:
```html
<img src="assets/foto-tutor.jpg"
     alt="Tutor de matemáticas y física en Valparaíso"
     width="320" height="320" loading="lazy" />
```

### 3. Tu QR de WhatsApp
Genera tu QR en https://wa.me/link/TU-NUMERO → descarga imagen → guárdala como `assets/qr-whatsapp.png`.
En el HTML reemplaza el bloque `.qr__placeholder` por:
```html
<img src="assets/qr-whatsapp.png"
     alt="Código QR para contactar por WhatsApp"
     width="200" height="200" loading="lazy" />
```

### 4. URL canónica
Reemplaza `tu-usuario` por tu usuario real de GitHub en:
- `index.html` → `<link rel="canonical" href="...">`
- `index.html` → `<meta property="og:url" content="...">`
- `robots.txt` → `Sitemap:`
- `sitemap.xml` → todas las `<loc>`

### 5. PDFs descargables
Crea o exporta tus guías como PDF y nómbralos igual que los archivos en `/pdfs/`. El HTML ya apunta a esos nombres. Si cambias el nombre, actualiza también el atributo `href` del enlace correspondiente.

---

## Cómo subir a GitHub Pages

### Paso 1 — Crear repositorio
1. Ve a https://github.com/new
2. Nombre: `tutorias` (o el que quieras; coincidirá con la URL)
3. Visibilidad: **Public**
4. Click en "Create repository"

### Paso 2 — Subir archivos
**Opción A — Desde la web (más fácil):**
1. En tu repositorio, click en "Add file" → "Upload files"
2. Arrastra toda la carpeta `tutorias-site/`
3. Escribe un mensaje de commit: `Publicación inicial`
4. Click en "Commit changes"

**Opción B — Desde terminal (Git):**
```bash
cd tutorias-site
git init
git add .
git commit -m "Publicación inicial del sitio"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/tutorias.git
git push -u origin main
```

### Paso 3 — Activar GitHub Pages
1. Ve a tu repositorio → **Settings** → **Pages**
2. En "Source" selecciona: **Deploy from a branch**
3. Branch: `main` → carpeta: `/ (root)`
4. Click en "Save"
5. Espera 1-2 minutos y tu sitio estará en:
   `https://tu-usuario.github.io/tutorias/`

---

## SEO — Lista de verificación

- [x] `<title>` optimizado con palabras clave locales
- [x] `<meta description>` descriptivo y con keywords
- [x] `<meta keywords>` con todas las búsquedas objetivo
- [x] Jerarquía H1 → H2 → H3 correcta
- [x] Schema.org LocalBusiness con ciudad Valparaíso
- [x] Open Graph para redes sociales
- [x] `robots.txt` configurado
- [x] `sitemap.xml` incluido
- [x] `rel="canonical"` en el `<head>`
- [x] Atributos `alt` en todas las imágenes
- [x] Texto SEO en secciones de matemáticas y física
- [x] Texto SEO en el footer con keywords clave
- [x] Fuentes cargadas con `preconnect` (velocidad)
- [x] Imágenes con `loading="lazy"`
- [x] Diseño responsive para móviles
- [ ] Agrega tu URL real en `sitemap.xml` y `robots.txt`
- [ ] Registra tu URL en Google Search Console
- [ ] Sube tus PDFs a la carpeta `/pdfs/`

---

## Registro en Google Search Console (recomendado)

1. Ve a https://search.google.com/search-console
2. Click en "Añadir propiedad" → elige "Prefijo de URL"
3. Pega tu URL de GitHub Pages
4. Verifica con el método HTML tag (pega el código en el `<head>` del index.html)
5. Envía el sitemap: `https://tu-usuario.github.io/tutorias/sitemap.xml`

Google tardará 1-4 semanas en indexar el sitio.

---

## Actualizar el sitio en el futuro

**Desde la web de GitHub:**
- Edita cualquier archivo directamente en GitHub haciendo click sobre él → ícono del lápiz.

**Desde terminal:**
```bash
git add .
git commit -m "Actualizo contenido"
git push
```
GitHub Pages se actualiza automáticamente en menos de 1 minuto.
