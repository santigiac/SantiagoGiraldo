
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
  ```markdown
  ```html
  <html>
    <head></head>
  </html>
  ```
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
