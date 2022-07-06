# Robotics-5-Robotica-Industrial-2

## Tarea 1

Para la tarea uno se utilizaron los mismos puntos utilizados para el laboratorio anterior. Por lo tanto las rutinas de path en rapid también tienen la misma configuración.

Primero se realiza la creación de las entradas digitales, que corresponden a dos botones cableados con la unidad de control. Estas entradas conrresponden a la entrada DI_01 y DI_02. La creación de las entradas se verifican en la siguiente imagen, en la imágen también se muestra el panel de simulación con el nombre de las entradas digitales creadas. 

[![Entradas.jpg](https://i.postimg.cc/FsRWHqB6/Entradas.jpg)](https://postimg.cc/JtfcTTm3)

Es importante también crear las entradas en el robot y realizar las conexiones de los pulsadores con el modulo de entradas.


El código realizado en rapid para la lectura de las entradas se realiza dentro del main, esto para que el controlador lea si hay cambio en la entrada digital.
Nótese que las entradas están inicialmente en cero, y los pulsadores son normalmente abiertos. De esta forma, cuando se presione el pulsador el estado de la variable de entrada digital pasará a ser 1, por lo que el condicional será verdadero y se procederá a ejecutar el procedimiento declarado como Path_10 o Path_20 según corresponda, teniendo en cuenta que cada uno de estos procedimientos corresponde a las dos trayectorias previamente generadas.

``` RAPID
    PROC main()
        IF DI_01=1 THEN
            Path_10;
        ENDIF
        IF DI_02=1 THEN
            Path_20;
        ENDIF
    ENDPROC
```
## Resultados

Los resultados se verificaron en simulación, también se cargó el código de rapid para observar el desarrollo de la tarea con el robot. El resultado se muestra en el siguiente video:

https://youtu.be/7uX0r3Xu_g4
