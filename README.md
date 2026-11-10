# IziMaker

Constructor visual de esqueletos de sitios web. Arrastra elementos a un lienzo,
ajusta sus propiedades, y descarga **HTML, CSS y JavaScript** listos para publicar.

Todo vive en **un único archivo `index.html`**, sin dependencias, sin instalación
y sin servidor: ábrelo con doble clic y funciona.

## Cómo se usa

1. Abre `index.html` en el navegador (doble clic).
2. Arrastra elementos de la paleta izquierda al lienzo, o haz clic en ellos para
   añadirlos al contenedor seleccionado.
3. Selecciona un elemento para editar su contenido y estilo en el panel derecho.
   También puedes escribir directamente sobre el lienzo y estirar los bordes con
   el ratón.
4. Descarga el resultado con **Descargar ZIP** (`index.html` + `styles.css` +
   `script.js` + `README.md`) o con **HTML único** (todo incrustado en un archivo).

## Qué incluye

- **30 elementos**: cabecera, barra de navegación, portada, sección, contenedor,
  columnas ×2/×3, pie, títulos H1–H3, párrafo, imagen, botón, enlace, separador,
  lista, cita, etiqueta, formulario, campo, área de texto, casilla, botón de envío,
  vídeo/iframe, icono, tabla, bloque de código, espaciador y tarjeta.
- **5 plantillas**: en blanco, landing, portafolio, blog y documentación.
- **Lienzo WYSIWYG**: arrastrar y soltar, reordenar, anidar en contenedores y
  columnas, edición de texto en línea y redimensionado arrastrando los bordes.
- **Inspector**: texto, enlaces, colores, tipografía, alineación, relleno, márgenes,
  ancho, alto, redondeo y clases CSS propias.
- **Vista previa** en tres anchos (escritorio, tablet, móvil) y **vista limpia**
  para ver la página sin los adornos del editor.
- **Código generado** visible en pestañas con resaltado de sintaxis y botón copiar.
- **Deshacer / rehacer**, autoguardado en el navegador y guardar/abrir proyecto
  en JSON.

## Cómo funciona

El maquetado es un árbol de nodos en memoria: cada elemento declara sus valores
por defecto, los campos que edita el inspector, su plantilla HTML y las
declaraciones CSS que se derivan de sus propiedades. De ese árbol se generan las
tres salidas:

- **HTML** semántico e indentado.
- **CSS** con un tema base, una regla por tipo de elemento (`.mz-boton`) y una
  regla por instancia (`.el-xxxx`) **sólo con lo que difiere** de los valores por
  defecto, así la hoja exportada es corta y legible.
- **JavaScript** con el comportamiento necesario (menú móvil, año del pie y
  confirmación de formularios), sin código muerto.

El lienzo se pinta con el mismo HTML y la misma hoja de estilos que la
exportación, por lo que lo que ves es exactamente lo que se descarga. El ancho de
la página se controla con *container queries*, de modo que las reglas de móvil
responden al marco del lienzo y no al tamaño de la ventana.

## Compatibilidad

Navegadores modernos (Chrome/Edge 105+, Safari 16+, Firefox 110+), por el uso de
*container queries*. El proyecto usa `localStorage` para el autoguardado y
`Blob` para las descargas; no envía nada a ningún servidor.

## Estructura

```
.
├── index.html   # la aplicación completa (HTML + CSS + JS)
├── README.md
└── LICENSE
```

## Licencia

MIT — puedes usar, modificar y distribuir el proyecto libremente.