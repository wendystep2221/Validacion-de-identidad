# Validación de identidad
El objetivo de este repositorio es generar dos estrategias de validación de identidad para una persona.

Para la validación, usando la cámara y micrófono del dispositivo en uso se pedirá a la persona responder ciertas preguntas acerca de su identidad, adicional a ello se pedirá una fotografía del documento original de identidad de la persona donde se encuentre una fotografía.

## Reconocimiento facial
Para el reconocimiento facial se requieren dos inputs: Foto de un documento de identidad donde se vea el rostro, video de su rostro tomado en el momento de hacer la validación.
[Imagen ejemplo]

Durante la toma del video se pide a la responder ciertas preguntas frente a la camára, del video resultante se extraen 3 frames los cuales serán comparados con la fotografia de rostro reconocida en el documento de identidad se valida la coincidencia en las imágenes.

## Estres de voz

Con la intención de determinar cuando una persona podría estar mintiendo se analiza el audio recogido en el video inicial donde la persona responde preguntas acerca de su identidad, (Ej. se pide decir viendo a la camara yo soy.. con .... años de edad, mi fecha de nacimiento es ..... vivo en la ciudad de...), este audio será sometido a una prueba de estres de voz donde se determina el estres en la voz al responder las preguntas. Con eso se puede asumir que una voz estresada o en otras palabras nerviosa  puede relacionarse con el acto de mentir.

# Procesamiento y modelamiento de datos
## Datos de video
###  Pre-procesamiento de imagen
El proyecto tendrá como objetivo la identificacion de rostro. 
Para esto se usará una red pre-entrenada ([dlib face recognition](http://dlib.net/)) que es capaz de reconocer el area del rostro posando de manera frontal.


## Propuesta de pre-procesamiento del dato

El objetivo es conectar el programa a la camará de algún dispositivo a disposición del usuario:

1. Del video se extraerán imagenes

2. De cada imagen se identificará el rostro eliminando información no util, por ejemplo, el fondo, las orejas, cabello y cuello.
3. Se pone en escala de grises
4. Se redimensionan las imagenes
