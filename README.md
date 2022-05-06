# Nginx-Virtual-Hosts | By Adrià
![image](https://user-images.githubusercontent.com/98842240/166708431-df70b37e-6794-46f7-8b7c-dcb72d3e9fb9.png)

___
- Introducción.
___
¿Que es Nginx?
Nginx es un servidor web/proxy inverso ligero de alto rendimiento y un proxy para protocolos de correo electrónico. Es software libre y de código abierto, licenciado bajo la Licencia BSD simplificada; también existe una versión comercial distribuida bajo el nombre de Nginx Plus.

¿Para que sirve Nginx?
NGINX es un servidor web open source de alta performance que ofrece el contenido estático de un sitio web de forma rápida y fácil de configurar. Ofrece recursos de equilibrio de carga, proxy inverso y streaming, además de gestionar miles de conexiones simultáneas.

___
- Instalación y Configuración Nginx.
___

Para configurar Nginx copiaremos el archivo default ubicado en la ruta del archivo para utilizarlo como plantilla, estableciendo nuestra URL personalizada.

Como nos solicita 2 subdominios, los cuales crearemos con el dominio principal y para ellos será necesario crearlo mediante código.

Cuando hayamos creado estos dos subdominios debemos editarlos para cambiar la configuración del archivo, cambiando la página web (la ruta) y la IP dónde debe conectarse Nginx, en este caso pondremos de URL: *root var/www/adria* y de IP: (nuestra IP).

![image](https://user-images.githubusercontent.com/98842240/167171280-3a194d1d-d74a-4af4-80fb-a52adbbc1534.png)

Cuando accedamos a esta ubicación debemos lanzar este comando:

![image](https://user-images.githubusercontent.com/98842240/167171462-306e8f96-e9c1-4bfd-9ead-2df86cac186c.png)
 
 dónde tenemos que añadir el nombre de nuestro servidor, en mi caso se llama "AJDL"
