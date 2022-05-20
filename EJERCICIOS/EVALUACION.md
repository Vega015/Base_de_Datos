## Práctica 1.

1. Introducción a base de datos

Objetivo: Identificar el nivel de comprensión de los conceptos de base de datos,
mediante preguntas abiertas.
 
Preguntas:

1. ¿Cuáles son las cinco funciones principales del administrador de bases de datos?
(valor 1.5)
- Asegurar el correcto funcionamiento de la Base de datos.
- Retención, almacenar la informacion de la BD.
- Proporcionar la seguridad de la BD.
- Evitar la perdida de la base de datos.
- Solucionar incidencia que se puedan presentar con la BD


2. Indíque cinco responsabilidades del sistema gestor de bases de datos (valor 1.5)
- Acrualizar, gestionar y configurrar la base de datos
- Dar soporte al equipo de desarrollo, seguridad y redes
- Definir el esquema de diccionarios
- Especificar restricciones de integridad para la seguridad de la BD.
- Garantizar la disponibilidad de la base de datos.


3. En una BD al usuario del sistema se le brindarán recursos para realizar diversas
operaciones sobre estos archivos, tales como: (valor 1.5)
 El usuario puede acceder depediente el nivel de accesibilidad que se le otorgue, puede modificar, consultar, acceder a los datos. También puede utilizar para un post procesamiento particular en los intereses del usuario.


4. ¿Qué es un Sistema de Información? (valor 1.5)
Es un conjunto de elementos orientados  al tratamiento y administracion de los datos e información y listos para su posterior uso con el fin de cubrir una necesidad. Un sistema de Informacion realiza cuatro actividades básicas, entrada, almacenamiento, procesamiento y salida.
## Práctica 2.

2. Diseño de un modelo relacional

Objetivo: Representar desde un modelo entidad relación un problema


Ejercicio:

Tenemos que diseñar una base de datos sobre proveedores y disponemos de la siguiente
información:

Realiza el modelo entidad relación. (valor 6)

Tenemos esta información sobre una cadena editorial:

● La editorial tiene varias sucursales, con su domicilio, teléfono y un código de
sucursal.

● Cada sucursal tiene varios empleados, de los cuales tendremos su nombre,
apellidos, NIF y teléfono. Un empleado trabaja en una única sucursal.

● En cada sucursal se publican varias revistas, de las que almacenaremos su título,
número de registro, periodicidad y tipo.

● Una revista puede ser publicada por varias sucursales.

● La editorial tiene periodistas (que no trabajan en las sucursales) que pueden
escribir artículos para varias revistas. Almacenaremos los mismos datos que para
los empleados, añadiendo su especialidad.

● También es necesario guardar las secciones fijas que tiene cada revista, que
constan de un título y una extensión.

● Para cada revista, almacenaremos información de cada ejemplar, que incluirá la
fecha, número de páginas y el número de ejemplares vendidos.


Sustantivos o entidades 
Sucursales
Empleados
Revistas
Periodistas
Secciones
Ejemplares

Atributos o campos

Domicilio_Surcursal
Telefono_Surcursal
Codigo_Sucursal

Nombre_Empleado
Apellido_Empleado
NIF_Empleado
Telefono_Empleado

Nombre_Periodista
Apellido_Periodista
NIF_Periodista
Telefono_Periodista

Titulo
Extension

Fecha_Revista
Num_Paginas
Num_Ejemplares

![image](https://user-images.githubusercontent.com/34118685/169565209-1f6534db-2c86-4f27-b767-b86fbe132350.png)





