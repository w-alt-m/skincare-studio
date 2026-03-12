# Natural Skin - Cuidado Facial Orgánico

Estudio de cuidado facial orgánico en Palermo, Buenos Aires. Esta es una landing page estática para presentar los servicios, beneficios y contacto del estudio, diseñada con un enfoque en la calma, la naturaleza y la relajación.

## Tecnologías Utilizadas

- **HTML5** semántico
- **Tailwind CSS v4** para estilos utilitarios modernos.
- **Vanilla JavaScript** (sin dependencias externas).
- **Iconos:** Material Symbols Outlined.
- **Fuentes:** Manrope (Textos) y Playfair Display (Títulos) a través de Google Fonts.
- **Formularios:** Preparado para integrarse con Formspree.

## Requisitos Previos

Para desarrollar y compilar el CSS del proyecto localmente, necesitas tener instalado:
- [Node.js](https://nodejs.org/) (incluye `npm`).

## Instalación y Desarrollo Local

1. **Clonar el repositorio y abrir la carpeta:**
   ```bash
   git clone <url-del-repositorio>
   cd skincare-studio
   ```

2. **Instalar las dependencias (Tailwind CSS):**
   ```bash
   npm install
   ```

3. **Ejecutar el compilador de CSS en modo "Watch":**
   Esto se quedará escuchando por cambios en los archivos HTML/CSS y recompilará automáticamente el archivo de salida en la carpeta `dist`.
   ```bash
   npx tailwindcss -i ./src/input.css -o ./dist/style.css --watch
   ```

4. **Visualizar el proyecto:**
   Abre el archivo `index.html` en cualquier navegador web, o utiliza una extensión como [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) en VS Code para que el navegador se recargue automáticamente ante los cambios.

## Estructura del Proyecto

```
skincare-studio/
├── src/
│   └── input.css          # Archivo CSS de entrada de Tailwind v4 (donde se definen variables y utilidades base)
├── dist/
│   └── style.css          # Archivo CSS final compilado e importado por la web (¡NO EDITAR MANUALMENTE!)
├── index.html             # Página principal del proyecto
├── main.js                # Archivo JavaScript (menú responsive, etc.)
├── package.json           # Dependencias de npm
├── README.md              # Documentación del proyecto
└── favicon.ico            # Favicon de la web (PENDIENTE de colocar la imagen real)
```

## Ajustes Pendientes Antes de Salir a Producción

La estructura técnica está lista y optimizada, solo quedan algunos detalles de contenido por parte del cliente:

1. **Imágenes Reales:**  
   Reemplazar las URLs de las imágenes en las etiquetas `<img>` (Hero section y sección "Nosotros") por las fotografías profesionales del estudio. Todas se recomiendan guardar en una carpeta local como `/assets`, o servirse desde un CDN.
2. **Formulario de Contacto (Formspree):**  
   Crear una cuenta en [Formspree](https://formspree.io/), generar un endpoint y reemplazar la URL `"https://formspree.io/f/placeholder"` en el atributo `action` del `<form>` en `index.html`.
3. **Favicon:**  
   Colocar una imagen en formato `.ico` o `.png` (idealmente 32x32 px) llamada `favicon.ico` en la raíz del proyecto para que se muestre en la pestaña del navegador.
4. **Nombres de Testimonios:**  
   Actualizar si se desea la palabra "Cliente" debajo de cada review por nombres o iniciales reales en la sección `#testimonials`.

## Despliegue (Deploy)

Al ser una web totalmente estática (HTML/CSS/JS), este proyecto se puede desplegar instantáneamente de forma gratuita y rápida utilizando servicios como:

- **GitHub Pages:** Habilitar desde la pestaña "Settings" > "Pages" del repositorio.
- **Vercel / Netlify:** Importar directamente la carpeta del repositorio y configurar el comando de compilación (`npx tailwindcss -i ./src/input.css -o ./dist/style.css`) y el directorio de publicación (`/` o la carpeta base). 

> *Nota: Recuerda que para Producción necesitas ejecutar de nuevo el comando de build sin el flag `--watch` si hay servicios CI/CD.*
