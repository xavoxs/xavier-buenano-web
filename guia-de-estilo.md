# Guía de estilo de la página de Xavier Buenaño

Documento de referencia de la cromática, la tipografía, el diseño y los componentes usados en la página de perfil profesional (versión 4). Sirve para mantener la coherencia al agregar contenido, cambiar de plataforma o pasar el diseño a otra persona.

## 1. Idea de diseño

Estilo **suizo con un toque humano**: rejilla rígida, tipografía grande y condensada, colores planos y reglas negras gruesas. Sobre esa base técnica se añaden **anotaciones escritas a mano** (flechas, subrayados, notas) que muestran criterio y voz propia, para que el sitio no parezca una plantilla generada automáticamente.

Cinco principios:

1. **Contenido orientado al cliente.** Cada sección responde una pregunta del visitante (¿me sirve?, ¿cómo trabaja?, ¿tiene resultados?, ¿cómo lo contacto?).
2. **Pocos colores, usados con intención.** Un acento para lo interactivo, dos bloques de color plano y neutros fríos.
3. **Nada de efectos suaves.** Sin degradados, sin sombras difusas, sin esquinas redondeadas, sin emojis.
4. **La jerarquía se ve en la forma.** Reglas gruesas separan secciones; reglas finas separan filas.
5. **El toque humano es limitado.** Las anotaciones a mano son pocas y siempre dicen algo útil.

## 2. Cromática

### 2.1 Paleta

| Rol | Nombre en el código | Claro | Oscuro | Dónde se usa |
|---|---|---|---|---|
| Fondo de página | `--bg` | `#EEF0F3` | `#0C0D11` | Fondo general (gris azulado frío, no blanco puro) |
| Texto y reglas | `--ink` | `#0B0C10` | `#F1F1EF` | Texto principal, reglas gruesas, bordes de nodos, botón principal |
| Texto secundario | `--muted` | `#4B515C` | `#A3A9B5` | Descripciones, párrafos de apoyo, pie de página |
| Líneas finas | `--line` | `#C6CBD3` | `#2A2D36` | Separadores de filas, bordes de apartados vacíos |
| Acento | `--link` | `#2B44FF` | `#8C9BFF` | Enlaces, subrayado ondulado, anotaciones a mano, selección de nodos, etiquetas |
| Superficie | `--surface` | `#FFFFFF` | `#14161C` | Nodos de servicio |
| Azul de bloque | `--blue` | `#2B44FF` | `#2B44FF` | Nodo raíz (perfil). Es el mismo en ambos temas |
| Texto sobre azul | `--on-blue` | `#FFFFFF` | `#FFFFFF` | Texto dentro del nodo raíz |
| Amarillo de bloque | `--yellow` | `#FFD21F` | `#FFD21F` | Logotipo, marco de la foto, bloque de contacto. Es el mismo en ambos temas |
| Texto sobre amarillo | `--on-yellow` | `#0B0C10` | `#0B0C10` | Texto dentro del bloque de contacto |

### 2.2 Reglas de uso del color

- **El acento (`--link`) solo para lo que se puede tocar o lo que el autor anota.** No se usa como decoración.
- **El azul de bloque aparece en un solo lugar:** el nodo raíz con tu perfil.
- **El amarillo aparece en tres lugares:** el logotipo "XB", el marco de la foto y el bloque de contacto. Es el único color cálido, y por eso marca los puntos donde la persona está presente.
- **El texto va siempre en `--ink` o `--muted`.** Nunca texto largo en el acento.
- **Dentro del bloque amarillo, las anotaciones a mano van en negro** (`--on-yellow`), no en el acento, porque el acento claro no se lee sobre amarillo.
- **No se añaden más colores.** Si hace falta un estado (éxito, error), se define aparte y no reemplaza al acento.

### 2.3 Contraste (accesibilidad)

Calculado con la fórmula de contraste de WCAG. Para texto normal, el mínimo recomendado es 4.5:1.

| Combinación | Contraste |
|---|---|
| Claro: texto sobre fondo | 17.12:1 |
| Claro: texto secundario sobre fondo | 6.99:1 |
| Claro: texto secundario sobre blanco | 7.98:1 |
| Claro: acento sobre fondo | 5.45:1 |
| Claro: acento sobre blanco | 6.22:1 |
| Oscuro: texto sobre fondo | 17.17:1 |
| Oscuro: texto secundario sobre fondo | 8.23:1 |
| Oscuro: texto secundario sobre superficie | 7.66:1 |
| Oscuro: acento sobre fondo | 7.63:1 |
| Oscuro: acento sobre superficie | 7.10:1 |
| Blanco sobre azul de bloque | 6.22:1 |
| Negro sobre amarillo de bloque | 13.49:1 |

