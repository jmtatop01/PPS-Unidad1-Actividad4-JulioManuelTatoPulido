# PPS-Unidad1-Actividad4-JulioManuelTatoPulido

Tenemos varios objetivos:

> [Buscar distintas alternativas de una Sandbox](#alternativas-de-sandboxs)

> [Crear el proyecto y probarlo](#crear-el-proyecto-y-probarlo)

---
## Alternativas de Sandboxs

Hay diferentes aplicaciones con las que puedes tener una Sandbox, en las cuáles se puede hacer un estudio de las consecuencias y de los riesgos en un estado de aislamiento para no perjudicar a nuestro ordenador:

- Firejail → Ligera y fácil de usar en Linux. Restringe el acceso de las aplicaciones al sistema.

- AppArmor → Mecanismo de seguridad en Linux que permite definir perfiles de restricción para aplicaciones.

- SELinux → Similar a AppArmor, pero con un control más granular sobre permisos y accesos.

- Bubblewrap → Minimalista y utilizado en sistemas Linux para aislar procesos.

- Sandboxie Plus → Versión moderna de Sandboxie, útil en Windows para aislar aplicaciones sospechosas.

## Crear el proyecto y probarlo

Para esta práctica utilizaré Firejail en una máquina virtual Ubuntu, para ello lo he tenido que instalar con el Firetools también para poder realizarlo de forma gráfica:

~~~
sudo apt update && sudo apt install firejail -y
sudo apt update && sudo apt install firetools -y
~~~

Después, he pasado a iniciar las dos aplicaciones y ejecutar el comando ´´firejail --noprofile python3 calculadora.py``

<div align="center">
  <img src="1.png" width="500">
</div>


### Checkstyle

Checkstyle es un plugin que se utiliza para verificar que el código siga un estándar de estilo definido. Es ideal para mantener la coherencia en equipos grandes, revisando el formato y la estructura del código automáticamente.

<div align="center">
  <img src="3.png" width="500">
</div>

