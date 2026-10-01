
# 2.1 — Instalación de Ubuntu Server

## Objetivo
Instalar Ubuntu server en HPE PROLIANT MICROSERVER Gen10 para establecer una base del entorno en nuestra infrestructura.

## Preparación
  

## Estado

**Instalación completada correctamente.**
Se descargo la imagen oficial de Ubuntu Server 26.04.01 LTS para arquitectura AMD64.

Antes de utilizarla se verifico su integridad mediante SHA-256

Posteriormente se creó una USB booteable utilizando Rufus con configuración UEFI y esquema de partición GPT.

## Instalación

El servidor se configuró para iniciar desde la USB mediante el menú de arranque UEFI.

Durante la instalación se realizaron las siguientes configuraciones:

- Idioma: Español
- Teclado: Español
- Tipo de instalación: Ubuntu Server
- Red: Ethernet mediante DHCP
- Dirección IP obtenida: `192.168.1.65/24`
- Mirror de Ubuntu: `mx.archive.ubuntu.com`
- Disco de instalación: Toshiba de aproximadamente 1 TB
- Particionado: uso completo del disco
- Administración del almacenamiento: LVM
- Cifrado: no habilitado
- Usuario administrativo: `admin-ti`
- OpenSSH Server: instalado
- Ubuntu Pro: omitido
- Paquetes adicionales: ninguno

El almacenamiento se configuró mediante LVM, dejando espacio disponible dentro del grupo de volúmenes para poder utilizarlo posteriormente según las necesidades del proyecto.

## Finalización
## Finalización

Una vez terminada la instalación, se reinició el servidor y se retiró el medio USB.

En el primer arranque se verificó el acceso al sistema mediante consola y se realizó el inicio de sesión con el usuario administrativo creado durante la instalación.

El servidor inició correctamente en modo consola, sin entorno gráfico, como corresponde a una instalación de Ubuntu Server.

## Resultado

Ubuntu Server 26.04.1 LTS quedó instalado y operativo en el HPE ProLiant MicroServer Gen10.

El servidor cuenta actualmente con conectividad de red y acceso mediante SSH, quedando preparado para continuar con la configuración de red y administración remota.

## Evidencias

Las evidencias del proceso de instalación se encuentran en la carpeta evidencias.
