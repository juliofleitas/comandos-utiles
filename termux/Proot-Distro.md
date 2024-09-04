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


Supported distributions:

  * Alpine Linux

    Alias: alpine
    Installed: no
    Comment: Rolling release branch (edge).

  * Arch Linux

    Alias: archlinux
    Installed: no
    Comment: Currently available only AArch64 and ARM ports.

  * Artix Linux

    Alias: artix
    Installed: no
    Comment: Currently available only for AArch64.

  * Debian (bookworm)

    Alias: debian
    Installed: no
    Comment: Stable release.

  * Debian (bullseye)

    Alias: debian-oldstable
    Installed: no
    Comment: Old stable release.

  * deepin

    Alias: deepin
    Installed: no
    Comment: Supports only 64-bit CPUs.

  * Fedora

    Alias: fedora
    Installed: no
    Comment: Version 40. Supports only 64-bit CPUs.

  * Manjaro

    Alias: manjaro
    Installed: no
    Comment: Currently available only for AArch64.

  * OpenKylin

    Alias: openkylin
    Installed: no
    Comment: Version 'nile'. Supports only 64-bit CPUs.

  * OpenSUSE

    Alias: opensuse
    Installed: no
    Comment: Rolling release (Tumbleweed).

  * Pardus

    Alias: pardus
    Installed: no
    Comment: Version 'yirmibir'. Not available for ARM 32 bit.

  * Ubuntu (24.04)

    Alias: ubuntu
    Installed: no
    Comment: LTS release (noble). Not available for x86 32-bit (i686) CPUs.

  * Ubuntu (22.04)

    Alias: ubuntu-oldlts
    Installed: no
    Comment: Previous LTS release (jammy). Not available for x86 32-bit (i686) CPUs.

  * Void Linux

    Alias: void
    Installed: no

Install selected one with: proot-distro install <alias>



