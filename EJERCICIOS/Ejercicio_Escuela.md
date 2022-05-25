![image](https://user-images.githubusercontent.com/34118685/169571214-72092cab-daa0-40f6-b1a7-30928857751d.png)

https://www.db-fiddle.com/f/f5YQQo1MCXhD95LFCdiYFB/6

    CREATE DATABASE escuela;
    USE escuela;

    CREATE TABLE profesores(
      codigo_profesor INT UNSIGNED PRIMARY KEY,
      nombre_profesor VARCHAR(50) NOT NULL,
        direccion_profesor VARCHAR(100) NOT NULL,
        telefono_profesor VARCHAR(50)	
      );

    CREATE TABLE materias(
      codigo_materia INT UNSIGNED PRIMARY KEY,
        nombre_materia VARCHAR(50) NOT NULL
      );

    CREATE TABLE jefe_grupo(
      id_jefe INT UNSIGNED PRIMARY KEY,
        nombre_jefe VARCHAR(50) NOT NULL,
        apellido_jefe VARCHAR(50) NOT NULL,
        grupo_jefe VARCHAR(20)
      );

    CREATE TABLE alumnos(
      id_alumno INT UNSIGNED PRIMARY KEY,
        nombre_alumno VARCHAR(50) NOT NULL,
        apeliido_alumno VARCHAR(50) NOT NULL,
        num_expedientes INT NOT NULL,
        fecha_nacimiento DATE,
        id_jefe1 INT UNSIGNED NOT NULL,
        FOREIGN KEY (id_jefe1) REFERENCES jefe_grupo(id_jefe) 	
      );

    CREATE TABLE prof_mat(
      codigo_profesor1 INT UNSIGNED NOT NULL,
        codigo_materia1 INT UNSIGNED NOT NULL,
        FOREIGN KEY (codigo_profesor1) REFERENCES profesores(codigo_profesor),
        FOREIGN KEY (codigo_materia1) REFERENCES materias(codigo_materia)
      );

    CREATE TABLE mat_alum(
      codigo_materia2 INT UNSIGNED NOT NULL,
        id_alumno1 INT UNSIGNED NOT NULL,
        FOREIGN KEY (codigo_materia2) REFERENCES materias(codigo_materia),
        FOREIGN KEY (id_alumno1) REFERENCES alumnos(id_alumno)
      );
