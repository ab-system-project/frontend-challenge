# Agripay FrontEnd Challenge
## Requisitos
* Crear una carpeta que contenga un sitio web escrito en Angular 13 o superior con la siguiente estructura:
![alt text](https://github.com/ab-system-project/frontend-challenge/blob/main/design.png "Wireframe")
* El sitio consta de dos páginas principales, un inicio y una página de administración de usuarios.
* La página de inicio debe dar una bienvenida a quien ingresa al sitio y no hay diseño estipulado para ello.
* La página de administración de usuarios es la que se ve en el wireframe de la imagen.
* La tabla de la derecha debe recibir los datos de la api al ingresar a la página de administración.
* El botón 'Guardar' del formulario de la izquierda debe enviar los datos del formulario a la API.
* Luego de cada insercion exitosa, los datos del nuevo usuario deben ser ingresados a la tabla, sin necesidad de hacer un nuevo llamado a la API.
* El botón 'Limpiar'debe limpiar los campos del formulario.
* El número de seguro social (ssn), es único, y no puede haber dos usuarios con el mismo ssn en la lista.
* En caso de un intento de inserción erroneo, se debe informar dicho error al usuario.
* Al pasar 2 minutos de inactividad, se deben refrescar los datos de la tabla la tabla automáticamente.

## API
El sitio debe comunicarse con la API de este repositorio. La misma está escrita en Node.Js y consta de 2 endpoints:
* GET http://localhost:8081/api/members - para obtener los usuarios
* POST http://localhost:8081/api/members - para añadir un nuevo usuario
* Para poder comunicarse con la API, el Authorization header de la request debe formatearse como: 'Bearer [token]' .

## AUTH
Para poder utilizar los 2 endpoint anteriores debe obtener un token y enviarlo en los request.
* POST http://localhost:8081/auth - para obtener el token
body:
  "username": "sarah"
  "password": "connor"

### Iniciar API local
* Clonar este repositorio
* Instalar las dependencias
* Usar el comando "serve"

### Validaciones de la API
* **firstName, lastName y address:** Más de 1 caracter, sin espacios a los costados (trim)
* **ssn:** Tener el formato ###-##-#### (donde cada # es un número y los guiones son obligatorios)
* Si el front no cumple las validaciones debe deshabilitar el boton 'Guardar'

## Condiciones y tips
* Los colores y formas del wireframe son solo a caracter ilustrativo, podés modificarlo libremente siempre buscando que mantenga la arquitectura general establecida.
* La página de inicio no está diseñada y no necesario hacerlo, pero un mensaje de bienvenida no estaría mal.
* Podés importar las librerías externas que quieras.
* Podés utilizar el framework de estilos que más te guste, o hacer tus estilos propios.
* No es necesario que sea mobile responsive, pero suma.
* No es necesaria y no se verificará la compatibilidad con otros navegadores que no sean chrome.
* Podés usar ES6 sin problemas.
* Podés usar HTML5 sin ningun problema.
* Podés usar google y stackoverflow =).
* Podés y recomendamos usar POSTMAN para verificar el funcionamento de la API.
* Crear un archivo README.md para indicar como se debe utilizar su desarrollo.
* Subir a un repositorio git con privilegios de lectura públicos y compartir el link como resultado.
* Podés dockerizar el resultado final y publicar la imagen en dockerhub, no es necesario, pero suma.
* Se tendrán en cuanta cuestiones de clean-code, code-standard y mantenibilidad de código.
