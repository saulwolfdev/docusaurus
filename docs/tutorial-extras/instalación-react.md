---
sidebar_position: 1
---

# Instalación de React

## Paso 1: Instalar Node.js y npm

Antes de instalar React, asegúrate de tener Node.js y npm (Node Package Manager) instalados en tu sistema. Puedes descargarlos desde el [sitio oficial de Node.js](https://nodejs.org/).

## Que es Node:

- Node.js es un entorno de ejecución de código JavaScript del lado del servidor. Permite a los desarrolladores utilizar JavaScript para escribir scripts del lado del servidor en lugar de depender de lenguajes como PHP o Python.

- Node.js está construido sobre el motor V8 de Google Chrome, que es conocido por ser rápido y eficiente en la ejecución de código JavaScript. Esto hace que Node.js sea una opción popular para construir aplicaciones web escalables y de alto rendimiento.

- Además de ser utilizado para crear servidores web, Node.js también se utiliza comúnmente para construir aplicaciones de red, herramientas de línea de comandos y otros tipos de software. Su naturaleza asincrónica y orientada a eventos lo hace adecuado para tareas que involucran muchas operaciones de entrada/salida (I/O) no bloqueantes.

- Node.js cuenta con un ecosistema robusto de bibliotecas y módulos de código abierto, gracias a **npm (Node Package Manager)**, que es el gestor de paquetes de JavaScript más grande del mundo. Esto facilita la integración de diversas funcionalidades en las aplicaciones.

- En resumen, Node.js es una plataforma que permite a los desarrolladores utilizar JavaScript en el lado del servidor, lo que abre muchas posibilidades para la construcción de aplicaciones y herramientas web eficientes y escalables.

## Paso 2: Crear una nueva aplicación de React

Abre tu terminal y ejecuta el siguiente comando para crear una nueva aplicación de React:

```bash
npx create-react-app my-app
```
## Paso 3:

Una vez que la aplicación se haya creado, navega al directorio de tu aplicación usando el siguiente comando:

```bash
cd my-app
```

Luego, inicia la aplicación con el siguiente comando:
```bash
npm start
```
Esto abrirá un servidor local y podrás ver tu aplicación creada de React en tu navegador.

## Estructura del Proyecto
El proyecto de React tiene la siguiente estructura básica:
```bash
my-app/
  ├── node_modules/
  ├── public/
  ├── src/
  ├── .gitignore
  ├── package.json
  ├── README.md

```
- node_modules/: Contiene todas las dependencias de tu proyecto.
- public/: Contiene archivos estáticos y el archivo index.html que es el punto de entrada de tu aplicación.
- src/: Contiene el código fuente de tu aplicación.
- .gitignore: Especifica los archivos y directorios que deben ser ignorados por Git.
- package.json: Archivo de configuración que contiene la lista de dependencias y scripts de tu proyecto.
- README.md: Este archivo, que es donde estamos escribiendo, es la documentación de tu proyecto en formato Markdown.