Todas las combinaciones de texto superan el mínimo.

### 2.4 Tema claro y oscuro

La página cambia sola según la configuración del dispositivo. Los tokens de la tabla se redefinen en el tema oscuro; los dos bloques de color plano (azul y amarillo) se mantienen iguales en ambos temas para conservar la identidad.

## 3. Tipografía

Todas las fuentes son de Google Fonts.

| Rol | Fuente | Pesos | Uso |
|---|---|---|---|
| Títulos y números | **Archivo** (variable, ancho 62 a 125) | 500 a 900 | Títulos, nombre de marca, botones, cifras. Se usa **condensada** (ancho 72 % a 90 %) |
| Texto de lectura | **IBM Plex Sans** | 400, 500, 600 | Párrafos y descripciones |
| Etiquetas técnicas | **IBM Plex Mono** | 400, 500 | Rótulos de columnas, fechas, correo, notas de pie |
| Anotaciones a mano | **Caveat** | 500, 700 | Notas, flechas con texto, "aquí va mi foto" |

Fuentes de respaldo: Arial Narrow o Helvetica para títulos; Segoe UI o la fuente del sistema para texto; Segoe Print para las anotaciones.

### 3.1 Escala tipográfica

| Elemento | Tamaño | Detalles |
|---|---|---|
| Titular de portada (h1) | de 2.8 rem a 5.6 rem (fluido) | Peso 800, ancho 76 %, interlínea 0.95 |
| Títulos de sección (h2) | de 2.4 rem a 4.2 rem (fluido) | Mayúsculas, peso 800, ancho 72 %, interlínea 0.92 |
| Título del contacto | de 3.2 rem a 7.6 rem (fluido) | Igual que h2, más grande |
| Nodo de servicio | 1.5 rem | Peso 800, ancho 84 % |
| Títulos de elementos (casos, filas) | 1.35 rem | Peso 700, ancho 90 % |
| Frases de "Problemas que resuelvo" | 1.4 rem | Peso 700, ancho 88 % |
| Cifras clave | de 2.8 rem a 4.6 rem (fluido) | Peso 800, ancho 72 % |
| Números de proceso | 2.8 rem | Color acento |
| Texto de lectura | 17 px (16 px en celular) | Interlínea 1.6 |
| Texto de apoyo | de 0.85 rem a 0.97 rem | Color secundario |
| Etiquetas en mono | 0.72 rem | Mayúsculas, espaciado de letras amplio |
| Botones | 0.95 rem | Mayúsculas, peso 700, ancho 90 % |
| Anotaciones a mano | 1.4 rem | Peso 700 |

## 4. Diseño y rejilla

- **Ancho máximo del contenido:** 1240 px, centrado.
- **Margen lateral mínimo:** 16 px en cualquier pantalla (se respeta también la zona segura de los celulares).
- **Secciones:** rejilla de dos columnas, 4 partes para el título y 8 para el contenido, con 48 px de separación. Por debajo de 900 px pasan a una columna.
- **Árbol de servicios:** tres columnas (perfil de 290 px, servicios y soluciones a partes iguales) con 84 px de separación para los cables.
- **Reglas:** 4 px en `--ink` para encabezado, pie y apertura de secciones; 1 px en `--line` para filas; la primera fila de una lista usa la regla negra.
- **Esquinas:** rectas, sin redondeo. Solo los puntos de conexión del árbol son círculos.
- **Puntos de corte:** 900 px (el árbol pasa a lista con sangría y las secciones a una columna) y 620 px (las rejillas de dos y tres columnas pasan a una).
- **Espaciado entre secciones:** 80 px en escritorio, 60 px en pantallas angostas.

## 5. Componentes

**Botón principal.** Fondo `--ink`, texto `--bg`, borde de 2 px, mayúsculas. Al pasar el cursor cambia a fondo y borde `--link` con texto blanco.

**Botón secundario.** Transparente, borde de 2 px en `--ink`. Mismo comportamiento al pasar el cursor.

