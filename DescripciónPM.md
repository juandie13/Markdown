# Definición de Requerimientos de Aplicativo de Chat

**Integrantes:**

* Castillo Carnero, Juan Diego - 20183730

* Cruz Ramirez, Gabriel - 20180515

* Hermitaño Castro, Juler - 20182700

* Micali Morales, Mauricio José - 20191288

**Profesor:**
José Jesús Valdivia Caballero


## EXPLICACIÓN DEL ENTORNO DE DESARROLLO

La presente sección se centrará en la instalación y configuración del SDK Flutter y el lenguaje de programación Dart. 
Previamente, se recomienda, tener instalado las siguientes herramientas: 
1. [Git](https://git-scm.com/downloads) para sistema de control de versiones.
2. [Postman](https://www.postman.com/downloads/) para el uso de APIs y peticiones
3. [VSCode](https://code.visualstudio.com/download) como editor de texto.
4. [Xcode](xcodereleases), [Android Studio](https://developer.android.com/studio) o cualquier simulador de dispositivos móviles. 

### __Instalación de Flutter:__

Primero, deberán dirigirse a la página oficial de [Flutter](https://flutter.dev/) y dar click en la sección de “Get started”

![alt](/Pictures/Diapositiva1.PNG)

Una vez en la página, seleccionamos el Sistema Operativo de nuestra preferencia

![alt](/Pictures/Diapositiva2.PNG)

### __Instalación en macOS__

Al seleccionar el SO macOS en la imagen anterior, deriva a la siguiente página en la que se debe seleccionar el procesador con la cuenta la mac (Intel o Apple Silicon)

![alt](/Pictures/Diapositiva3.PNG)

Al seleccionar el procesador indicado, descargará un .xip portable. Este debe ser descomprimido, como recomendación, en la siguiente ruta:

![alt](/Pictures/Diapositiva4.PNG)

Si no se cuenta con la carpeta “Development”, solo debe crearse.

A continuación, se debe añadir Flutter al path para que sea accesible desde cualquier lugar. Para esto, se debe ingresar a la terminal y seguir los siguientes comandos:


![alt](/Pictures/Diapositiva5.PNG)

Esto quiere decir que debemos dirigirnos a nuestra carpeta de usuario y abrir el archivo “.zshrc”, el cual, si no se ha creado, debe hacerse.

Dentro de este archivo, se debe colocar lo siguiente cambiando la ruta por la correcta donde se encuentra la carpeta bin.

![alt](/Pictures/Diapositiva6.PNG)

Salimos del entorno de edición presionando la tecla “Esc” y luego escribiendo “wq”, lo cual significa “write” y “quit”

Para verificar si la instalación se dio de manera correcta, debemos cerrar la terminal y abrir otra. Luego, escribimos el comando “Flutter --version” y debería salir lo siguiente:

![alt](/Pictures/Diapositiva7.PNG)

### __Instalación en Windows__
Lo primero a realizar es ir a la página de web de Flutter SDK y elegir el sistema operativo en el que se va a trabajar. Para este caso, se utilizará Windows.

![alt](/Pictures/Diapositiva8.PNG)

Posterior a la elección de Windows, nos sale la siguiente pantalla en la que haremos clic en el botón celeste. Esto para descargar el archivo .zip y realizar la instalación.

![alt](/Pictures/Diapositiva9.PNG)

Posterior a la descarga del archivo .zip, descomprimimos el archivo y lo copiamos directamente en el disco local C.

![alt](/Pictures/Diapositiva10.PNG)

Luego de ello, toca generar la variables en el PATH del sistema operativo. En el nos vamos a las variables de entorno, y en el Path nos vamos a editar y copiamos la dirección de la carpeta BIN que está dentro de la carpeta flutter. Guardamos y aceptamos los cambios.

![alt](/Pictures/Diapositiva.PNG)

Por último, para comprobar la instalación del flutter, abrimos un cmd o powershell y escribimos “flutter --version”. Si sale el siguiente resultado, es porque se logró una instalación satisfactoria de flutter. En caso de error, revisar el PATH.

![alt](/Pictures/Diapositiva11.PNG)

### __Configuración en VSCode__

Instalar la extensión del lenguaje Dart en Vscode:

![alt](/Pictures/Diapositiva12.PNG)

Instalar la extensión del framework Flutter en Vscode:

![alt](/Pictures/Diapositiva13.PNG)

## Diagrama de despligue

![alt](/Pictures/Diapositiva14.PNG)

## Requerimientos no funcionales

__RNF1:  Rendimiento__

* La aplicación debe cargar y mostrar la pantalla principal en un tiempo máximo de 3.5 segundos, en todas las plataformas compatibles.
* El tiempo de respuesta para enviar y recibir mensajes en la pantalla de chat no debe exceder los 1,5 segundos, incluso en condiciones de baja conectividad.
* El tiempo de respuesta para los resultados de búsqueda en pantalla no debe exceder los 2 segundos.

__RNF2: Seguridad:__
* Proteger la comunicación entre la aplicación y Firebase mediante el uso de HTTPS para garantizar la confidencialidad de los datos transferidos.

__RNF3: Usabilidad__
*  La interfaz de usuario de la página de inicio de sesión debe seguir las pautas de diseño para la plataforma respectiva (Android e iOS), no obstante, cada una debe proporcionar una experiencia familiar y coherente con las demás.
* La página de chat debe tener un diseño intuitivo y fácil de usar, con una disposición clara de mensajes y funciones de interacción claramente identificables.

__RNF4: Fiabilidad__
* La aplicación debe ser capaz de manejar la conexión intermitente o la pérdida momentánea de conectividad de red permitiéndole al usuario mantener su sesión abierta, almacenando los mensajes enviados sin conexión y sincronizándolos automáticamente una vez que se restablezca la conexión.
* La aplicación deberá de ser tolerante a errores siendo capaz de poderse realizar las funcionalidades principales a pesar de errores.

__RNF5: Escalabilidad__
* La aplicación debe ser capaz de manejar un crecimiento en la cantidad de usuarios registrados y grupos de chat, manteniendo un rendimiento óptimo sin afectar la experiencia del usuario.

__RNF6: Mantenibilidad__
* Se deben agregar comentarios y documentación adecuada para facilitar la comprensión del código y el trabajo en equipo.
* La estructura de carpetas y orden del código debe mantenerse según las prácticas recomendadas por la comunidad de flutter.

__RNF7: Compatibilidad__
* La aplicación debe ser compatible con las últimas versiones de los sistemas operativos móviles (Android e iOS) para garantizar una experiencia uniforme en todas las plataformas compatibles.

## Requerimientos funcionales

__RF1: Login en la plataforma:__
* El usuario, previamente registrado, debe ser capaz de acceder a una pantalla de Login, en la cual al poner sus datos debe ingresar al servicio de mensajería.

__RF2: Creación de usuarios:__
* En caso de no estar registrado, el usuario debe poder registrarse rellenando los campos correspondientes.

__RF3: Ver chats disponibles:__
* El usuario podrá visualizar los chats que tenga para realizar una conversación con otro usuario.

__RF4: Ver grupos:__
* El usuario debe ver en qué grupos se encuentra para realizar una conversación.

__RF5: Ver perfil:__
* El usuario podrá ver su perfil. En el debe visualizar su nombre, correo y foto.

__RF6: Cerrar sesión:__
* El usuario podrá cerrar su sesión.

## Diagrama de Caso de Uso

![alt](/Pictures/Diapositiva15.PNG)

## Descripción de Caso de Uso y Mockups

A continuación se muestran los mockups de la aplicación junto al requerimiento funcional que representan.

__RF1: Login a la plataforma__

![alt](/Pictures/Diapositiva16.PNG)

__RF2: Creación de usuarios__

![alt](/Pictures/Diapositiva17.PNG)

__RF3: Ver chats disponibles__

![alt](/Pictures/Diapositiva18.PNG)

__RF4: Ver grupos__

![alt](/Pictures/Diapositiva19.PNG)

__RF5: Ver perfil:__

![alt](/Pictures/Diapositiva20.PNG)