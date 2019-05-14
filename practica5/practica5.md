# Práctica 5: Replicación de bases de datos MySQL
### Autores: David Joaquín González-Venegas Guerra-Librero y Marina Hurtado Rosales
### Correos: davidvenegasfb@correo.ugr.es; marinahurtado@correo.ugr.es

## 5.2 Crear un tar con ficheros locales y copiarlos en un equipo remoto

## 5.2 Crear una BD e insertar datos

Vamos a crear una BD en MySQL e insertar algunos datos. Así tendremos datos con los cuales hacer las copias de seguridad:

Entramos en la interfaz de la línea de comandos de MySQL con:
>mysql -uroot -p

Creamos la base de datos contactos con:
>create database contactos;

Declaramaos que vamos a usar dicha tabla con:
>use contactos;

Creamos la tabla datos con:
>create table datos(nombre varchar(100),tlf int);

Mostramos todas las tabla con:
>show tables;

Insertamos una linea de datos en nuestra tabla con:
>insert into datos(nombre,tlf) values ("pepe",95834987);

![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/0.png)

Aquí podemos ver como como podemos hacer consultas sql como:
>select * from datos;

O que nos diga los tipos de datos de la tabla:
>describe datos;

![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/1.png)


## 5.3 Replicar una BD MySQL con mysqldump

![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/2.png)
![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/3.png)
![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/4.png)
![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/5.png)
![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/6.png)

