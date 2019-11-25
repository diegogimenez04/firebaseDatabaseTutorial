# Firebase

## Este turorial va a explicar en 6 pasos como crear una base de datos en Firebase.

---

### Paso Nº1:

Lo primero que hay que hacer es ingresar con una cuenta de Google a firebase, y luegi crear un proyecto, para esto primero debemos darle nombre, en este caso vamos a desactivar "Google Analytics", y luego en continuar. Una vez creado el proyecto vamos al paso Nº2.

---

### Paso Nº2:

Una vez estemos en la pagina principal del proyecto. Debemos seleccionar la opción de "Web". Luego de esto, debemos registrar un sobrenombre de la app en el campo de texto que tenemos a simple vista, en este ejemplo, incluiremos la opcion de "Firebase Hosting", y por ultimo registrar app. Copiamos todo lo que nos aparece en el recuadro y lo mantendremos en algun lado hasta que nos sea util, luego clickeamos siguiente. Nos va a pedir que instalemos CLI (Command Line Interface), para lo cual necesitaremos npm (Node Package Manager), el cual se puede encontrar [aqui](https://nodejs.org/). Una vez instalada necesitaremos ejecuta unos comandos para poder usar las herramientas de firebase, el comando es: [npm install -g firebase-tools] (sin los corchetes). Una vez tengamos el CLI vamos a hacer lo siguiente en la terminal. Primero ejercutaremos el comando [firebase login] en el caso que no hayamos iniciado sesion antes por este medio. Luego, buscaremos un directorio vacio donde crear nuestro proyecto e inicializaremos el proyecto con el comando [firebase init]. Por ultimo, cuando estemos listos para mostrar la pagina ejecutaremos el comando [firebase deploy].

---

### Paso Nº3: (Saltear este paso si el proyecto ya esta creado con CLI) 
Una vez ejecutado el comando [firebase init], nos preguntara si estamos listos, a lo cual presionaremos "Y" y enter. Luego de eso, nos preguntara que deseamos implementar al proyecto, en este caso solamente manejaremos una base de datos, por lo que seleccionaremos "Database" y "Hosting", luego seleccionaremos nuetro proyecto y daremos a la tecla enter, luego daremos de vuelta a la misma tecla enter, y una ultima vez. Nos preguntara si queremos crear una aplicacion de una sola pagina, en este ejemplo le daremos a la "y" es decir que si.

---

### Paso Nº4:
Una vez en el directorio del proyecto, ejecutaremos el comando [firebase deploy] y veremos que nuestro proyecto ya esta en funcionamiento al entrar en el IP que nos muestra. En caso de querer testear nuestra aplicacion ejecutaremos [firebase serve] y podremos ver los cambios en tiempo real de nuestra app. Entraremos en la carpeta del proyecto y abriremos la carpeta con un editor de texto, y editaremos el archivo "index.html". Limpiaremos el tag de <body> hasta que nos quede vacio, es decir <body> </body>, tambien borraremos el tag <style></style> completamente.
Una vez terminado esto, crearemos un tag <script type="text/javascript" src="index.js"></script> al final de el tag <head> (es decir una linea antes de </head>).
Y por ultimo crearemos un script llamado index.js en el mismo directorio.

---

### Paso Nº5:
Cuando tengamos el archivo index.js, entraremos en el mismo con un editor de texto y copiaremos la configuracion que nos proporciona la pagina. Agregando al final una linea de codigo que diga lo siguiente: firebase.initializeApp({nombre de la variable en la que esta guardada la configuracion});  (Por defecto es configApp).
Una vez hecho esto vamos a la pagina principal e implementaremos la base de datos. Para lo cual nos vamos al apartado de database y clickeamos donde dice "Crear base de datos". Inicializamos en modo de prueba, esto nos dejara manipular la base de datos a gusto, no es recomendable a la hora de usarse para produccion pero mientras tanto, vamos a dejarla asi. Por ultimo ingresaremos un objeto nuevo dependiendo de lo que queramos hacer con la base de datos, si no se sabe como realizar esto es posible [ver este video](https://youtu.be/gyDGlgvG_qM?t=163).

---

### Paso Nº6
Una vez creada la base de datos, ingresaremos un campo de usuarios con algunos objetos dentro de el. Vamos a index.js e ingresamos lo siguiente en una nueva linea para que sea mas legible: [var database = firebase.database();]. Y ya tendremos conectado nuestra aplicacion con la base de datos creada.