# Enumeración de subdominios
## CTFR (método pasivo)
- https://github.com/UnaPibaGeek/ctfr.git
- `python3 ctfr.py -d facebook.com`
## Sublist3r (Método pasivo)
- https://github.com/aboul3la/Sublist3r.git
- `python3 sublist3r.py -d www.facebook.com`
## gobuster (método activo)
`gobuster vhost -u www.facebook.com -w /home/pastor/repos/SecLists/Discovery/DNS/subdomains-top1million-5000.txt -t 20`
## wfuzz (método activo)
`wfuzz -c -t 20 -w /home/pastor/repos/SecLists/Discovery/DNS/subdomains-top1million-5000.txt -H "Host: FUZZ.facebook.com" www.facebook.com`
### Opciones adicionales para wfuzz
- `--hc=404` -> Ocultar código de estado
- `--sc=200` -> Mostrar código de estado
