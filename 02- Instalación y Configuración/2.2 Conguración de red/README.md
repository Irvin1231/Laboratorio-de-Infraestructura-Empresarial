# 2.2 — Configuración de red

## Objetivo

Verificar y documentar la configuración de red del servidor después de la instalación de Ubuntu Server.

## Configuración inicial

El servidor cuenta con dos interfaces Ethernet.

La interfaz `enp2s0f0` se encuentra activa y obtiene su configuración IPv4 mediante DHCP.

La interfaz `enp2s0f1` permanece sin conexión física y no participa actualmente en la comunicación de red.

La configuración de red es administrada mediante Netplan y `systemd-networkd`.

## Pruebas de conectividad

- Comunicación con el gateway.
- Salida hacia Internet mediante una dirección IP externa.
- Resolución de nombres mediante DNS.
- Comunicación desde otra computadora dentro de la misma red.
- Conexión remota mediante SSH.

Todas las pruebas realizadas fueron satisfactorias y no se presentó pérdida de paquetes.

## Decisión

Por el momento se mantiene la configuración mediante DHCP.

No se estableció una dirección IP estática debido a que actualmente no se cuenta con información suficiente sobre el rango de direcciones administrado por el dispositivo de red.

La configuración de una dirección permanente podrá realizarse posteriormente mediante una reservación DHCP o una configuración estática, una vez que se tenga acceso administrativo a la infraestructura de red.

## Resultado

El servidor cuenta con conectividad funcional y puede comunicarse con otros equipos de la red.

También se comprobó el acceso remoto mediante SSH, permitiendo administrar el servidor desde otra computadora sin necesidad de utilizar directamente el monitor conectado al equipo.

## Evidencias

Las evidencias de esta etapa se encuentran en la carpeta `evidencias/`.

Las direcciones IP, direcciones MAC y demás datos específicos de la infraestructura empresarial fueron omitidos o anonimizados para proteger información interna.
