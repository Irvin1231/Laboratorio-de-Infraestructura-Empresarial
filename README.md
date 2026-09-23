# Laboratorio de Infraestructura Empresarial
Proyecto práctico de infraestructura orientado a la implementación y administración de un servidor físico para resolver necesidades reales de TI dentro de la empresa.

El proyecto permitirá desarrollar conocimientos prácticos en Linux, redes, almacenamiento, respaldos, monitoreo, seguridad, automatización, virtualización, nube e inteligencia artificial aplicada a infraestructura.

## 1. Evaluación inicial del servidor
### 1.1 Identificación del equipo

- **Fabricante:** HPE
- **Modelo:** ProLiant MicroServer Gen10

### 1.2 Procesador

- **Modelo:** AMD Opteron X3421 APU
- **Núcleos:** 4
- **Frecuencia:** aproximadamente 2.1 GHz

### 1.3 Memoria RAM

- **Memoria instalada y funcional:** 4 GB DDR4 ECC UDIMM.
- **Memoria adicional disponible para pruebas:** módulos de 16 GB.
- **Tipo de memoria adicional probada:** RDIMM.

#### Prueba de compatibilidad

Se realizó una prueba utilizando uno de los módulos de memoria de 16 GB disponibles, con el objetivo de determinar si podía ser utilizado en el servidor.

Al instalar el módulo, el servidor no inició correctamente.

Posteriormente se revisaron las características del módulo y se identificó que corresponde a memoria RDIMM, mientras que la memoria funcional instalada en el servidor es ECC UDIMM.

**Resultado:** el módulo RDIMM probado no es compatible con la configuración del servidor.

La configuración funcional se mantiene con 4 GB de memoria DDR4 ECC UDIMM.

### 1.4 Almacenamiento

- **Fabricante:** Toshiba
- **Modelo:** DT01AC
- **Capacidad:** aproximadamente 1 TB
- **Interfaz:** SATA
- **Puerto detectado:** SATA Port 2

El disco fue detectado correctamente durante la revisión del BIOS.

### 1.5 Conectividad de red

El servidor cuenta con dos interfaces de red Ethernet de 1 Gb.

Estas interfaces permitirán establecer posteriormente la conectividad del servidor con la red y administrar el equipo de forma remota mediante SSH.

### 1.6 Virtualización

Durante la revisión de la configuración del procesador en el BIOS se verificó que la opción **SVM Mode** se encuentra habilitada.

Esto indica que el procesador tiene habilitada la virtualización por hardware.

La virtualización no forma parte de la implementación inicial, pero se mantiene como una capacidad disponible para etapas posteriores del proyecto.

### 1.7 Estado inicial del servidor

El servidor inicia correctamente y permite acceder al BIOS.

Durante la evaluación no se encontró un sistema operativo instalado ni una entrada de arranque correspondiente a un sistema operativo.

Al salir del BIOS, el equipo ingresó a EFI Shell, lo que confirmó que actualmente no existe un medio de almacenamiento con un sistema operativo configurado para iniciar.
