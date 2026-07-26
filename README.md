# Portafolio bilingüe de Ian Gutiérrez

Portafolio estático y responsive construido con HTML, CSS y JavaScript, basado en el diseño original de Canva y ampliado con el contenido del CV y del documento de proyectos.

## Funciones incluidas

- Tema claro: blancos, verde agua, turquesa y azul claro.
- Tema oscuro: negro, morado y azul.
- Preferencia de tema guardada en `localStorage`.
- Contenido independiente en español e inglés, no traducción automática.
- Preferencia de idioma guardada en `localStorage`.
- Nueve proyectos completos con filtros y casos de estudio.
- Descarga del CV correspondiente al idioma activo.
- Barra de progreso de lectura y scrollbar personalizado.
- Modal de proyectos con scroll interno oculto y cierre accesible.
- Diseño responsive para computadora, tablet y móvil.
- Formulario que prepara un correo con `mailto:`.

## Estructura

```text
ian-portfolio/
├── index.html
├── styles.css
├── script.js
├── README.md
└── assets/
    ├── CV-Ian-Gutierrez-ES.pdf
    ├── CV-Ian-Gutierrez-EN.pdf
    └── projects/
```

## Ejecutarlo localmente

### VS Code

Abre la carpeta y usa la extensión **Live Server** sobre `index.html`.

### Python

```bash
cd ian-portfolio
python -m http.server 5500
```

Abre `http://localhost:5500`.

## Modificar textos

Todo el contenido se administra en `script.js`:

- `uiCopy.es` y `uiCopy.en`: navegación, hero, perfil, contacto y etiquetas.
- `portfolioData.projects`: contenido completo de cada proyecto en ambos idiomas.
- `portfolioData.skills`: habilidades por idioma.
- `portfolioData.timeline`: experiencia y formación.
- `portfolioData.impact`: métricas superiores.

El inglés y el español son textos independientes. Puedes cambiar uno sin afectar el otro.

## Modificar paletas

Las variables están al inicio de `styles.css`:

- `:root`: modo claro.
- `html[data-theme="dark"]`: modo oscuro.

Los colores visuales de cada tarjeta usan variables `--visual-*` y también tienen variantes distintas por tema.

## Estado real de proyectos

El contenido diferencia entre:

- Proyectos empresariales desarrollados en AMX Contenido.
- Prototipos técnicos funcionales.
- Proyectos personales con integraciones pendientes.
- Proyectos académicos.

Esto evita presentar como producción algo que todavía está en fase de prototipo.

## Imágenes de proyectos

Los visuales actuales están construidos con CSS para que el sitio no dependa de imágenes externas. Puedes agregar capturas dentro de `assets/projects/` y sustituir `.project-mockup` por una etiqueta `<img>` desde `projectCard()` en `script.js`.

## Publicación

El proyecto puede desplegarse directamente en GitHub Pages, Vercel, Netlify o Cloudflare Pages.