**Nodo de servicio.** Fondo `--surface`, borde de 2 px en `--ink`, título en Archivo, descripción en secundario. Al seleccionarlo, el borde pasa a `--link` y aparece una sombra dura de 5 px en el mismo color (sin difuminado).

**Nodo de solución.** Fondo `--bg`, borde de 1.5 px en `--ink`, título corto y una línea de apoyo.

**Cables.** Curvas dibujadas en SVG, de 2 px en `--ink`. Al seleccionar un servicio, sus cables pasan a 3 px en `--link` y el resto se atenúa. Los puntos de conexión son círculos de 12 px.

**Nodo raíz (perfil).** Bloque en `--blue` con el marco de la foto en `--yellow` (proporción 4:5, marcas de recorte en las esquinas), cargo en Archivo y datos en mono.

**Anotación a mano.** Texto en Caveat, color `--link`, con una pequeña flecha trazada a mano. Usos: indicar interacción, señalar datos pendientes y comentar un hito.

**Subrayado ondulado.** Trazo SVG de 3.4 px en `--link` bajo la frase clave del titular.

**Bloque de caso.** Tres columnas (reto, solución, resultado). La del resultado lleva un borde izquierdo de 3 px en `--link` y texto en `--ink` para destacarla.

**Bloque de contacto.** Fondo `--yellow`, texto negro, título gigante, correo en mono con botón "Copiar" en negro.

## 6. Movimiento

- Solo transiciones de 0.15 a 0.18 segundos en botones, enlaces, nodos y cables.
- Sin animaciones al desplazarse ni elementos que aparezcan tarde.
- Se respeta la preferencia "reducir movimiento" del dispositivo.

## 7. Voz y contenido

- Primera persona y frases completas (sin textos telegráficos).
- El nombre completo aparece **una sola vez a la vista** (en la barra superior). El resto del texto habla del cliente y de lo que se hace por él.
- Cada afirmación se respalda con un hecho verificable; lo que falta se marca con una anotación a mano hasta tener el dato.
- No se publican teléfonos, dirección ni números de registro de títulos.

## 8. Variables listas para copiar

```css
:root {
  --bg: #EEF0F3;
  --ink: #0B0C10;
  --muted: #4B515C;
  --line: #C6CBD3;
  --link: #2B44FF;
  --surface: #FFFFFF;
  --blue: #2B44FF;
  --on-blue: #FFFFFF;
  --yellow: #FFD21F;
  --on-yellow: #0B0C10;
  --font-display: "Archivo", "Arial Narrow", "Helvetica Neue", Arial, sans-serif;
  --font-body: "IBM Plex Sans", "Segoe UI", system-ui, sans-serif;
  --font-mono: "IBM Plex Mono", ui-monospace, Menlo, Consolas, monospace;
  --font-hand: "Caveat", "Segoe Print", "Bradley Hand", cursive;
}

/* Tema oscuro automático */
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --bg: #0C0D11;
    --ink: #F1F1EF;
    --muted: #A3A9B5;
    --line: #2A2D36;
    --link: #8C9BFF;
    --surface: #14161C;
    color-scheme: dark;
  }
}
```

Enlace de las fuentes:

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Archivo:wdth,wght@62..125,500..900&family=Caveat:wght@500;700&family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@400;500;600&display=swap">
```

## 9. Glosario

- **Hexadecimal (`#2B44FF`):** código de seis caracteres que identifica un color exacto.
- **Token (variable de diseño):** nombre que se le da a un valor, como `--link`, para reutilizarlo y cambiarlo en un solo lugar.
- **Contraste (WCAG):** medida de qué tan legible es un texto sobre su fondo; 4.5:1 es el mínimo recomendado.
- **Rejilla (grid):** estructura de columnas invisible que alinea todos los elementos.
- **Tipografía condensada:** letras más angostas de lo normal.
- **Fuente variable:** una sola fuente que permite ajustar peso y ancho de forma continua.
- **Interlínea:** espacio vertical entre líneas de texto.
- **Color plano:** área de un solo color, sin degradado ni sombra.
- **Sombra dura:** sombra desplazada y sin difuminado.
- **SVG:** formato de dibujo vectorial que no pierde nitidez al ampliarse.
- **Punto de corte (breakpoint):** ancho de pantalla en el que el diseño cambia de forma.
- **rem:** unidad de tamaño relativa al texto base de la página.
