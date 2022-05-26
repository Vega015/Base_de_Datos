## Práctica 4.
### Introducción a SQL
Objetivo: Demostrar la correcta identificación de los conceptos del lenguaje SQL
Ejercicio:

1. Menciona los comandos DMl: (valor .85)
- Los Comandos DML son SELECT, INSERT INTO, UPDATE, DELETE.

2. Menciona 3 tipos de datos que existen: (valor .85)
- Existen 3 tipos de datos los cuales son: numerico, caracter, booleano.


3. ¿Qué diferencia existe entre TRUNCATE y DELETE?(valor .85)
- TRUNCATE es una funcion DDL, sirve para borrar el contenido de toda la tabla, no se puede aplicar si existen FK asociadas.
- DELETE es una funcion DML, sirve para borrar un contenido selectivo en la tabla (con ayuda de la clausula WHERE), se puede aplicar aunque tengan una FK asociada

4. ¿Para qué se utiliza el atributo UNIQUE?(valor .85)
- Es una funcion que permite no repetir los datos dentro de un atributo.

5. ¿Qué diferencia hay entre los tipos de datos VARCHAR y CHAR? (valor .85)
- La principal diferencia es la capacidad de almacenar la memoria, VARCHAR se ajusta al tamaño de la cadena, por otro lado, CHAR es fija, a pesar de que la cadena sea  - mas pequeña que la capacidad de memoria que se le habia ajustado previamente.

6. Defina brevemente el significado de las siglas SQL(valor .85)
- Standarized Query Languaje , es un lenguaje estandarizado para la consulta, organizar  grandes canitidades de datos, que se encuentran estructurados como el modelo entidad relacion.

7. Defina brevemente qué es MySQL WorkBench (valor .85)
- MySQL es un software que sirve como gestor de base de datos, que rirve como interfaz entre la base de datos y los usuarios finales.
## Práctica 5.
### Gestores de base de datos

Objetivo: Categorizar los distintos gestores de base de datos que existen y señalar las
ventajas y desventajas

Evaluación: Conoce los tipos de gestores de base de datos 3 puntos.

Domina sus diferencias de los gestores de base de datos mencionados 3 puntos

Ejercicio:

En un mapa conceptual presenta 3 gestores de bases de datos, sus características
principales, las ventajas y desventajas. (valor 6)

![image](https://user-images.githubusercontent.com/91554777/170415427-e2b7321b-a97f-43b0-ac24-6e506c307e6b.png)

## Práctica 6.
### Herramienta en línea y ejercicio necesarios para realizar las prácticas

Creación de base de datos.

Objetivo: Demostrar mediante la creación de una base de datos el uso y la aplicación de
las funciones

Ejercicio: Creación de la base de datos (valor 18 puntos)

Tienda de informática

![image](https://user-images.githubusercontent.com/91554777/170415101-717bca19-3644-46a9-8a57-8d5940c5d283.png)




Modelo entidad/relación




Base de datos para MySQL

    CREATE DATABASE informatica;
    USE informatica;

    CREATE TABLE fabricantes(
      id_fabricante VARCHAR(50) UNIQUE PRIMARY KEY,
        nombre_fabricante VARCHAR(50)
    );

    INSERT INTO fabricantes VALUES ('SEA01','SEAGATE');
    INSERT INTO fabricantes VALUES ('CRU01','CRUCIAL');
    INSERT INTO fabricantes VALUES ('SAM01','SAMNSUNG');
    INSERT INTO fabricantes VALUES ('GIG01','GIGABYTE');
    INSERT INTO fabricantes VALUES ('ASU01','ASUS');
    INSERT INTO fabricantes VALUES ('LEN01','LENOVO');
    INSERT INTO fabricantes VALUES ('HP01','HP');

    CREATE TABLE productos (
      id_producto VARCHAR(50) UNIQUE PRIMARY KEY,
        nombre_producto VARCHAR(50) NOT NULL,
        precio FLOAT NOT NULL,
        id_fabricante1 VARCHAR(50),
        FOREIGN KEY (id_fabricante1) REFERENCES fabricantes(id_fabricante)
      );

     INSERT INTO productos VALUES ('DD-23','Disco duro SATA3 1TB',86.99,'SEA01');
     INSERT INTO productos VALUES ('MM-34','Memoria RAM DDR4 8GB',120,'CRU01');
     INSERT INTO productos VALUES ('DD-98','Disco SSD 1 TB',150.99,'SAM01');
     INSERT INTO productos VALUES ('MM-98','GeoForce GTX 1050Ti',185,'GIG01');
     INSERT INTO productos VALUES ('MM-23','GeoForce GTX 1080 Xtreme',755,'CRU01');
     INSERT INTO productos VALUES ('MT-12','Monitor 24 LED Full HD',202,'ASU01');
     INSERT INTO productos VALUES ('MT-08','Monitor 27 LED Full HD',245.99,'ASU01');
     INSERT INTO productos VALUES ('LP-19','Portátil Yoga 520',559,'LEN01');
     INSERT INTO productos VALUES ('LP-11','Portátil Ideapd 320',444,'LEN01');
     INSERT INTO productos VALUES ('IM-56','Impresora HP Deskjet 3720',59.99,'HP01');
     INSERT INTO productos VALUES ('IP-54','Impresora HP Laserjet Pro M26nw',180,'HP01');
 
