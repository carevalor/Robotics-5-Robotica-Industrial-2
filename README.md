# Robotics-5-Robotica-Industrial-2

##Tarea 1

Para la tarea uno se utilizaron los mismos puntos utilizados para el laboratorio anterior. Por lo tanto las rutinas de path en rapid también tienen la misma configuración.

Primero se realiza la creación de las entradas digitales, que corresponden a dos botones cableados con la unidad de control. Estas entradas conrresponden a la entrada DI_01 y DI_02. 


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


