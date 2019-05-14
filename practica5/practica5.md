# Práctica 5: Replicación de bases de datos MySQL
### Autores: David Joaquín González-Venegas Guerra-Librero y Marina Hurtado Rosales
### Correos: davidvenegasfb@correo.ugr.es; marinahurtado@correo.ugr.es

## 5.1 Crear un tar con ficheros locales y copiarlos en un equipo remoto

NECESITO CONEXIÓN

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

Vamos a usar mysqldump para generar copias de seguridad de BD.

Podemos ver todas las opciones disponibles con el comando:
>mysqldump --help

En primer lugar debemos de tener en cuenta que los datos pueden estar actualizándose constantemente en el servidor de BD principal. En este caso, antes de hacer la copia de seguridad en el archivo .SQL debemos evitar que se acceda a la BD para cambiar nada. Para ello haremos:

>FLUSH TABLES WITH READ LOCK;

![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/2.png)

Ahora ya podemos usar mysqldump para guardar los datos.
![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/3.png)

Si hacemos un vim de contactos.sql veremos:
![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/4.png)

Y desbloqueamos por último las tablas:
![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/5.png)

VARIAS COSAS CON CONEXIÓN

Creamos la tabla en la segunda máquina para hacerlo con un solo comando:
![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica5/6.png)

