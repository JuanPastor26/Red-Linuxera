# Fuzzing y enumeración de archivos en un servidor web
## gobuster
`gobuster dir -u www.facebook.com -w /home/pastor/repos/SecLists/Discovery/Web-Content/directory-list-2.3-medium.txt -t 200`
### Opciones adicionales para gobuster
- `-b 403,404` -> Ocultar código de estado.
- `--add-slash` -> Añadir slash (/) al final de la ruta.
- `-x php,html,txt` -> Realizar fuzzing de los archivos con las extensiones ingresadas.
- `-s 200 -b ''` -> Mostrar resultados con código de estado 200.
## wfuzz
  `wfuzz -c -t 200 -w /home/pastor/repos/SecLists/Discovery/Web-Content/directory-list-2.3-medium.txt www.facebook.com/FUZZ/`
### Opciones adicionales para wfuzz
  - `--hc=404` -> Ocultar código de estado.
  - `--sc=404` -> Mostrar código de estado.
  - `--sl=216` -> Mostrar resultados con 216 líneas.
  - `--hl=216` -> Ocultar resultados con 216 líneas.
  - `--hh=85` -> Ocultar resultados con 85 caracteres.
  - `--sh=85` -> Mostrar resultados con 85 caracteres.
  - `-z list,html-txt-php`  -> Listar resultados por extensiones (www.facebook.com/FUZZ.FUZ2Z).
  - `-z range,1-2000 'www.facebook.com/product_id=FUZZ'` -> Aplicar un rango a un valor específico.
## Diccionarios
https://github.com/danielmiessler/SecLists.git
