---
sidebar_position: 8
---

# Métodos para Strings y Arrays

En React, como en JavaScript en general, se puede utilizar métodos para manipular strings o arrays.

# **Métodos para Strings:**

**1. str.length**
Descripción: Retorna la longitud de una cadena de texto.
Uso:

```js
const str = "Hola Mundo";
const length = str.length; // 10
```

**2. str.toLowerCase(), str.toUpperCase()**
Descripción: Convierte una cadena de texto a minúsculas o mayúsculas respectivamente.
Uso:
```js
const str = "Hola Mundo";
const lowerCase = str.toLowerCase(); // "hola mundo"
const upperCase = str.toUpperCase(); // "HOLA MUNDO"
```

**3. str.trim()**
Descripción: Elimina los espacios en blanco al principio y al final de una cadena de texto.
Uso:

```js
const str = "    Hola Mundo    ";
const trimmed = str.trim(); // "Hola Mundo"
```

**4. str.split(separator)**
Descripción: Divide una cadena de texto en un array de substrings basado en un separador.
Uso:

```js
const str = "Hola,Mundo";
const parts = str.split(","); // ["Hola", "Mundo"]
```

**5. str.includes(substring)**
Descripción: Verifica si una cadena de texto contiene un substring especificado.
Uso:

```js
const str = "Hola Mundo";
const containsHello = str.includes("Hola"); // true
```

# **Métodos para Arrays:**

**1. arr.length**
Descripción: Retorna la cantidad de elementos en un array.
Uso:

```js
const arr = [1, 2, 3, 4];
const length = arr.length; // 4
```

**2. arr.push(element)**
Descripción: Añade un elemento al final del array.
Uso:

```js
const arr = [1, 2, 3];
arr.push(4); // arr ahora es [1, 2, 3, 4]
```

**3. arr.pop()**
Descripción: Elimina el último elemento del array y lo retorna.
Uso:

```js
const arr = [1, 2, 3, 4];
const lastElement = arr.pop(); // lastElement = 4, arr = [1, 2, 3]
```

**4. arr.map(callback)**
Descripción: Crea un nuevo array aplicando una función a cada elemento del array original.
Uso:

```js
const arr = [1, 2, 3];
const mappedArr = arr.map(item => item * 2); // [2, 4, 6]
```

**5. arr.filter(callback)**
Descripción: Crea un nuevo array con todos los elementos que pasen una condición.
Uso:

```js
const arr = [1, 2, 3, 4, 5];
const filteredArr = arr.filter(item => item % 2 === 0); // [2, 4]
```

Estos son algunos métodos que son nativos de JavaScript y se pueden utilizar en cualquier proyecto de React. Para utilizarlos en tu aplicación simplemente accede a las propiedades y métodos de los strings y arrays como se haria en JavaScript estándar.