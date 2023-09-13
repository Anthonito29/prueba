# Clasificación de objetos a través del color.
Este ejemplo muestra como utilizar un conjunto de datos de un sensor para crear un modelo de aprendizaje profundo que clasifique diferentes objetos.
Se ha creado diferentes carpetas para cada placa ya que algunas librerías difieren entre placas.
## Características.
El ejemplo usa el sensor APDS9960 para capturar el color de diferentes objetos. Esto como una demostración de cómo podríamos diferenciar objetos de diferentes colores o materiales.
Esta idea se basa del ejemplo “Color Clasify”. Vemos una oportunidad de usar el TinyML para la clasificación de objetos.

Opciones como la programación convencional resulta mas compleja para sistemas que se pueden ver afectados por factores externos, asi pues factores como la iluminación podrían dar resultados diferentes en el color capturado durante transcurso del día.
Debido a esto se decidió crear un modelo de machine learning que busque reconocer colores de un objeto a travez de un entrenamiento con una base de datos de colores que abarque todos esos cambios posibles.
Para desarrollar esta idea tomamos 4 objetos de diferentes colores y los pusimos en un lugar con una iluminación variable y controlada.
Los objetos son rollos de cinta de diferentes colores (Rojo, Azul, Amarillo, Verde). Se ha creado una base de datos para cada placa debido a que la placa Arduino Nano 33 Ble ya incorpora este sensor en su misma PCB y las demás placas usan un módulo separado de este sensor.

## Requisitos.
Para desarrollar este ejemplo debemos tener instalado algunas herramientas como son:
-	Librería para la tarjeta Arduino Nano 33 Ble Sense.
-	Librería para la tarjeta Esp32.
-	Librería para la tarjeta Raspberry Pi Pico.
-	Coolterm.
-	Entorno de Google Colaboratory.
### Librería para la tarjeta Arduino Nano 33 Ble Sense.
Para realizar la instalación debemos abrir el IDE de Arduino y posteriormente remitirnos al gestor de tarjetas de este modo:
- Herramientas.
   - Placa.
	   - Gestor de tarjetas.
![Gestor1]( https://github.com/udenarML/prueba/blob/main/imagenes/gestor1.png)

Ya en el gestor de placas debemos buscar la librería como “Arduino Mbed OS Nano Boards”

![gestor]( https://github.com/udenarML/prueba/blob/main/imagenes/gestor.PNG)

Para corroborar que la placa se instalo correctamente procedemos a cargar un programa para un parpadeo de un led.
Primero debemos escoger la placa correspondiente de esta manera:

![escoger placa]( https://github.com/udenarML/prueba/blob/main/imagenes/escoger%20placa.png)

Luego de esto debemos escoger el ejemplo asi:

![blink]( https://github.com/udenarML/prueba/blob/main/imagenes/blink.png)

Finalmente cargamos el ejemplo. Para esto debemos conectar la placa y presionar dos veces el botón de reset para que la placa entre en modo de programación.

Cuando la placa empieza a iluminar el led de color naranja procedemos a escoger el puerto que se le ha asignado a la placa

** Nota ** este puerto cambio según el modo en que este la placa.

![puerto]( https://github.com/udenarML/prueba/blob/main/imagenes/puerto.png)

Por último, cargamos el ejemplo y debemos observar que el LED de la placa empezara a parpadear.


