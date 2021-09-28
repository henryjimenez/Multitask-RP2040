# Multitask-RP2040
FreeRTOS over RP2040 processor

El desarrollador de Raspberry Pi y arquitecto de rendimiento Graham Sanderson ha creado un puerto de la rama de multiprocesamiento simétrico (SMP) FreeRTOS recientemente revelada para Raspberry Pi Pico y compatible, lo que permite que el sistema operativo en tiempo real haga uso de ambos núcleos del RP2040.

"Agrega soporte para RP2040 usando Raspberry Pi Pico SDK", escribe Sanderson sobre su solicitud de extracción combinada desde entonces al proyecto FreeRTOS. "FreeRTOS se puede ejecutar en cualquier núcleo. Los semáforos, colas, mutexes y funciones de suspensión del SDK se pueden usar libremente desde / hacia las tareas de FreeRTOS y se pueden usar para interactuar con el código que se ejecuta en el otro núcleo RP2040".

La totalidad de este cambio se encuentra dentro del puerto RP2040, excepto por el nuevo puerto STACK_LIMIT_PADDING define (que solo se usa para la verificación de desbordamiento de pila). Esto se agrega para permitir que un puerto mantenga un estado adicional para la tarea conmutada por debajo de la 'parte superior' normal de la ubicación de la pila. Esto permite que se guarde información adicional en la pila sin interrumpir la capacidad del depurador para analizar el marco de la pila.


Entorno :
cmake: uso cmake-3.21.0-windows-x86_64.msi, la mejor versión> 3.12
GNU Arm Embedded Toolchain: uso 10 2020-q4-major
python: el entorno python3 está bien, python3.7.9
agrego el directorio de archivos bin de las dos herramientas anteriores a la ruta del sistema y también agrego el directorio python dentro de la ruta

El ejemplo ejecutado es:
![image](https://user-images.githubusercontent.com/1444408/135130999-6c9ed4fb-d59a-48a4-89c5-0ad41e111239.png)


