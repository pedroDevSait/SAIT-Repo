# Capacitación SAIT
## Desarrollo
### Pedro
Un poco de documentación sobre mi capacitación en Microsistemas San Luis.

## Fecha: 1-SEP-2022

Tuve una sesión de capacitación en la cual el Ing. Ignacio me explicó como 
se agrega funcionalidad a SAIT mediante el método autorun, para ello:

1. Primero debemos ubicarnos en la carpeta DEMO de SAIT ya sea por la consola de comandos
de Visual FoxPro o  mediante el entorno gráfico del mismo y crear un programa nuevo.
2. En este nuevo archivo vamos a añadir toda la funcionalidad que el cliente solicite,
sean botones, ventanas, campos, etiquetas, etc.

3. Supongamos que nuestro cliente es "Bimbo", para agregar nuevo código a SAIT es necesario crear una funcion que
arranque toda la nueva funcionlidad por ejemplo, initBimboApp. Dentro de initBimboApp se llamarán
todas las funciones y métodos nuevos.

4. Una vez se tenga todo lo nuevo que se quiere agregar se compila el programa.

5. Ahora, ubicar el archivo autorun.prg, si no existe crearlo. Dentro de él se llama a la función
init del nuevo modulo, continuando con el ejemplo anterior sería:

```
  do initBimboApp in Bimbo
```

Donde:
- Do: Es un comando de VFP el cual ejecuta un programa o procedimiento.
- initBimboApp: Es la función que se definió para arrancar dicho modulo
- in: Le indica a VFP donde está la función que se va a ejecutar
- Bimbo: Es el archivo donde se encuetra la funció o procedimiento que se va a ejecutar

6. Si todo a salido bien, una vez que compiles los programas y ejecutes SAIT deberías ver la nueva funcionaldiad en marcha, si tenías abierto SAIT mientras modificabas o compilabas la nueva funcionalidad cierra el sistea y vuelve a abrilo.

#### Nos quedamos en la creación de objetos para pasar más de un parametro entre formuarios.

## Fecha: 2-SEP-2022

Tuve una sesión de capación con Ricardo en la cuál me mostró como trabajó en un desarrollo especial, también cómo es que se trabaja con la base de datos.

Estas son algunos de los temas que se tomaron:

1. Usando las librerías de SAIT pueden facilitar operaciones como conexión con bases de datos.

2. Me mostró como se hacia la apertura de conexión y que normalmente se usan cursores o temporales para hacer consultas a la base de datos.

3. Me enseñó como funciona el ciclo SCAN de VFP, también la palabra reservada LOCATE FOR, la palabra reservada SEEK.

4. Como agregar métodos a un formulario.

5. Siempre hay que validar lo que se quiere insertar en la base de datos, para evitar redundacia de información.

6. La configuración por defecto que se usa en el control Grid 

7. Como se usa el operador diferente en VFP "<>"

## Fecha: 7-SEP-2022
Tuve sesión de capacitación con Ignacio, estos son algunos de los temas que se trataron.
1. Como agregar atajos de teclado mediante código de VFP.
  
  
    Syntax:
    ``` 
      thisform.btn_delete.Caption = "\<Eliminar" 
    ```


    En este caso la letra E tendrá un subrayado como el siguiente.

  
    ![Ejemplo de subrayado](https://github.com/pedrosait/SAIT-Repo/blob/main/img/btn_eliminar.png)
  
2. DATASESSION ID es una propiedad la cual identifica las sesiones de datos privadas, ejemplo si existe una sesión abierta con el ID 1, si se abre una sesión privada su ID será 2.

3. El comando SET tiene varios usos principalmente se usa para establecer la configuración interna de VFP.


## Fecha: 8-SEP-2022
Tuve sesión con Ricardo.

1. Para dar saltos de lineas en VFP se usa 
  
  ```
    chr(10)
  ```

2. En VFP se recomienda abrir una sola instancia de una tabla de la Base de Datos, si es necesario manipular una tabla desde otra forma al mismo tiempo es mejor abrir una copia en un cursor.

3. SCAN por defecto te posiciona en el primer registro de la tabla. Si no se establece una condición recorrerá todos los registros.

4. El diseñador de reportes acepta funciones en los campos del reporte.

5. Para que un procedimiento reciba parametros se tiene que indicar en el programa con lparameter.

6. Es necesario vereficar que no existe una conexión abierta a la base de datos.

7. SEEK te posiciona en el registro que se parece al que se establece en el método.

8. Siempre cerrar todas las conexiones con la base de datos.
