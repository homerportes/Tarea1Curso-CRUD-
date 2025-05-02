<h4>API de gestion de usuarios basica</h4>

Este proyecto es un crud basico para gestion de usuario, es una Web Api con .Net core 9, swagger y Entity Framework.
se uso como base de datos sql server.

CREATE DATABASE db_usuario;
USE db_usuario;

CREATE TABLE Usuario(
 id INT PRIMARY KEY IDENTITY,
 nombres VARCHAR(50) NOT NULL,
 apellidos VARCHAR(50) NOT NULL,
 correo VARCHAR(100) NOT NULL,
 username VARCHAR(100),
 fecha_creacion DATETIME
)
GO 

ALTER TABLE Usuario ALTER COLUMN username VARCHAR(100) NOT NULL;
ALTER TABLE Usuario ADD CONSTRAINT UQ_Correo UNIQUE (correo);
