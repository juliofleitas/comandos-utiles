Proot-Distro

Proot distro es una versión custom del comando proot que ha sido diseñada para Termux. Con proot-distro podremos instalar distribuciones populares de GNU/Linux en Termux. Esto nos va a permitir instalar programas de esas distribuciones y disponer del sistema de ficheros común de GNU/Linux.

Lista las distribuciones disponibles

proot-distro list

Mustra las distribuciones de GNU/Linux disponibles, su nombre, su alias y su estado de instalación

Instala una distribución

proot-distro install alpine

Para instalar una distribución, debes utilizar el alias correspondiente a 

la distribución que deseas instalar.

Arranca una distribución

proot-distro login alpine

Haz copia de seguridad de una distribución

proot-distro backup alpine

Elimina una distribución

proot-distro remove alpine

Elimina y reinstala una distribución

proot-distro reset alpine

Recupera un sistema mediante copia de seguridad

proot-distro restore alpine

Arranca una distribución aislada de Termux

proot-distro login alpine --isolated

Ejecuta un comando desde una distribución

proot-distro login alpine --isolated -- pwd