# Estados

#### Revisar Animator controller unity character 
Octubre diseñaremos el producto, tanto como el proyecto 
se acaba octubre tendremos seis proyectos elección popular, interactiva remota, usaremos micro controladores, preguntar a las personas algo se abre opciones y representar las respuestas, debe tener sentido, primera parte vamos a investigar y conceptualización 
lucid dreams
Buscar profundización del tema 
Preguntas polemicas, metodo, crear ramas de investigación, marco conceptual 
Rube Goldberg 

## ¿Cómo crearse una cuenta en arduino cloud?

1. Abrir en el navegador https://cloud.arduino.cc/.
2. Descargar la app móvil en tu teléfono y convertirlo en un dashboard para que pueda aparecer online en arduino cloud.
3. Presionar la opción Get started for free.
4. Luego te pedirá registrarte con github, Google, Facebook o Apple.

## Conexión de un led a Arduino uno r4 wifi
Para conectar a un led que será controlado con un dimmer debemos conectarlo a un pin DWM los podemos identificar ya que cuentan con una especie de guión con curvas. Este tipo de pin a diferencia de los demás permite la variación de energía, en cambio los otros solo permiten o bloquean su salida.

 ![ConexionLed](https://github.com/user-attachments/assets/fc270553-770f-4d32-a951-1f9d040a719c)

 ## ¿Cómo conectar un arduino y hacer un dimmed con un led?
 
1. Luego de iniciar sesión podrás comenzar a conectar tu arduino, que debes conectar al puerto USB.
2. Luego deberás ir a Things, donde debes conectar un device, seleccionando en este caso una placa arduino y anclarlo a una red wifi mediante Network .
2. Si miras a la parte izquierda de la columna donde aparece el device encontrarás un Add, el cual te permitirá añadir una variable.
4. En este caso añadiremos la variable Integer Number y le daremos el nombre de ledBrillo.
5. En la parte superior derecha aparecerá la opción de ir a Scketch en donde deberás añadir lo siguiente

6. ```ino
       //luego del #include agregar

       const int ledPin= 11; // Define el pin en el cual estará conectado el Led

       // en el void setup, luego de ArduinoCloud.begin

       pinMode(ledPin, OUTPUT); // define que el pin establecido en el inicio sera una salida

       // luego de void onLedBrilloChange

       analogWrite(ledPin, ledBrillo); // define que lo que será escrito será la variación del brillo en el led
```
6. cuando esto esté listo nos aseguraremos de que el código este correcto (Esto se demora un poco), si no es correcta debemos fijarnos que el void no haya creado otra variable.
7. Luego de editar el código iremos al inicio, para ir a la opción Dashboard, donde crearemos un slider y lo ligaremos a la variable que creamos anteriormente (ledBrillo).
8. Finalmente cargaremos nuestro código en el arduino y usaremos el slicer para ver los resultados.

###CODIGO FINAL 
```ino
       /* 
       Sketch generated by the Arduino IoT Cloud Thing "Untitled"
       https://create.arduino.cc/cloud/things/41b4b59f-6976-4a62-ab7b-8e173c8f3081 

       Arduino IoT Cloud Variables description

       The following variables are automatically generated and updated when changes are made to the Thing

       int ledBrillo;

       Variables which are marked as READ/WRITE in the Cloud Thing will also have functions
       which are called when their values are changed from the Dashboard.
       These functions are generated with the Thing and added at the end of this sketch.
       */

       #include "thingProperties.h"
       const int ledPin= 11;

       void setup() {
       // Initialize serial and wait for port to open:
       Serial.begin(9600);
       // This delay gives the chance to wait for a Serial Monitor without blocking if none is found
       delay(1500); 

       // Defined in thingProperties.h
       initProperties();

       // Connect to Arduino IoT Cloud
       ArduinoCloud.begin(ArduinoIoTPreferredConnection);

       // LedPin es un output
       pinMode(ledPin, OUTPUT);
  
       /*
       The following function allows you to obtain more information
       related to the state of network and IoT Cloud connection and errors
       the higher number the more granular information you’ll get.
       The default is 0 (only errors).
       Maximum is 4
       */
       setDebugMessageLevel(2);
       ArduinoCloud.printDebugInfo();
       }

       void loop() {
       ArduinoCloud.update();
       // Your code here 
  
  
       }

       /*
       Since LedBrillo is READ_WRITE variable, onLedBrilloChange() is
       executed every time a new value is received from IoT Cloud.
       */
       void onLedBrilloChange()  {
       // Add your code here to act upon LedBrillo change
       // aca escribe osea muestra el valor que este llegando del slider que esta conectado a int ledBrillo;  y se lo aplica al led
       analogWrite(ledPin, ledBrillo);
       }
```
## Observaciones 

- En un principio al querer conectar el arduino como device, existieron dificultades para que el cloud lograra reconocerlo, dedujimos que podía ser el navegador y nos dimos cuenta de que el cable que utilizaramos igual influia. Sirvió refrescar la página y luego era mas facíl conectarlo.
- En mi caso al habilitar el celular como Dashboard no me permitía usar algún otro dashboard en la nube, y lo notamos luego de deshabilitarlo y solo dejar los de la nube.
- Para que el arduino aparezca online  debe tener cargado un código funcional.
- Tratar de cambiar lo menos posible las configuraciones predeterminadas.

 *Github campus program*
Nos puede dar acceso a más recursos de github si ingresamos como estudiantes

## *¿Cómo llegar a controlar un proyecto con la nube?*

- Buscar bien tutoriales que hagan y detallen cosas que queremos conseguir
- Ver todo y leer todo (me ayudará a entender con que estoy trabajando)
- Buscar las variables que nos pueden servir dentro de los códigos y agregarlas en la nube.
- Fijarse en que pines conecta cada cosa.
- Nombrar cada cosa para organizarse.
- Tomar primero las decisiones.
- Tener en cuenta los estados de los elementos.
- Animator controller unity Character.
- ¿Funciona o no funciona?

## Proyecto de titulo Andres

Construccionismo: Paradigma de la educación que plantea el aprender haciendo.

. Toma de decisiones

. Aprender como funcionan las cosas

. Interactuar con el entorno

. Manipular el entorno

. Aprender con las manos

desarrollo de un sistema planetario físico en un sistema digital

naves que permitan recorrer el universo

Gamificación: Formas de incentivar, no necesariamente de manera material

Tipos de jugadores: Killers, Sociales, Exploradores y Creadores.

¿Cómo quería que se sintiera la actividad?

*Distintas etapas*

1 explorar -> 2 crear -> 3 ganar -> 4 social coop

que tecnologías sirven?

Comunicar al usuario o a la aplicación que piezas se ensamblan

 parte importante del proceso es diseñar partes aparte, que no estan definidas desde un principio.

 placa pcb
opinion 

