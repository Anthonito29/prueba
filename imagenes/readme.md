# 1)	Captura de datos.
Debemos cargar el archivo “Capture_color.ino” para capturar los datos que recibimos del sensor APDS9960.
Con el programa cargado procedemos a realizar pruebas acercando algún objeto. Debe recibir valores parecidos a estos:

IMAGEN DE CAPTURA DATOS SERIAL.

Para realizar de manera mas adecuada el experimento hemos puesto los objetos a censar debajo de una iluminación LED la cual podemos variar su intensidad con el fin de simular cambios de iluminación.

DIAGRAMA MONTAJE.
FOTO MONTAJE.

Con el montaje realizado es hora de crear la base de datos. Para esto usamos el programa llamado “COOLTERM” que nos permite la comunicación de la placa de desarrollo con la PC, además automatiza el grabado de los datos.

IMAGEN COOLTERM.

En primer lugar debemos configurar el puerto y la velocidad de trasmisión. Para esto debemos seguir los siguientes pasos.

   - Connection.
     - Options.            

Cuando demos clic aparecerá una ventana nueva.

IMAGEN CONFIGURAR PLACA COOL TERM

Aquí escogemos el puerto al que le corresponde a la placa, además de la velocidad en baudios.
Luego de esto le damos en OK y la placa estará configurada.
Antes de nada, es necesario crear una carpeta en donde se guardarán los archivos.
En el programa coolterm debemos seguir unos pasos para crear el archivo donde se almacenarán los datos.

*. Connection
            -capture text/ binary file
                        -Start

Cuando demos clic en Start aparecerá una ventana en donde podremos elegir en donde guardar el archivo y además podemos cambiar el nombre y su extensión.
Asi pues para crear el archivo nos dirigimos a la carpeta que creamos y luego cambiamos el nombre del archivo por ejemplo “Amarillo.csv” y antes de guardar debemos cambiar el tipo de archivo, para esto debemos dar clic en la pestaña de tipo y elegir la opción de “All files”

IMAGEN CREACION ARCHIVO COOL


El objeto debe estar colocado frente al sensor antes de conectar la placa.

Ahora procedemos a conectar la placa con el botón llamado connect que tiene un icono de un puerto USB.

**Nota:** 
es recomendable antes de conectar la placa. Resetearla por medio de el botón de reset o desconectando y conectándola de nuevo.
Con todo listo procedemos a conectar la placa y esta enseguida empieza a enviar datos, ahí es cuando por medio de un potenciómetro modificamos la intensidad de la iluminación de una manera suave para que se capturen datos de color en diferentes cantidades de iluminación.
El proceso de captura dura unos pocos minutos, este proceso es para la captura de un objeto asi que debemos repetirlo para los demás objetos.
Para terminar la grabación debemos dirigirnos a:

Connection—capture/binary—stop.

Para verificar si el archivo contiene los datos debemos abrirlo con algún programa como Excel o bloc de notas.

IMAGEN ARCHIVO ABIERTO.

El archivo debe contener el encabezado R, G, B. si este no aparece debemos ponerlo manualmente.

# 2)	Entrenamiento.
Hemos creado un cuaderno de Google colab con la programación en Python del entrenamiento del modelo y su conversión usando TensorFlow y TensorFlow lite.
En este cuaderno esta la explicación detallada del código usado.
Para el desarrollo de este cuaderno deberá de copiarlo en un archivo nuevo creado en su propio entorno.

