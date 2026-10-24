# Colmado Fénix: Hackeando el Futuro de una Pyme

Práctica del reto **"Hackeando el Futuro de una Pyme-Individual"**. Un colmado dominicano de Santo Domingo Este fue borrado de Internet de la noche a la mañana; este sitio reconstruye su presencia digital, la hace más resistente y cuenta la historia de su "resurrección".

> Negocio, personas, números de teléfono y datos son ficticios. Proyecto académico.

## Páginas

| Página | Archivo | Contenido |
|---|---|---|
| Historia del misterio | `index.html` | Pantalla de error inicial, cronología del incidente, mensaje del USB y medidas de protección |
| Servicios reinventados | `servicios.html` | Servicios nuevos (antes y ahora), cotizador en línea y preguntas frecuentes |
| Contacto | `contacto.html` | Formulario validado, pruebas del incidente, mapa y horario |

## Requisitos cubiertos

**HTML**
- Estructura semántica: `header`, `nav`, `main`, `section`, `article`, `aside`, `footer`, `time`, `blockquote`, `details/summary`, `table` con `caption`.
- Tres páginas enlazadas con navegación común y `aria-current` en la página activa.
- Accesibilidad: enlace "saltar al contenido", etiquetas en todos los campos, `aria-live`, foco visible.

**CSS**
- Identidad propia: toldo de colmado (rayas magenta y turquesa), sello amarillo mango, paleta índigo/magenta/turquesa/mango.
- Efecto glitch en los títulos, líneas de escaneo, temblor en la pantalla de error.
- Responsive con `grid`, `flex` y `clamp()`; menú hamburguesa en móvil.
- Respeta `prefers-reduced-motion`.

**JavaScript**
- Pantalla de "ERROR 404: negocio no encontrado" que se recupera con un clic y una barra de restauración.
- Easter egg "Modo Fénix" con cupón secreto. Se activa de 4 formas:
  1. Escribir `fenix` en cualquier parte de la página.
  2. Código Konami: ↑ ↑ ↓ ↓ ← → ← → B A.
  3. Cinco clics rápidos en el logo.
  4. Doble clic en "F.E.N.I.X." dentro de la Prueba 3 (página de contacto).
- Chatbot **Fenixito**: reconoce intenciones (horario, delivery, precios, ubicación, fiao, pagos, seguridad, la historia) con botones de sugerencia.
- Efecto máquina de escribir, contador de días desde el incidente, estado "abierto/cerrado" en tiempo real.

**Extras (opcional, 2 puntos)**
- **API de mapas**: Leaflet + OpenStreetMap con marcador y radio de delivery.
- **Cotización en línea**: calculadora con envío y botón que arma el pedido en WhatsApp.
- **API de tasa de cambio**: `open.er-api.com` convierte el total de RD$ a US$ con la tasa del día.
- **Modo oscuro / claro** con botón y preferencia guardada.

## Cómo verlo

Abrir `index.html` en el navegador, o con Live Server en VS Code. También se puede publicar en GitHub Pages (Settings → Pages → rama `main`, carpeta `/root`).

## Estructura

```
colmado-fenix/
├── index.html
├── servicios.html
├── contacto.html
├── css/styles.css
└── js/
    ├── main.js        # tema, menú, pantalla de error, easter egg, chatbot
    ├── servicios.js   # cotizador + API de tasa de cambio
    └── contacto.js    # formulario, mapa, estado abierto/cerrado
```
