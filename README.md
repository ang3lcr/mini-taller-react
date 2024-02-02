# Taller React

## Que es React?

React es una librería Javascript de código abierto diseñada para crear interfaces de usuario con el objetivo de facilitar el desarrollo de aplicaciones en una sola página. Es mantenido por Facebook y la comunidad de software libre. En el proyecto hay más de mil desarrolladores libres.

## Requisitos

- [Node](https://nodejs.org/en)

## Crear proyecto de React

```bash
npm create vite@latest
cd <nombre-del-proyecto>
npm install
```

---

## Limpiar proyecto nuevo

- Eliminar App.css
- Eliminar index.css
- Eliminar imports en App.jsx
- Eliminar imports en main.jsx
- Dejar solo un <div> en App.jsx

---

## Componente

Los componentes **permiten separar la interfaz de usuario en piezas independientes, reutilizables y pensar en cada pieza de forma aislada**. En esencia son archivos separados que contienen la logica de una parte de todo el proyecto.

---

## Crear componente

Primeramente crearemos una carpeta nueva llamada “components” dentro de la carpeta “src”. Cada nuevo componente que creemos lo almacenaremos aqui.

Para crear un nuevo componente creamos un archivo dentro de la carpeta components siguiendo ciertas reglas:

- El nombre de un componente debe iniciar con una letra mayuscula.
- La extension del archivo sera “.jsx”

Abrimos nuestro archivo de componente e ingresamos el comando “rafce” y presionamos tabulador, de esta forma la extension de snippets nos creara la estructura de un componente de React.

---

## Estructura de un Componente

Podemos dividir la estructura de un componente de React en dos partes, la parte logica y la parte visual.

La parte logica de un componente, es aquella que como su nombre lo indica lleva la parte logica/programable de un componente, dentro de esta division ingresamos codigo de JavaScript para controlar el comportamiento de nuestro componente. La parte logica del componente se encuentra delimitada por un llave de apertura “{” y la palabra “return”.

```jsx
import React from 'react'

const Componente = () => {
//
//
//        Logica
//
//
  return (
    <div>
        
    </div>
  )
}

export default Componente
```

La segunda parte de un componente es la parte visual, que es donde pondremos todo el codigo HTML que renderizara el navegador. Esta se encuentra delimitada dentro de la etiqueta <div>.

```jsx
import React from 'react'

const Componente = () => {
//
//
//        Logica
//
//
  return (
    <div>
        Visual
    </div>
  )
}

export default Componente
```

---

## Creando una barra de navegacion

1. Crear archivo“NavBar.jsx”
2. Crear componente
    
    ```jsx
    import React from 'react'
    
    const NavBar = () => {
      return (
        <div>NavBar</div>
      )
    }
    
    export default NavBar
    ```
    
3. Escribimos una estructura HTML para una barra de navegacion en la parte visual del componente
    
    ```jsx
    import React from 'react'
    
    const NavBar = () => {
      return (
        <div>
            <ul>
                <li>Home</li>
                <li>About</li>
                <li>Services</li>
            </ul>
        </div>
      )
    }
    
    export default NavBar
    ```
    
4. Agregamos clases para aplicar estilos con CSS
    
    ```jsx
    import React from 'react'
    
    const NavBar = () => {
      return (
        <div className='NavBar'>
            <ul className='Navbar__ul'>
                <li className='NavBar__li'>Home</li>
                <li className='NavBar__li'>About</li>
                <li className='NavBar__li'>Services</li>
            </ul>
        </div>
      )
    }
    
    export default NavBar
    ```
    
5. Creamos una carpete de estilos llamada “styles” dentro de la carpeta “src”
6. Creamos un archivo para los estilos de la Navbar llamada “navbar.css”
7. Enlazamos el archivo css a nustro componente con import
    
    ```jsx
    import React from 'react'
    import "../styles/navbar.css" //importamos el archivo de estilos
    
    const NavBar = () => {
      return (
        <div className='NavBar'>
            <ul className='Navbar__ul'>
                <li className='NavBar__li'>Home</li>
                <li className='NavBar__li'>About</li>
                <li className='NavBar__li'>Services</li>
            </ul>
        </div>
      )
    }
    
    export default NavBar
    ```
    
8. Agregamos nuestros estilos
    
    ```css
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    
    .NavBar{
       width: 100%;
       height: 50px;
       display: flex;
       justify-content: space-between;
       background-color: rgb(0, 0, 0);
    }
    
    .NavBar__img{
        width: auto;
        margin-left: 20px;
    }
    
    .Navbar__ul{
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        width: 40%;
        align-items: center;
    }
    
    .NavBar__li{
        list-style: none;
        color: white;
    }
    ```