# pagina_kumelen
Diseño de pagina web para el Centro de Día Kumelen

Sitio web estático, hecho con **HTML y CSS**, para presentar al Centro de Día Kumelen (Mar del Plata): quiénes son, los talleres que ofrecen, el equipo profesional, los datos de contacto y un formulario de solicitud de admisión. Es un proyecto personal de práctica de maquetación web; varios textos son todavía de relleno (*lorem ipsum*) a la espera del contenido definitivo.

## Tecnologías

- HTML5
- CSS3 (sin frameworks ni JavaScript)
- Mapa embebido de Google Maps (`iframe`)

## Estructura del proyecto

```
Pagina Kumelen/
├── index.html            # Página principal
├── solicitud.html        # Formulario de solicitud de admisión
├── css/
│   ├── style.css         # Estilos de la página principal
│   └── styleSolicitud.css# Estilos del formulario
└── images/               # Logo e imágenes de la institución y los talleres
```

## Secciones y funcionalidades

### `index.html`
- **Encabezado** con el logo del centro.
- **Barra de navegación** con enlaces internos (Inicio, Talleres, Equipo, Contacto) y a la página de Admisión.
- **Sobre Nosotros**: texto de presentación y dos imágenes superpuestas que se intercalan al pasar el mouse (transición de opacidad en CSS).
- **Talleres**: tarjetas para Jardinería, Estimulación Cognitiva, Computación, Música, Pintura, Teatro y Educación Física.
- **Equipo Profesional**: Directivos, Nutrición, Terapia Ocupacional, Orientadores y Psicología.
- **Contacto** (footer): dirección, mapa de Google Maps, enlaces a Facebook e Instagram y teléfono.

### `solicitud.html`
Formulario de admisión con validaciones nativas de HTML5 (`required`, `min="18"`, `type="email"`, `type="tel"`) para cargar:
nombre, apellido, edad y DNI del concurrente, discapacidad, obra social, teléfono y email de contacto.
El formulario aún no está conectado a un backend (`action="mi_server"`).

## Conceptos aplicados

- Estructura semántica: `header`, `nav`, `section`, `footer`, `fieldset`/`legend`.
- Navegación por anclas (`#inicio`, `#workspaces`, `#equip`, `#contact`) y entre páginas.
- Formularios HTML con distintos tipos de `input`, `select` y validación nativa.
- CSS: selectores por clase y descendencia, `display: inline-block` para las tarjetas, bordes redondeados, posicionamiento absoluto y `transition` + `:hover` para el efecto de intercalado de imágenes.
- Inserción de contenido externo con `iframe`.

## Cómo verlo

No requiere instalación ni build. Como las hojas de estilo e imágenes se referencian con rutas absolutas (`/css/...`, `/images/...`), conviene servir la carpeta desde un servidor local en lugar de abrir el HTML con doble clic, por ejemplo:

- Con la extensión **Live Server** de VS Code, abriendo `index.html`.
- O desde la raíz del proyecto:

```bash
python -m http.server 8000
# luego abrir http://localhost:8000
```
