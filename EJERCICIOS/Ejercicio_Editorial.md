
![image](https://user-images.githubusercontent.com/34118685/169565209-1f6534db-2c86-4f27-b767-b86fbe132350.png)
https://www.db-fiddle.com/f/adHufv5Q7G8s5gPpeZCt2S/0

    CREATE DATABASE editorial;
    USE editorial;

    CREATE TABLE sucursales(
      codigo_sucursal INT UNSIGNED PRIMARY KEY,
        domicilio_sucursal VARCHAR(100) NOT NULL,
        telefono_sucursal VARCHAR(50) NOT NULL
      );

    CREATE TABLE revistas(
      num_registro INT UNSIGNED PRIMARY KEY,
        titulo_revista VARCHAR(50) NOT NULL,
        periodicidad VARCHAR(50) NOT NULL,
        tipo VARCHAR(50) NOT NULL
      );

    CREATE TABLE periodistas(
      nif_periodista INT UNSIGNED PRIMARY KEY,
        nombre_periodista VARCHAR(50) NOT NULL,
        apellido_periodista VARCHAR(50) NOT NULL,
        telefono_perioditsa VARCHAR(50) NOT NULL
      );

    CREATE TABLE empleados(
      nif_empleado INT UNSIGNED PRIMARY KEY,
        nombre_empleado VARCHAR(50) NOT NULL,
        apellido_empleado VARCHAR(50) NOT NULL,
        telefono_empleado VARCHAR(50) NOT NULL,
        codigo_sucursal2 INT UNSIGNED NOT NULL,
        FOREIGN KEY (codigo_sucursal2) REFERENCES sucursales(codigo_sucursal)
      );

    CREATE TABLE secciones(
      id_seccion INT UNSIGNED PRIMARY KEY,
        titulo VARCHAR(50) NOT NULL,
        extension VARCHAR(50),
        num_registro3 INT UNSIGNED NOT NULL,
        FOREIGN KEY (num_registro3) REFERENCES revistas(num_registro)
      );

    CREATE TABLE ejemplares(
      id_ejemplar INT UNSIGNED PRIMARY KEY,
        num_ejemplar INT UNSIGNED NOT NULL,
        num_pagina INT UNSIGNED,
        fecha_ejemplar DATE NOT NULL,
        num_registro4 INT UNSIGNED NOT NULL,
        FOREIGN KEY (num_registro4) REFERENCES revistas(num_registro)
      );

    CREATE TABLE suc_rev(
      codigo_sucursal1 INT UNSIGNED NOT NULL,
        num_registro1 INT UNSIGNED NOT NULL,
        FOREIGN KEY (codigo_sucursal1) REFERENCES sucursales(codigo_sucursal),
        FOREIGN KEY (num_registro1) REFERENCES revistas(num_registro)
      );

    CREATE TABLE rev_per(
      num_registro2 INT UNSIGNED NOT NULL,
        nif_periodista1 INT UNSIGNED NOT NULL,
        FOREIGN KEY (num_registro2) REFERENCES revistas(num_registro),
        FOREIGN KEY (nif_periodista1) REFERENCES periodistas(nif_periodista)
      );
