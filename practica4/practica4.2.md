# Práctica 4: Asegurar la granja web
### Autores: David Joaquín González-Venegas Guerra-Librero y Marina Hurtado Rosales
### Correos: davidvenegasfb@correo.ugr.es; marinahurtado@correo.ugr.es

### Instalar un certificado SSL autofirmado para configurar el acceso por HTTPS

Vamos a generar un certificado SSL autofirmado en Ubuntu Server:

> Activamos el módulo SSL de Apache:

![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica4/imagenes/1.png)

> Pasamos a generar los certificados:

![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica4/imagenes/2.png)

> Editamos el archivo de configuración del sitio default-ssl, y agregamos estas lineas debajo de donde pone SSLEngine on:
SSLCertificateFile /etc/apache2/ssl/apache.crt
SSLCertificateKeyFile /etc/apache2/ssl/apache.key

![img](https://github.com/davidvenegasfb/SWAP/blob/master/practica4/imagenes/3.png)
