
https://www.db-fiddle.com/f/26N3vCMEwN58VKx14Sh7nb/0

    CREATE DATABASE editorial;
    USE editorial;

    CREATE TABLE sucursales(
      codigo_sucursal VARCHAR(50) PRIMARY KEY,
        domicilio_sucursal VARCHAR(100) NOT NULL,
        telefono_sucursal VARCHAR(50) NOT NULL
      );
    -- Insertas datos a surcursal
    INSERT INTO sucursales VALUES ('suc-01','Tenayuca 15, Colonia Porvenir CDMX	Migual Hidalgo','5573485948');	
    INSERT INTO sucursales VALUES ('suc-02','Ahuehuetes 24, Colona Reynosa GUADALAJARA	Zaragoza','3395847649');
    INSERT INTO sucursales VALUES ('suc-03','San Juan 12, Colonia Electricistas TOLUCA	Toluca','7293840947');
    INSERT INTO sucursales VALUES ('suc-04','Manuel Buendía 948, Colonia Reforma MONTERREY	Revolucion','8293459375');
    INSERT INTO sucursales VALUES ('suc-05','Petroleos 12, Colonia Alabama QUERETARO Júarez','7394850983');
    INSERT INTO sucursales VALUES ('suc-06','Petén 1209 Roma Norte CDMX	GAM','5587394785');
    INSERT INTO sucursales VALUES ('suc-07','Tlahuac 10, Colonia Reyes PUEBLA Oriental','4593849058');
    INSERT INTO sucursales VALUES ('suc-08','Anaxagoras 15, Polanco CANCUN	Cancun','3384909859');
    INSERT INTO sucursales VALUES ('suc-09','Miguel Hidalgo 98, Colonia Angustura GUADALAJARA Zapopan', '3338930403');
    INSERT INTO sucursales VALUES ('suc-10','Cervantes 56, Colonia Juárez TIJUANA Hidalgo','2288473845');

    CREATE TABLE revistas(
      num_registro VARCHAR(50) PRIMARY KEY,
        titulo_revista VARCHAR(50) NOT NULL,
        tipo VARCHAR(50) NOT NULL,
        periodicidad VARCHAR(50) NOT NULL
      );

    -- Insertas datos a revistas
    INSERT INTO revistas VALUES ('REV_098','POLITICA HOY','POLITICA','SEMANAL');
    INSERT INTO revistas VALUES ('REV_099','EMOCION DEPORTIVA','DEPORTIVA','QUINCENAL');
    INSERT INTO revistas VALUES ('REV_100','MUNDO ROSA','ESPECTACULOS','SEMANAL');
    INSERT INTO revistas VALUES ('REV_101','VIDEOGAMER','VIDEOJUEGOS','MENSUAL');
    INSERT INTO revistas VALUES ('REV_102','CINE HOY','CINE','SEMANAL');
    INSERT INTO revistas VALUES ('REV_103','TODO EN CULTURA','CULTURAL','MENSUAL');

    CREATE TABLE periodistas(
      nif_periodista VARCHAR(50) PRIMARY KEY,
        nombre_periodista VARCHAR(50) NOT NULL,
        apellido_periodista VARCHAR(50) NOT NULL,
        telefono_perioditsa VARCHAR(50) NOT NULL,
        espelcialidad VARCHAR(50) NOT NULL
      );

     -- Insertar datos periodistas
    INSERT INTO periodistas VALUES ('PER_01','KARLA', 'JUAREZ PEREZ','5534563748','DEPORTES');
    INSERT INTO periodistas VALUES ('PER_02','BEATRIZ','LOPEZ	ANGELES','7289467349','POLITICA');
    INSERT INTO periodistas VALUES ('PER_03','TITO','MARQUEZ	GALINDO','8203978465','ESPECTACULOS');
    INSERT INTO periodistas VALUES ('PER_04','ISABEL','SUAREZ	JIMENEZ','8263748987','VIDEOJUEGOS');
    INSERT INTO periodistas VALUES ('PER_05','PABLO','FERNANDEZ	DUARTE','5523784938','CINE');
    INSERT INTO periodistas VALUES ('PER_06','SERGIO','INFANTE	MORALES','7238946574','CINE');
    INSERT INTO periodistas VALUES ('PER_07','CARLOS','GUIZAR	CISNEROS','3398475840','CULTURA');
    INSERT INTO periodistas VALUES ('PER_08','JUAN','SALAS	MACIAS','5682394848','DEPORTES');
    INSERT INTO periodistas VALUES ('PER_09','PEDRO','RICO	GARAY','5548738495','POLITICA');
    INSERT INTO periodistas VALUES ('PER_10','ANGEL','HERASFUENTES','8236475894','VIDEOJUEGOS');
    INSERT INTO periodistas VALUES ('PER_11','CESAR','SAN PEDRO	RODRIGUEZ','4585968495','CINE');
    INSERT INTO periodistas VALUES ('PER_12','MAGDA','LIRA	SANCHEZ','7683749504','POLITICA');

    CREATE TABLE empleados(
        nif_empleado VARCHAR(50) PRIMARY KEY,
        nombre_empleado VARCHAR(50) NOT NULL,
        apellido_empleado VARCHAR(50) NOT NULL,
        telefono_empleado VARCHAR(50) ,
        codigo_sucursal2 VARCHAR(50) NOT NULL,
        FOREIGN KEY (codigo_sucursal2) REFERENCES sucursales(codigo_sucursal)
      );
    -- Insertar datos empleados
    INSERT INTO empleados VALUES ('EMP_01','ANGELICA','BLANCAS	MIRANDA',NULL,'suc-05');
    INSERT INTO empleados VALUES ('EMP_02','DAVID','ASPEITIA	ESCOBEDO',NULL,'suc-04');
    INSERT INTO empleados VALUES ('EMP_03','ANGEL','GALINDO	HERAS',NULL,'suc-03');
    INSERT INTO empleados VALUES ('EMP_04','ISMAEL','FERNANDEZ	HERNADEZ',NULL,'suc-01');
    INSERT INTO empleados VALUES ('EMP_05','MAURICIO','ANDA	JUAREZ',NULL,'suc-01');
    INSERT INTO empleados VALUES ('EMP_06','ALONSO','BLANCO	ANGELES',NULL,'suc-08');
    INSERT INTO empleados VALUES ('EMP_07','ALMA','SALAZAR	HUERTA',NULL,'suc-02');
    INSERT INTO empleados VALUES ('EMP_08','BLANCA','SANTOS	SANTIAGO',NULL,'suc-06');
    INSERT INTO empleados VALUES ('EMP_09','IGNACIO','HERNANDEZ	HERNNDEZ',NULL,'suc-07');
    INSERT INTO empleados VALUES ('EMP_10','MAURICIO','MARQUEZ	CHAVEZ',NULL,'suc-09');

    CREATE TABLE secciones(
      id_seccion VARCHAR(50) PRIMARY KEY,
        extension VARCHAR(50) NOT NULL,
        titulo VARCHAR(50),
        num_registro3 VARCHAR(50) NOT NULL,
        FOREIGN KEY (num_registro3) REFERENCES revistas(num_registro)
      );
    -- Ingresar datos a la tabla secciones
    INSERT INTO secciones VALUES ('1','esp','espectaculos','REV_100');
    INSERT INTO secciones VALUES ('2','dep','deportes','REV_100');
    INSERT INTO secciones VALUES ('3','pol','politica','REV_099');
    INSERT INTO secciones VALUES ('4','cin','cine','REV_102');
    INSERT INTO secciones VALUES ('5','hog','hogar','REV_100');
    INSERT INTO secciones VALUES ('6','cul','cultura','REV_103');
    INSERT INTO secciones VALUES ('7','vid','videojuegos','REV_101');

    CREATE TABLE ejemplares(
      id_ejemplar VARCHAR(50) PRIMARY KEY,
        num_ejemplar INT UNSIGNED NOT NULL,
        num_pagina INT UNSIGNED,
        fecha_ejemplar DATE NOT NULL,
        num_registro4 VARCHAR(50) NOT NULL,
        FOREIGN KEY (num_registro4) REFERENCES revistas(num_registro)
      );

    -- Ingresar datos a la tabla ejemplares
    INSERT INTO ejemplares VALUES ('M01',4855,56,'2021-09-23','REV_098');
    INSERT INTO ejemplares VALUES ('M02',1234,89,'2021-09-30','REV_101');
    INSERT INTO ejemplares VALUES ('M03',5343,78,'2021-10-09','REV_098');
    INSERT INTO ejemplares VALUES ('M04',5654,90,'2022-04-06','REV_098');
    INSERT INTO ejemplares VALUES ('M05',3434,100,'2022-03-15','REV_100');
    INSERT INTO ejemplares VALUES ('M06',6546,100,'2021-06-01','REV_100');
    INSERT INTO ejemplares VALUES ('M07',4534,56,'2022-05-15','REV_100');

    CREATE TABLE suc_rev(
      codigo_sucursal1 VARCHAR(50) NOT NULL,
        num_registro1 VARCHAR(50) NOT NULL,
        FOREIGN KEY (codigo_sucursal1) REFERENCES sucursales(codigo_sucursal),
        FOREIGN KEY (num_registro1) REFERENCES revistas(num_registro)
      );
    INSERT INTO suc_rev VALUES ('suc-01','REV_098');
    INSERT INTO suc_rev VALUES ('suc-01','REV_099');
    INSERT INTO suc_rev VALUES ('suc-01','REV_100');
    INSERT INTO suc_rev VALUES ('suc-02','REV_101');
    INSERT INTO suc_rev VALUES ('suc-03','REV_100');
    INSERT INTO suc_rev VALUES ('suc-04','REV_103');
    INSERT INTO suc_rev VALUES ('suc-05','REV_098');
    INSERT INTO suc_rev VALUES ('suc-05','REV_101');
    INSERT INTO suc_rev VALUES ('suc-06','REV_102');
    INSERT INTO suc_rev VALUES ('suc-07','REV_100');
    INSERT INTO suc_rev VALUES ('suc-07','REV_101');
    INSERT INTO suc_rev VALUES ('suc-08','REV_099');
    INSERT INTO suc_rev VALUES ('suc-09','REV_098');
    INSERT INTO suc_rev VALUES ('suc-10','REV_102');
    INSERT INTO suc_rev VALUES ('suc-10','REV_103');



    CREATE TABLE rev_per(
      num_registro2 VARCHAR(50) NOT NULL,
        nif_periodista1 VARCHAR(50) NOT NULL,
        FOREIGN KEY (num_registro2) REFERENCES revistas(num_registro),
        FOREIGN KEY (nif_periodista1) REFERENCES periodistas(nif_periodista)
      );

    INSERT INTO rev_per VALUES ('REV_098','PER_01');
    INSERT INTO rev_per VALUES ('REV_098','PER_07');
    INSERT INTO rev_per VALUES ('REV_098','PER_10');
    INSERT INTO rev_per VALUES ('REV_098','PER_12');
    INSERT INTO rev_per VALUES ('REV_099','PER_01');
    INSERT INTO rev_per VALUES ('REV_099','PER_03');
    INSERT INTO rev_per VALUES ('REV_099','PER_05');
    INSERT INTO rev_per VALUES ('REV_100','PER_02');
    INSERT INTO rev_per VALUES ('REV_100','PER_04');
    INSERT INTO rev_per VALUES ('REV_101','PER_01');
    INSERT INTO rev_per VALUES ('REV_101','PER_06');
    INSERT INTO rev_per VALUES ('REV_102','PER_02');
    INSERT INTO rev_per VALUES ('REV_102','PER_05');
    INSERT INTO rev_per VALUES ('REV_102','PER_08');
    INSERT INTO rev_per VALUES ('REV_103','PER_05');
    INSERT INTO rev_per VALUES ('REV_103','PER_09');
INSERT INTO rev_per VALUES ('REV_103','PER_11');

