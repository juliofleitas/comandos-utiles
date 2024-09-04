Ngrok y Exponer Servicios
Qué es Ngrok?
Ngrok es una herramienta que permite crear un túnel seguro hacia un servidor local, lo que permite exponer aplicaciones o servicios que se ejecutan en un equipo local a Internet. Básicamente, permite que una aplicación web que se ejecuta en un equipo local sea accesible a través de una URL pública. Esto es muy útil para desarrolladores que necesitan probar sus aplicaciones web en diferentes dispositivos o compartir sus aplicaciones con otros.

Ngrok crea una conexión segura entre su equipo local y la nube, lo que le permite acceder a su servidor local desde cualquier lugar del mundo. También proporciona un panel de control web para administrar su conexión y configurar diferentes opciones, como la autenticación y el registro de solicitudes.

Ngrok es fácil de usar y se puede instalar en diferentes sistemas operativos. Además, tiene una versión gratuita y varias opciones de pago con características adicionales, como el uso de subdominios personalizados y la asignación de puertos dedicados.

Qué es un servicio local y cómo se expone?
Un servicio local es un servicio o aplicación que se ejecuta en un equipo local, como una aplicación web, una API o un servidor de base de datos. Estos servicios suelen estar disponibles solo en el equipo donde están instalados y no son accesibles desde otros equipos en la red o desde Internet.

Los usuarios pueden utilizar Ngrok para exponer estos servicios locales y hacerlos accesibles desde cualquier lugar del mundo a través de una URL pública. Esto es útil para desarrolladores que necesitan probar sus aplicaciones en diferentes dispositivos o compartir sus aplicaciones con otros, ya que les permite acceder a sus servicios locales sin tener que exponerlos a Internet directamente. Además, Ngrok facilita la configuración de conexiones seguras y elimina la necesidad de abrir puertos en el router, lo que lo hace una solución fácil y segura para exponer servicios locales.

Por que utilizar una versión opensource en lugar de la oficial
La seguridad es un factor importante cuando se trata de exponer servicios a través de Internet. Mientras que Ngrok es una herramienta popular y útil para crear túneles seguros y exponer servicios locales, algunos usuarios pueden tener preocupaciones sobre la seguridad de su código cerrado y la privacidad de sus datos.

Una de las ventajas de utilizar una versión de Ngrok de código abierto (open source) es que cualquier persona puede revisar y auditar el código para detectar posibles vulnerabilidades y problemas de seguridad. Esto significa que hay una mayor transparencia y confianza en el software, ya que los usuarios pueden ver exactamente lo que está sucediendo en el código subyacente.

Además, los desarrolladores de la versión open source de Ngrok pueden responder a las preocupaciones de seguridad de la comunidad y proporcionar soluciones rápidas en caso de que se descubran vulnerabilidades. También hay una comunidad de usuarios activa que puede proporcionar soporte y asistencia en caso de que surjan problemas.

Por otro lado, al ser una versión cerrada de código (closed source), los usuarios no pueden revisar el código y tienen que confiar en que la empresa detrás de Ngrok está tomando las medidas de seguridad necesarias para proteger sus datos y privacidad.

En conclusión, utilizar una versión open source de Ngrok proporciona una mayor transparencia y seguridad, ya que los usuarios pueden revisar el código y confiar en la comunidad de usuarios para solucionar posibles vulnerabilidades y problemas de seguridad.

cómo instalar un cliente de ngrok opensource
Abre la aplicación Termux en tu dispositivo Android.

Instala las dependencias necesarias ejecutando el siguiente comando:

pkg install openssh tmux
Descarga el cliente de ngrok opensource en tu dispositivo Android ingresando el siguiente comando:

git clone https://github.com/stringmanolo/ngrok.git
Navega hasta el directorio donde se encuentra el cliente de ngrok ingresando el siguiente comando:

cd ngrok
Configura el cliente de ngrok utilizando el asistente ingresando el siguiente comando:

chmod 775 ngrokWizard.sh
./ngrokWizard.sh
Sigue las instrucciones que se muestran en pantalla para configurar el cliente de ngrok. Esto incluirá generar una clave pública ECDSA, pegar la clave en la página de configuración de ngrok y establecer el puerto de tu servidor.

Una vez que hayas configurado el cliente de ngrok utilizando el asistente, puedes iniciar y detener el cliente utilizando los siguientes comandos:

./ngrokStart.sh
y

./ngrokStop.sh
El primer comando iniciará el cliente de ngrok y establecerá una conexión inversa SSH con el servidor, lo que permitirá que el tráfico se reenvíe a través de ngrok. El segundo comando detendrá la conexión SSH y cerrará el cliente de ngrok.

Asegúrate de establecer el puerto correcto cada vez que ejecutes el comando ngrokStart.sh.

Ahora puedes usar el cliente de ngrok opensource para exponer tu servidor web a través de ngrok en tu dispositivo Android usando Termux. Recuerda que la URL pública que te proporciona ngrok cambiará cada vez que ejecutes el comando ngrokStart.sh, por lo que es posible que debas actualizar la URL que compartes con otros usuarios cada vez que la uses.