---
sidebar_position: 6
---

# Async - Await

En React, las promesas son una forma de manejar operaciones **asíncronas** de manera más limpia y legible. Puedes usarlas para realizar operaciones como hacer solicitudes HTTP, cargar recursos o ejecutar código asíncrono en general. 

Actualmente, **async/await** es una forma muy común y recomendada de trabajar con promesas en JavaScript y, por lo tanto, también en React. Te permite escribir código asíncrono de una manera más legible y similar a código síncrono.

El uso de **async** antes de una función indica que la función devuelve una promesa, y **await** se utiliza para esperar el resultado de una promesa. Esto hace que el código sea mucho más claro y fácil de entender.

Aquí un ejemplo de cómo usar async/await con una solicitud HTTP en un componente React:

```js
import React, { useState, useEffect } from 'react';

const MiComponente = () => {
  const [datos, setDatos] = useState(null);

  useEffect(() => {
    const obtenerDatos = async () => {
      try {
        const response = await fetch('https://api.example.com/data');
        const data = await response.json();
        setDatos(data);
      } catch (error) {
        console.error('Error:', error);
      }
    };

    obtenerDatos();
  }, []);

  return (
    <div>
      {datos ? (
        <div>
          {/* Renderizar los datos */}
        </div>
      ) : (
        <div>Cargando...</div>
      )}
    </div>
  );
};

export default MiComponente;
```

## **CallBacks**

Antes de que se introdujera **async/await en ECMAScript 2017**, la forma común de manejar operaciones asíncronas en JavaScript era a través de **callbacks y promesas**.

**1. Callbacks -Promesas:**

Los callbacks eran funciones que se pasaban como argumentos a otras funciones y se ejecutaban una vez que la operación asíncrona se completaba.
Esto a menudo resultaba en código anidado conocido como **"callback hell" o "infierno de callbacks"**, lo cual era difícil de mantener y entender.

Ejemplo usando callbacks:

```js
function obtenerDatos(callback) {
  setTimeout(function() {
    const datos = 'Estos son los datos';
    callback(datos);
  }, 2000);
}

obtenerDatos(function(datos) {
  console.log(datos);
});
```

**2. Promesas:**

Las promesas proporcionaron una forma más estructurada y legible de manejar operaciones asíncronas, evitando el problema del callback hell.

Las promesas tienen dos posibles estados: **fulfilled (cumplida)** o **rejected (rechazada)** y permiten encadenar operaciones usando los métodos **.then() y .catch()**.

Ejemplo usando promesas:

```js
function obtenerDatos() {
  return new Promise((resolve, reject) => {
    setTimeout(function() {
      const exito = true; // Indica si la operación fue exitosa o no

      if (exito) {
        resolve('La operación fue exitosa');
      } else {
        reject('La operación falló');
      }
    }, 2000);
  });
}

obtenerDatos()
  .then((mensaje) => {
    console.log(mensaje); // La operación fue exitosa
  })
  .catch((error) => {
    console.error(error); // La operación falló
  });
```

Si bien las promesas proporcionaron una mejora significativa en la gestión de código asíncrono, **async/await** simplificó aún más el proceso al permitir que el código se escribiera de una manera que se asemeja al código síncrono, haciendo que sea más fácil de leer y mantener.