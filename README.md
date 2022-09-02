# Capacitación SAIT
Un poco de documentación sobre mi capacitación en Microsistemas San Luis.

## Fecha: 1-SEP-2022
### Pedro, Desarrollo

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

```do initBimboApp in Bimbo```

Donde:
- Do: Es un comando de VFP el cual ejecuta un programa o procedimiento.
- initBimboApp: Es la función que se definió para arrancar dicho modulo
- in: Le indica a VFP donde está la función que se va a ejecutar
- Bimbo: Es el archivo donde se encuetra la funció o procedimiento que se va a ejecutar

6. Si todoa ha salido bien, una vez que compiles los programas y ejecutes SAIT deberías ver la nueva funcionaldiad en marcha, si tenías abierto SAIT mientras modificabas o compilabas la nueva funcionalidad cierra el sistea y vuelve a abrilo.
