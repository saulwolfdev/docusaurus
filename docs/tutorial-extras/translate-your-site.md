---
sidebar_position: 2
---

# Creacion y Uso

## **Creacion de Componente en React y Uso**
Para crear un componente en React se puede hacer de dos maneras: como componente de función o como componente de clase.

Dentro de la carpeta src, crea un nuevo archivo con el nombre de tu componente, por ejemplo Component.js.

- ## Crear un componente de clase (menos habitual con la incorporación de los hooks):
Esta manera de escribir se usaba antes de ECMAScript 6(ES6)
```js
import React, { Component } from 'react';

class myComponent extends Component {
  render() {
    return <h1>Hola, {this.props.nombre}</h1>;
  }
}

export default myComponent;
```

- ## Crear un componente de función:
```js
import React from 'react';

function myComponent(props) {
  return <h1>Hola, {props.nombre}</h1>;
}

export default myComponent;
```

## **Uso**

Una vez que creas tu componente, puedes usarlo en otros componentes de la siguiente manera:
```js
import React from 'react';
import myComponent from './Component';

function App() {
  return (
    <div className="App">
      <MiComponente nombre="Mundo" />
    </div>
  );
}

export default App;
```