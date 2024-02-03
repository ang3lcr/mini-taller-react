# Taller React

## Que es React? 🤔

React es una librería Javascript de código abierto diseñada para crear interfaces de usuario con el objetivo de facilitar el desarrollo de aplicaciones en una sola página. Es mantenido por Facebook y la comunidad de software libre. En el proyecto hay más de mil desarrolladores libres.

## Requisitos ✔

- [Node](https://nodejs.org/en)

## Crear proyecto de React

```bash
npm create vite@latest
cd <nombre-del-proyecto>
npm install
```

---

## Limpiar proyecto nuevo 🕸

- Eliminar App.css
- Eliminar index.css
- Eliminar imports en App.jsx
- Eliminar imports en main.jsx
- Dejar solo un <div> en App.jsx

---

## Ejemplo de proyecto limpio

```jsx
function App() {

  return (
    <div>
      
    </div>
  )
}

export default App
```

```jsx
import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App.jsx'

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
)
```

## Componentes ⚙

Los componentes **permiten separar la interfaz de usuario en piezas independientes, reutilizables y pensar en cada pieza de forma aislada**. En esencia son archivos separados que contienen la logica de una parte de todo el proyecto.

---

## Crear componente 🐱‍💻

Para comenzar, crearemos una nueva carpeta llamada **"/components"** dentro de la carpeta **"/src"**. Todos los nuevos componentes que creemos se almacenarán aquí.

Para crear un nuevo componente creamos un archivo dentro de la carpeta components siguiendo ciertas reglas:

- El nombre de un componente debe iniciar con una letra mayuscula.
- La extension del archivo sera “.jsx”

Para crear la estructura básica de un componente de React, abrimos nuestro archivo de componente y escribimos "rafce". Luego, presionamos la tecla Tab, lo que activará la extensión de snippets para generar automáticamente la estructura del componente.

---

## Estructura de un Componente 💾

La estructura de un componente de React puede dividirse en dos partes distintas: la parte lógica y la parte visual.

La sección lógica de un componente es aquella que, como su nombre sugiere, contiene la parte lógica/programable del componente. Dentro de esta división, introducimos código en JavaScript para controlar el comportamiento de nuestro componente. La sección lógica del componente está delimitada por una llave de apertura "{" y la palabra "return".

```jsx
import React from 'react'

const Componente = () => {

	
			//Logica

  return (
    <div>
        
    </div>
  )
}

export default Componente
```

La segunda parte de un componente es la parte visual, donde ubicamos todo el código HTML que será renderizado por el navegador. Esta sección está delimitada dentro de la etiqueta **`<div>`**.

```jsx
import React from 'react'

const Componente = () => {

	
			

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

1. Creamos el archivo“NavBar.jsx”
2. Creamos un componente
    
    ```jsx
    import React from 'react'
    
    const NavBar = () => {
      return (
        <div>NavBar</div>
      )
    }
    
    export default NavBar
    ```
    
3. En la sección visual del componente, escribimos una estructura HTML para una barra de navegación.
    
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
    
4. Agregamos clases para aplicar estilos con CSS.
    
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
    
5. Creamos una carpeta de estilos llamada “styles” dentro de la carpeta ***/src***
6. Creamos un archivo para los estilos de la Navbar llamada ***navbar.css***
7. Enlazamos el archivo css a nuestro componente con `import`
    
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
    
9. Importamos nuestro componente en el archivo ***App.jsx***
    
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
    
    ## Abrir proyecto en navegador
    
    Ejecutamos este comando en una terminar ubicados en la raiz del proyecto.
    
    ```bash
    npm run dev
    ```