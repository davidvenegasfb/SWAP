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

![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/0.png)

![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/1.png)


## 5.3 Replicar una BD MySQL con mysqldump


