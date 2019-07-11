# Ejemplo 1
```
$> docker run -v /ruta/scripts:/ruta/mnt/container --rm imagen:tag python /ruta/scripts/script.py
```
# Ejemplo 2, ejecutar 2 script o mas, separado por &&
```
$> docker run -v /ruta/scripts:/ruta/mnt/container --rm imagen:tag bash -c "python app1.py && python app2.py"
```
# Script Ruby:
```
$> docker run -v C:\Users\miuser\Desktop:/script --rm ruby:2.6 ruby /script/app.rb
```
# Instalacion de libreria con gem y ejecucion script Ruby, envio de 2 comandos a docker
```
$> docker run -v C:\Users\miuser\Desktop:/script --rm ruby:2.6 bash -c "gem install httparty && ruby /script/app.rb"
```
# Script Python
```
$> docker run -v C:\Users\miuser\Desktop:/script --rm python:3.7 python /script/app.py
```
# Script bash
```
$> docker run -v C:\Users\miuser\Desktop:/script --rm debian:buster sh /script/app.sh
```
# Script GO
```
$>  docker run -v C:\Users\miuser\Desktop:/script --rm golang:1.12 go run /script/app.go
```
# Script GO - Compilar y ejecutar
```
$> docker run -v C:\Users\miuser\Desktop:/script --rm golang:1.12 bash -c "go build -o /script/appcompilada /script/app.go && /script/appcompilada"
```
# Script PERL
```
$> docker run -v C:\Users\miuser\Desktop:/script --rm perl:5.30 bash -c "perl /script/app.pl" 
```
# Script Node 
```
$> docker run -v C:\Users\miuser\Desktop:/script -p 3000:3000 --rm node:8.16 bash -c "npm install express && node /script/app.js" 
```