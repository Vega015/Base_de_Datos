
## Práctica 4
### Data warehouse

Objetivo: Demostrar la identificación de los elementos que componen data warehouse y
su esquema

Ejercicio:

1. ¿Qué es un DataWarehouse?(valor 2)
- Es un sistema que agrega y combina informacion de diferentes fuentes en un almacen de datos único y centralizado, sirve para respaldar el analisis empresarial, la mineria de datos, etc.

2. Realiza un diseño del modelo en estrella (valor 2)
- Un esquema estrella es un tipo de esquema de base de datos relacional que consta de una sola tabla de hechos central rodeada de tablas de dimensiones.

![image](https://user-images.githubusercontent.com/34118685/171877827-de6dee4d-05b7-441f-a915-15bb435c702e.png)


3. Realiza un diseño del modelo copo de nieve (valor 2)
- El esquema de copo de nieve consta de una tabla de hechos que está conectada a muchas tablas de dimensiones, que pueden estar conectadas a otras tablas de dimensiones a través de una relación de muchos a uno.
- 
![image](https://user-images.githubusercontent.com/34118685/171881089-d65dc212-c826-40d2-a2e9-a21eaa82374f.png)


## Práctica 7
### Funciones en SQL
Objetivo: Demostrar el uso y aplicación en una base de datos para mejorar la gestión

Ejercicio:

1. Calcula el número total de productos que hay en la tabla productos. (valor 4.5)
 ![image](https://user-images.githubusercontent.com/34118685/171875334-2844bd7e-1796-4cf7-a817-0c2703d8f06a.png)



2. Muestra el número total de productos que tiene cada uno de los fabricantes. El listado
también debe incluir los fabricantes que no tienen ningún producto. El resultado
mostrará dos columnas, una con el nombre del fabricante y otra con el número de
productos que tiene. Ordene el resultado descendentemente por el número de
productos. (valor 4.5)

![image](https://user-images.githubusercontent.com/34118685/171875449-5a526afa-ede2-4104-80de-a447521c26b9.png)


3. Muestra el precio máximo, precio mínimo y precio medio de los productos de cada
uno de los fabricantes. El resultado mostrará el nombre del fabricante junto con los
datos que se solicitan. (valor 4.5)
![image](https://user-images.githubusercontent.com/34118685/171875538-e944cea0-ccee-4a05-8bc1-5cd58b8a4b07.png)


4. Muestra el nombre de cada fabricante, junto con el precio máximo, precio mínimo,
precio medio y el número total de productos de los fabricantes que tienen un precio
medio superior a 200€. Es necesario mostrar el nombre del fabricante. (valor 4.5)
 ![image](https://user-images.githubusercontent.com/34118685/171875654-36cb2cb5-9206-40ba-8d9d-d6d580b2955d.png)

Los ejercicios se encuentran en este link : https://www.db-fiddle.com/f/c63xUmSw1K8ndYKNyhSRmp/3

## Práctica 8.
### Disparadores (Triggers)

Objetivo: Demostrar las operaciones que se realizan en una base de datos.

Ejercicio: Crea una base de datos llamada test que contenga una tabla llamada
alumnos con las siguientes columnas. (valor 18)

Evaluación:

Creación de la base de datos : 9 puntos.

Creación de los Disparadores(Triggers): 9 puntos.

Tabla alumnos:

● id (entero sin signo)

● nombre (cadena de caracteres)

● apellido1 (cadena de caracteres)

● apellido2 (cadena de caracteres)

● nota (número real)

Una vez creada la tabla escriba dos triggers con las siguientes características:

● Trigger 1: trigger_check_nota_before_insert

  o Se ejecuta sobre la tabla alumnos.
  
  o Se ejecuta antes de una operación de inserción.
  
  o Si el nuevo valor de la nota que se quiere insertar es negativo, se guarda
  como 0.
  
  o Si el nuevo valor de la nota que se quiere insertar es mayor que 10, se
  guarda como 10.

● Trigger2 : trigger_check_nota_before_update
  o Se ejecuta sobre la tabla alumnos.
  
  o Se ejecuta antes de una operación de actualización.
  
  o Si el nuevo valor de la nota que se quiere actualizar es negativo, se guarda
  como 0.
  
  o Si el nuevo valor de la nota que se quiere actualizar es mayor que 10, se
  guarda como 10.
  
Una vez creados los triggers escribe varias sentencias de inserción y actualización
sobre la tabla alumnos y verifica que los triggers se están ejecutando
correctamente.

Los ejercicios se encuentran en este 
https://www.db-fiddle.com/f/v96s3LYoJY2gz68vhEvPHD/1
