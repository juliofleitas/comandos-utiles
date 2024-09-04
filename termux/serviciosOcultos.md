Servicios Ocultos
Qué es?
Un Hidden Service (también conocido como Servicio Oculto) es un sitio web alojado en la red Tor (conocida también como Dark Web o internet profunda) que se encuentra en una ubicación desconocida para los usuarios normales de la web y que solo puede ser accedido a través de la red Tor. En lugar de tener una dirección IP pública y estar alojado en un servidor web estándar, un Hidden Service se aloja en una red anónima y utiliza una dirección web única que termina en ".onion".

Cuando un usuario intenta acceder a un sitio web alojado en un Hidden Service, su conexión se enruta a través de una serie de nodos de la red Tor, lo que proporciona un alto nivel de anonimato.

Los Hidden Services se pueden utilizar para una amplia variedad de propósitos, desde sitios web de periodismo y activismo político hasta mercados en línea y comunidades en línea privadas. Algunos usuarios también utilizan Hidden Services para alojar sus propios sitios web personales sin revelar su ubicación física o dirección IP pública.

En resumen, los Hidden Services ofrecen una forma segura y anónima de alojar y acceder a contenido en línea, lo que los hace útiles para una variedad de aplicaciones en línea que requieren privacidad y anonimato.

Crear un servicio oculto
1 Crea una carpeta para el sitio web y otra para el hidden service utilizando los siguientes comandos:
mkdir -p $PREFIX/var/lib/tor/hidden_service/mywebsite;
mkdir -p $PREFIX/etc/tor/hidden_service;
2 Cambia los permisos de la carpeta:
chmod 700 $PREFIX/var/lib/tor/hidden_service/mywebsite
3 Agrega las líneas de configuración de Tor al archivo torrc utilizando el siguiente comando:
echo -e "HiddenServiceDir $PREFIX/var/lib/tor/hidden_service/mywebsite\nHiddenServicePort 80 127.0.0.1:8000" >> $PREFIX/etc/tor/torrc;
4 Reinicia el servicio Tor ejecutando el siguiente comando:
killall tor;
tor &
5 Crea un archivo index.html para el sitio web utilizando el siguiente comando:
echo "Hello, world!" > $PREFIX/var/lib/tor/hidden_service/mywebsite/index.html;
6 Inicia un servidor web local en la carpeta mywebsite usando el siguiente comando:
cd $PREFIX/var/lib/tor/hidden_service/mywebsite;
python3 -m http.server 8000 &
7 Obten la dirección de tu servicio:
cat $PREFIX/var/lib/tor/hidden_service/mywebsite/hostname
8 Accede al sitio web a través del Hidden Service ejecutando el siguiente comando en la terminal:
torify curl http://<hidden-service-address>.onion/;
Reemplaza <hidden-service-address> con la dirección del Hidden Service que obtuviste en el paso 7.

Otra forma de comprobar si funciona es utilizando el servicio tor2web. Te vas a este enlace en cualquier navegador e introduces la dirección de tu servicio. Si funciona verás tu página web con el mensaje "Hello World". Esta web sirve para poder visualizar páginas web alojadas en la red tor en tu navegador sin necesidad de instalar el navegador de tor.

9 Para detener el servicio Tor y el servidor web de Python, ejecuta los siguientes comandos en la terminal:
killall tor;
killall python3;
Con estos pasos, se creará una carpeta para el sitio web y otra para el hidden service, se configurará el archivo de Tor para exponer el servidor web local en el Hidden Service, se creará un archivo index.html para el sitio web y se iniciará un servidor web local. Cualquier persona con conexión a tor podrá acceder a tu servicio utilizando el dominio .onion.