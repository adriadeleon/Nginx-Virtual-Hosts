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

![image](https://user-images.githubusercontent.com/98842240/167388241-32626104-f0b1-4c78-adaa-a315e85d2f1e.png)


Cuando ejecutemos el default, debemos de escribir los dos nombres de los dos subdominios para poder ponerles un nombre y tener los dos por separado, le añadiré de nombre "AJDL".

Cuando hayamos creado estos dos subdominios debemos editarlos para cambiar la configuración del archivo, cambiando la página web (la ruta) y la IP dónde debe conectarse Nginx, en este caso pondremos de URL: *root var/www/adria* y de IP: (nuestra IP).

![image](https://user-images.githubusercontent.com/98842240/167171280-3a194d1d-d74a-4af4-80fb-a52adbbc1534.png)

Cuando accedamos a esta ubicación debemos lanzar este comando:

![image](https://user-images.githubusercontent.com/98842240/167171462-306e8f96-e9c1-4bfd-9ead-2df86cac186c.png)
 
 dónde tenemos que añadir el nombre de nuestro subdominio, en mi caso se llama "AJDL".
 
 ![image](https://user-images.githubusercontent.com/98842240/167388226-0755fd63-4742-4701-9afc-26e639056cca.png)
 
 Debemos acceder al directorio *sites-available* mediante comandos, en este caso el comando *cd* como aprendimos en la practica pasada.
 
 ![image](https://user-images.githubusercontent.com/98842240/167388996-057712a0-4f8b-43e5-bf5b-3d2efe7b291e.png)
 
 Una vez hayamos entrado, debemos crear dos copias del archivo con el nombre *default*. A los dos archivos que clonaremos debemos ponerle nombres diferentes en mi caso seerán las siglas de mi nombre *AJDL* y *AJDL1*. 
 
 ![image](https://user-images.githubusercontent.com/98842240/167388936-bc141f25-7d2b-4b5f-929d-8969860444d9.png)

Cuando realizemos las dos copias debemos modificar el primer archivo, en mi caso *AJDL*, para ello lo realizamos con el comando *vim* este comando puede ser que no esté instalado en tú máquina, por lo cual deberás instalarlo manualmente mediante consola mediante *apt install*.

Cuando hayamos accedido al archivo *AJDL* debemos acceder a la línea que contiene la palabra *server_name _* y debemos cambiarlo por *server_name AJDL.com*, una vez realizado esto, debemos ir a la línea root y cambiar *root /var/www/web (como ejemplo)* por *root /var/www/AJDL.com (nombre de mi subdominio)*.

- Una vez modificado el primer subdominio debemos acceder al segundo y realizar exactamente los mismos pasos, pero en este caso poner de nombre *AJDL1*.
 ___
 
 Una vez hayamos configurado todo, debemos ir a una página web y escribir la url de nuestro subdominio, después de esto debemos hacer que el host se conecte mediante la ip de nuestro ordenador. 
 
 Para ello modificamos el archivo *host*.
 ![image](https://user-images.githubusercontent.com/98842240/167390562-e21a65ee-b137-4896-8648-236145b1b50a.png)

Debemos editarlo y poner la ip del host con la url de nuestro subdominio.

Una vez hecho esto debemos acceder a la ruta */var/www/* con el comando que vimos con anterioridad, enn este caso el comando *cd*, una vez dentro debemos crear con el comando *mkdir* dos directorios con los nombres de los subdominios *AJDL* y *AJDL1*.

Cuando entremos a estos directorios debemos crear un archivo *index.html* y modificarlo con el código html referente al juego que queramos añadir en ese subdominio.

Para poder visualizar los juegos debemos ir al navegador y mediante Nginx debemos entrar con las url del subdominio mientras se conecta a nuestra ip del ordenador:

- AJDL.com:
![image](https://user-images.githubusercontent.com/98842240/167391226-33698bea-044f-4e8c-b366-c3ab7a56de55.png)

- AJDL1.com:
![image](https://user-images.githubusercontent.com/98842240/167391318-fac52df3-48a5-4296-9516-f52793d5427e.png)

___

- **Opinión personal:** Me ha costado más hacerlo esta vez que la primera vez que lo hiicmos antes de Pascua, me dio un fallo a la hora de reiniciar Nginx ya que al reiniciarlo de golpe se me borró del sistema y tuve que volver a instalarlo y generar todos los aarchivos de nuevo, no hubo problema pero perdí tiempo por eso.

Adrià
