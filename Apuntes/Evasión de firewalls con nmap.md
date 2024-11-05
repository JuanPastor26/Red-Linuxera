# Evasion de firewalls con nmap
`nmap -p80 192.168.1.10` -> Escaneo básico de nmap a un puerto de un host
## Opciones adicionales
- `-f` -> Fragmenta los paquetes enviados durante el escaneo para que no puedan ser detectados por el firewall del host objetivo.
- `--mtu 8` -> Tamaño máximo de los paquetes enviados durante el escaneo (en múltiplos de 8).
- `-D 192.168.1.123` -> Enviar paquetes durante el escaneo utilizando una dirección IP falsa, o varias.
- `-source-port 53` -> Específica el puerto de origen de los paquetes enviados durante el escaneo.
- `-data-length 20` -> Aumenta el length de los paquetes enviados en cierta cantidad.
- `-spoof-mac Dell` -> Falsifica la MAC de los paquetes enviados durante el escaneo. Utilizando el nombre de algún fabricante o una dirección MAC especifica (00:11:22:33:44:55).
- `-sS` -> Realiza un escaneo SYN con el host victima sin crear una conexión completa entre estos dos.
- `-min-rate 5000` -> Especifica la velocidad mínima de paquetes por segundo para realizar el escaneo.
