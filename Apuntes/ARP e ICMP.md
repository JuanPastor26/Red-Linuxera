# ARP e ICMP
- `arp-scan -I enp0s3 --localnet` -> Descubrir dispositivos en red local. Cambia enp0s3 por tu adaptador de red.
- `arp-scan -I enp0s3 --localnet --ignoredups` -> Descubrir dispositivos en red local ignorando dispositivos duplicados.
- `ping -c 1 192.168.1.1` -> Enviar ping a una dirección IP
- `timeout 1 bash "ping -c 1 192.168.1.1"` -> Tiempo máximo de ejecución de un comando en bash (en segundos)
- `masscan -p80,445,8080 -Pn 192.168.0.0/16 --rate=10000` -> Utiliza masscan para escanear los puertos especificados en la red local con una velocidad de 10000 paquetes por segundo
