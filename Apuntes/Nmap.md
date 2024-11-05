# Nmap
`nmap -p- 192.168.1.1` -> Escanear todos los puertos de una dirección IP.
## Opciones adicionales
- `-p1-65535` o `-p-` -> Escanea los 65535 puertos.
- `--top-ports 100` -> Escanea los 100 puertos principales.
- `--open` -> Muestra los puertos abiertos.
- `-v` o `-vv` o `-vvv` -> Muestra detalles durante el escaneo.
- `-n` -> Desactiva resolución DNS.
- `-T5` -> Plantilla de tiempo para velocidad de escaneo (1 a 5).
- `-sT` -> Escanea realizando una conexión completa con el host victima, TCP Connect(), (SYN, SYN/ACK, ACK).
- `-Pn` -> Determina por defecto que el host está activo.
- `-sU` -> Escanea puertos UDP.
- `-sn` -> Descubre dispositivos en red local.
- `-O` -> Detecta el sistema operativo del host.
- `-sV` -> Detecta los servicios que se están ejecutando en el host.
