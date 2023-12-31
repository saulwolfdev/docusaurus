---
sidebar_position: 2
---

# Let y Const

Antes que nada cabe mencionar que las variables se declaraban anteriormente con **var** la razón por la que ya no se recomienda usar la palabra clave **var** en React (y en JavaScript en general) se debe a la introducción de **let y const** en ECMAScript 6 (ES6)

**let y const** tienen un alcance de bloque más estricto en comparación con **var**, lo que significa que solo están disponibles dentro del bloque donde se declaran (por ejemplo, dentro de una función o un bucle). Por otro lado, var tiene un alcance de función o global, lo que puede llevar a errores difíciles de depurar y a problemas de legibilidad en el código.

En React, se recomienda el uso de **const** para declarar variables que no van a ser reasignadas, y **let** para aquellas que sí pueden cambiar de valor. Esto ayuda a evitar errores sutiles y a escribir código más claro y predecible.
## **let:**
let es una palabra clave introducida en ECMAScript 6 (también conocido como ES6 o ECMAScript 2015) que permite declarar variables con alcance de bloque. Como se menciono anteriormente se pueden declarar variables con let para aquellas variables que pueden cambiar su valor.

Sintaxis:

```javascript
let variable = valor;
```

Ejemplo:

```javascript
let x = 10;

if (true) {
  let x = 20;
  console.log(x); // 20
}

console.log(x); // 10
```

En este ejemplo, la variable x declarada dentro del bloque if tiene un alcance limitado a ese bloque, mientras que la variable x declarada fuera del bloque if tiene un alcance global al script.

## **const:**
const es otra palabra clave introducida en ECMAScript 6. Al igual que let, permite declarar variables con alcance de bloque, pero a diferencia de let, las variables declaradas con const no pueden ser reasignadas después de su inicialización. Sin embargo, esto no significa que el valor es inmutable, solo que la variable no puede apuntar a otro valor.

Sintaxis:

```javascript
const variable = valor;
```
Ejemplo:

```javascript
const PI = 3.14;
PI = 42; // Error: No puedes reasignar una constante

const array = [1, 2, 3];
array.push(4); // Esto es válido, porque no estamos reasignando 'array', si bien es valido no es lo ideal ya que estariamos mutando el array

const newArray = [...array, 4]; //lo ideal seria utilizar el spread operator para evitar mutar el arreglo original.

console.log(newArray); // Output: [1, 2, 3, 4] 
```

En este ejemplo, PI no puede ser reasignada después de su inicialización. Sin embargo, el arreglo array puede ser modificado, aunque no puede apuntar a otro arreglo.

Es importante notar que cuando usas const con objetos o arreglos, el valor al que apunta (la referencia) no puede ser cambiado, pero los valores internos del objeto o arreglo sí pueden ser modificados.

## **Resumen:**

let se utiliza para declarar variables con alcance de bloque que pueden ser reasignadas.
const se utiliza para declarar constantes con alcance de bloque, cuyos valores no pueden ser reasignados después de la inicialización, aunque sus propiedades o elementos internos pueden ser modificados.
