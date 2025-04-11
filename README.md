
# APUNTES: GitHub, Markdown y HTML

## GitHub

### Configuración Inicial
1. **Instalar Git**: Descargar desde [git-scm.com](https://git-scm.com).  
2. **Configurar usuario**:
   ```bash
   git config --global user.name "Tu Nombre"
   git config --global user.email tu.email@ejemplo.com
   ```

### Comandos Básicos
- **Inicializar repositorio local**:  
  ```bash
  git init
  ```
- **Agregar archivos al área de preparación**:  
  ```bash
  git add archivo.txt   # Un archivo
  git add .             # Todos los archivos
  ```
- **Realizar un commit**:  
  ```bash
  git commit -m "Mensaje descriptivo"
  ```
- **Subir cambios a GitHub**:  
  ```bash
  git push origin main
  ```
- **Clonar un repositorio**:  
  ```bash
  git clone URL-del-repositorio
  ```
- **Actualizar cambios desde el remoto**:  
  ```bash
  git pull
  ```

### GitHub Pages
1. Configurar un repositorio público.
2. En `Settings > Pages`, seleccionar la rama y directorio (generalmente `main` y `root`).
3. El archivo principal debe llamarse `index.html`.

---

## Markdown

### Encabezados
```markdown
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

### Estilos de Texto
- **Cursiva**: `*texto*` o `_texto_`  
- **Negrita**: `**texto**` o `__texto__`  
- **Tachado**: `~~texto~~`

### Listas
- **Ordenadas**:
  ```markdown
  1. Elemento 1
  2. Elemento 2
  ```
- **Desordenadas**:
  ```markdown
  - Elemento 1
  - Elemento 2
  ```

### Código
- Línea de código: `` `código` ``
- Bloque de código:
  ```html
  <html>
    <head></head>
  </html>
  ```

### Enlaces e Imágenes
- **Enlace**:  
  ```markdown
  [Texto del enlace](https://ejemplo.com "Título opcional")
  ```
- **Imagen**:  
  ```markdown
  ![Alt text](URL "Título opcional")
  ```

### Tablas
```markdown
| Encabezado 1 | Encabezado 2 |
| ------------ | ------------ |
| Dato 1       | Dato 2       |
```

### Listas de Verificación
```markdown
- [ ] Tarea 1
- [x] Tarea 2
```

---

## HTML

### Estructura Básica
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Título de la página</title>
    <link rel="icon" href="favicon.ico">
  </head>
  <body>
    <h1>Encabezado</h1>
    <p>Párrafo</p>
  </body>
</html>
```

### Etiquetas Comunes
- **Encabezados**: `<h1>` a `<h6>`
- **Párrafo**: `<p>`
- **Listas**:
  ```html
  <ul>
    <li>Elemento desordenado</li>
  </ul>
  <ol>
    <li>Elemento ordenado</li>
  </ol>
  ```
- **Enlaces**:  
  ```html
  <a href="https://ejemplo.com">Texto del enlace</a>
  ```
- **Imágenes**:  
  ```html
  <img src="imagen.png" alt="Texto alternativo">
  ```
- **Comentarios**: 
  ```html
  <!-- Comentario -->
  ```
- **Agrupación de contenido**:
  - `<span>`: Agrupa contenido en línea, como texto dentro de un párrafo.
  - `<div>`: Agrupa contenido en bloque, como secciones o contenedores.
  
- **Estructura de la página**:
  - `<header>`: Encabezado de una página o sección.
  - `<footer>`: Pie de página.
  - `<article>`: Contenido independiente, como una entrada de blog o un artículo de noticias.
  - `<section>`: Sección de contenido relacionado.
  - `<nav>`: Enlaces de navegación.

### Formularios en HTML

Los **formularios** permiten interactuar con los usuarios y transmitir información al servidor. Incluyen una variedad de elementos para captar diferentes tipos de datos.

### Elementos de Formularios
- **Campos básicos**:
  - `<input>`: Define un campo de entrada de datos.
    - **Atributos comunes**:
      - `type`: Define el tipo de entrada (texto, email, contraseña, etc.).
      - `name`: Nombre del campo para identificarlo.
      - `value`: Establece el valor inicial del campo.
      - `placeholder`: Muestra un texto indicativo dentro del campo.
      - `required`: Hace obligatorio rellenar el campo.
      - `disabled`: Desactiva el campo, no permite interacción.
      - `readonly`: Campo de solo lectura.
    - **Tipos de `<input>` más comunes**:
      - `text`: Entrada de texto.
      - `email`: Entrada con validación de formato de correo electrónico.
      - `password`: Entrada oculta para contraseñas.
      - `submit`: Botón para enviar el formulario.
      - `reset`: Botón para restablecer todos los campos.

- **Campo de texto grande**:
  - `<textarea>`: Campo para escribir textos largos.
    - **Atributos comunes**:
      - `cols`: Ancho en número de columnas.
      - `rows`: Alto en número de filas.

- **Listas de selección**:
  - `<select>`: Campo para elegir entre varias opciones.
    - **Subetiqueta**:
      - `<option>`: Define una opción dentro de la lista.

---

### Ejemplo de Formulario Completo
```html
<form action="/submit" method="post">
  <!-- Campo de texto -->
  <label for="name">Nombre:</label>
  <input type="text" id="name" name="user_name" placeholder="Tu nombre" required>

  <!-- Campo de correo -->
  <label for="email">Correo Electrónico:</label>
  <input type="email" id="email" name="user_email" placeholder="ejemplo@correo.com" required>

  <!-- Contraseña -->
  <label for="password">Contraseña:</label>
  <input type="password" id="password" name="user_password" required>

  <!-- Campo de texto grande -->
  <label for="message">Mensaje:</label>
  <textarea id="message" name="user_message" cols="30" rows="5" placeholder="Escribe aquí..."></textarea>

  <!-- Lista de selección -->
  <label for="options">Elige una opción:</label>
  <select id="options" name="user_option">
    <option value="opcion1">Opción 1</option>
    <option value="opcion2">Opción 2</option>
    <option value="opcion3">Opción 3</option>
  </select>

  <!-- Botones -->
  <button type="submit">Enviar</button>
  <button type="reset">Restablecer</button>
</form>
```	

# CSS: Propiedades, Selectores y Diseño Responsive

## CSS: Propiedades Básicas

Las propiedades básicas de CSS nos permiten dar estilo y formato a los elementos HTML. A continuación, te explico las más comunes:

```css
/* Cambia el color del texto */
color: red;

/* Cambia el color de fondo del elemento */
background-color: yellow;

/* Define el tamaño del texto */
font-size: 16px; /* Puede usar px, em, rem, %, etc. */

/* Define el tipo de letra */
font-family: Arial, sans-serif;

/* Grosor del texto */
font-weight: bold; /* También puede ser normal, lighter, o valores numéricos como 400, 700 */

/* Estilo del texto */
font-style: italic; /* También puede ser normal, oblique */

/* Alineación del texto */
text-align: center; /* También puede ser left, right, justify */

/* Espaciado interno: espacio entre el borde y el contenido */
padding: 10px; /* Puede especificarse para cada lado: padding-top, padding-right, etc. */

/* Espaciado externo: espacio entre el borde y otros elementos */
margin: 15px; /* Igual que padding, puede ir por lados o usar la propiedad global */

/* Borde del elemento */
border: 1px solid black; /* Grosor | estilo | color */

/* Ancho y alto del elemento */
width: 200px;
height: 100px;

/* Oculta el elemento (no ocupa espacio) */
display: none;

/* Muestra el elemento como bloque (ocupa todo el ancho disponible) */
display: block;

/* Muestra el elemento en línea (dentro de la misma línea) */
display: inline;

/* Hace que el elemento flote a un lado (izquierda o derecha) */
float: left;

/* Posición del elemento: relativa, absoluta, fija o sticky */
position: relative;

/* Añade sombra a la caja */
box-shadow: 2px 2px 5px gray;

/* Redondea las esquinas del elemento */
border-radius: 10px;

/* Espaciado entre letras */
letter-spacing: 1px;

/* Espaciado entre líneas de texto */
line-height: 1.5;

/* Opacidad del elemento (0 = invisible, 1 = visible) */
opacity: 0.8;
```

## CSS: Selectores

### Selectores Básicos

```css
p {
  color: blue;
}

.titulo {
  font-size: 24px;
  color: green;
}

#especial {
  background-color: lightgray;
}

* {
  font-family: sans-serif;
}
```

### Selectores Combinados

```css
div p {
  color: purple;
}

div > p {
  font-weight: bold;
}

h2 + p {
  color: orange;
}
```

### Pseudoclases

```css
a:hover {
  color: red;
}

a:visited {
  color: gray;
}

a:active {
  font-weight: bold;
}

li:first-child {
  color: blue;
}
```

### Pseudoelementos

```css
p::first-letter {
  font-size: 2em;
  color: red;
}

p::first-line {
  font-weight: bold;
}

h1::before {
  content: "👉 ";
}
```

### Selectores de Atributo

```css
img[alt] {
  border: 2px dashed red;
}

a[href="https://google.com"] {
  color: green;
}
```

## CSS: Diseño Responsive

### Meta Viewport

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Media Queries

```css
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }

  .column {
    width: 100%;
  }
}

@media (min-width: 768px) {
  .column {
    width: 50%;
  }
}

@media (min-width: 320px) and (max-width: 480px) {
  p {
    font-size: 14px;
  }
}
```

### Orientación del dispositivo

```css
@media (orientation: landscape) {
  body {
    background-color: lightgreen;
  }
}
```

### Mobile First

```css
.container {
  width: 100%;
  font-size: 14px;
}

@media (min-width: 768px) {
  .container {
    width: 80%;
    font-size: 16px;
  }
}
```

### Unidades recomendadas

- `em`, `rem`: relativas al tamaño de fuente.
- `%`: relativo al contenedor.
- `vh`, `vw`: porcentaje del alto/ancho de la ventana.

### Ejemplo completo

```css
body {
  font-family: sans-serif;
  font-size: 14px;
  background-color: white;
}

@media (min-width: 600px) {
  body {
    font-size: 16px;
  }
}

@media (min-width: 992px) {
  body {
    font-size: 18px;
    margin: 0 auto;
    max-width: 960px;
  }
}
```

