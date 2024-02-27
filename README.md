# Topicos
## Descripcion general del repositorio 
Este repositoria crea una serie de scripts, cada uno con una funcionalidad diferente, para generar contenido en paginas web. 

---
### Descripcion de los scripts


### Script-1 Contenedores
El script genera 10 contenedores de tamaño 100, y les agrega de manera aleatoria 10 colores. 

1. **Función colorAleatorio**
   - Esta función devuelve un color aleatorio de una lista predefinida.
2. **Generar contenedores**
   - Se crean 10 contenedores con un bucle `for` y se le aplican los estilos correspondientes con nuestra funcion `colorAleatorio`
   - Se agrega al `body` del html

``` javaScript 
const body = document.querySelector('body')
const colores = ['LigthPink', 'HotPink', 'Khaki', 'Lavender', 'Violet', 'Purple', 'Indigo', 'SpringGreen', 'SkyBlue', 'Navy'];

for(let i = 0 ; i < 10 ; i++){
    const div = document.createElement('div')
    div.style.height = '100px'
    div.style.width = '100px'
    div.style.backgroundColor = colores[Math.floor(Math.random()*colores.length)]
    body.appendChild(div) 
}
```

### Script-2 Contenedores 1.2
Con el script anterior, nos aseguramos que los colores no se repitan en los contenedores

1. **Creación de una lista de colores únicos**:
   - Se define una lista `colores` con una variedad de colores predefinidos, en esta ocasion 10.
   - Se crea una lista vacía de `coloresUnicos` para almacenar los colores ya seleccionados.
   - Se utiliza `while` para seleccionar aleatoriamente colores de la lista `colores` y ponerlos en `coloresUnicos` hasta que haya 10 colores distintos, asegurandonos que no esten ya en el arreglo.

2. **Generación de elementos `<div>`**:
   - Con un bucle `for`, en cada iteración, se crea un contenedor y se le asignan estilos de tamaño y color de fondo utilizando el color correspondiente de `coloresUnicos`.
   - Se agrega al `body` del html

``` javaScript 
let colores = ['LigthPink', 'HotPink', 'Khaki', 'Lavender', 'Violet', 'Purple', 'Indigo', 'SpringGreen', 'SkyBlue', 'Navy', 'Coral', 'Teal', 'Magenta', 'Turquoise', 'Crimson', 'Maroon', 'SlateGray', 'DarkOrange', 'DarkCyan', 'DarkRed'];
let coloresUnicos = []

while (coloresUnicos.length < 10) {
    let color = colores[Math.floor(Math.random() * colores.length)]
    if (!coloresUnicos.includes(color)) {
        coloresUnicos.push(color)
    }
}

for (let i = 0; i < coloresUnicos.length; i++) {
    let contenedor = document.createElement('div')
    contenedor.style.width = '100px'
    contenedor.style.height = '100px'
    contenedor.style.backgroundColor = coloresUnicos[i]
    document.body.appendChild(contenedor)
}
```

### Script-3 Parrafos inteligentes
Un script que es capaz de generar 5 parrafos, con una longitud de 50 a 100 palabras aleatoriamente, ademas muestra la cantidad de caracteres en cada parrafo

1. **Texto aleatorio**:
   - Se crea un arreglo de palabras aleatorias
   - La función `textoAleatorio()` genera texto aleatorio seleccionando palabras de `palabras`, y se asegura quela longitud se encuentre entre 50 y 100 palabras

2. **Creacion de los parrafos**
   - Con ayuda de un blucle`for`se genera texto aleatorio utilizando la función `textoAleatorio()`.
   - Se crea un elemento `<p>` y se le asigna el texto generado, seguido de la longitud del texto en paréntesis.
   - Se agrega al `body` del html

``` javaScript 
let colores = ['LigthPink', 'HotPink', 'Khaki', 'Lavender', 'Violet', 'Purple', 'Indigo', 'SpringGreen', 'SkyBlue', 'Navy', 'Coral', 'Teal', 'Magenta', 'Turquoise', 'Crimson', 'Maroon', 'SlateGray', 'DarkOrange', 'DarkCyan', 'DarkRed'];
let coloresUnicos = []

while (coloresUnicos.length < 10) {
    let color = colores[Math.floor(Math.random() * colores.length)]
    if (!coloresUnicos.includes(color)) {
        coloresUnicos.push(color)
    }
}

for (let i = 0; i < coloresUnicos.length; i++) {
    let contenedor = document.createElement('div')
    contenedor.style.width = '100px'
    contenedor.style.height = '100px'
    contenedor.style.backgroundColor = coloresUnicos[i]
    document.body.appendChild(contenedor)
}
```
