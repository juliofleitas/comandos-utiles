Tor, Configuración y Uso
Qué es Tor?
Tor (The Onion Router) es una red de comunicaciones en línea diseñada para proporcionar anonimato y privacidad a los usuarios de Internet. Fue desarrollado originalmente por la Marina de los Estados Unidos para proteger las comunicaciones gubernamentales, pero posteriormente se convirtió en un proyecto de código abierto para permitir que cualquier persona pueda utilizarlo.

Tor funciona enrutando las conexiones de Internet a través de una serie de nodos (también llamados "nodos de cebolla" o "onion routers") distribuidos por todo el mundo. Cada nodo en la red solo conoce la dirección IP del nodo anterior y el siguiente nodo en la cadena, lo que hace que sea difícil (aunque no imposible) rastrear las comunicaciones de un usuario de Internet.

Además, Tor también utiliza técnicas de cifrado para proteger las comunicaciones y garantizar que solo el usuario final pueda leer el contenido de los mensajes. Esto hace que Tor sea una herramienta valiosa para aquellos que desean proteger su privacidad y anonimato en línea, ya sea por razones políticas, de seguridad o simplemente por preferencia personal.

Instalación, configuración y uso
1 Abre Termux y asegúrate de que estás en la última versión actualizada. Para actualizar, escribe en la terminal:
apt update && apt upgrade
2 A continuación, es necesario instalar el paquete de Tor y torify. Para hacerlo, escribe en la terminal:
pkg install tor torsocks
3 Añade las siguientes líneas al archivo de configuración de Tor, usando el comando echo:
echo 'ControlPort 9051' >> $PREFIX/etc/tor/torrc && echo 'CookieAuthentication 1' >> $PREFIX/etc/tor/torrc
4 Inicia el servicio de Tor en background usando el ampersand:
tor &
Nota: El ampersand al final del comando permite que el proceso se ejecute en segundo plano, lo que significa que puedes seguir utilizando la terminal mientras Tor está activo.

5 Para asegurarte de que Tor está funcionando, ejecuta:
torify curl -s https://check.torproject.org/ | grep -q "Congratulations"
Este comando debería mostrar un mensaje de felicitación si estás usando Tor. Si no ves el mensaje, es posible que algo esté mal configurado o que Tor no esté funcionando correctamente.

6 Ahora puedes usar Tor con cualquier aplicación que soporte proxies SOCKS5, incluyendo curl. Simplemente precede cualquier comando que quieras ejecutar con torsocks. Por ejemplo:
torsocks curl https://example.com
7 Cuando hayas terminado de usar Tor, detén el servicio ejecutando el siguiente comando:
killall tor
¡Listo! Ahora sabes cómo instalar, configurar y usar Tor en Termux. Recuerda que el uso de Tor es importante para proteger tu privacidad y anonimato en línea.