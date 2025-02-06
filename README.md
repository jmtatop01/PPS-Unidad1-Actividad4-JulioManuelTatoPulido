# PPS-Unidad1-Actividad4-JulioManuelTatoPulido

Tenemos varios objetivos:

> [Buscar distintas alternativas de una Sandbox](#Alternativas de Sandboxs)

> [Crear el proyecto y probarlo](#Crear el proyecto y probarlo)

---
## Alternativas de Sandboxs

1. Primero creamos las carpetas necesarias y cambiamos el propietario:
~~~
sudo mkdir -p  $HOME/docker/eclipse/datos
sudo chown -R kali:kali eclipse
~~~

2. Configuramos el entorno gráfico:

~~~
export DISPLAY=:0
startxwin -- -listen tcp &
xhost + 
~~~

3. Lanzamos el contenedor:

~~~
sudo docker run -ti --rm \
           --ulimit nofile=8096:8096\
           -e DISPLAY=$DISPLAY \
	       -e artifactory_host='IP:PUERTO'\
		   --name eclipse \
           -v /tmp/.X11-unix:/tmp/.X11-unix \
           -v `pwd`:/workspace \
           -v $HOME/docker/eclipse/datos:/home/developer \
           dockeruc/eclipse
~~~

<div align="center">
  <img src="2.png" width="500">
</div>

## Crear el proyecto y probarlo

Las dos extensiones que comentaré a continuación han sido instalados en Visual Studio, que va a ser el IDE que vaya a utilizar en estas prácticas.

### Checkstyle

Checkstyle es un plugin que se utiliza para verificar que el código siga un estándar de estilo definido. Es ideal para mantener la coherencia en equipos grandes, revisando el formato y la estructura del código automáticamente.

<div align="center">
  <img src="3.png" width="500">
</div>

