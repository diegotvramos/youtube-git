# Curso de _Git_ & _GitHub_

Hola soy tu amigo y docente digital Jhonatan mircha, bienvenid@s a mi curso

Agregando mas contenido al _README.md_

Este commit es para oficializar nuestra version *1.0.0*

el enlace de la rama git pages creada ==> https://diegotvramos.github.io/youtube-git/ 

Quieres dominar el uso de _git_?

Mira este [enlace](https://jonmircha.com/git)

![flujo de Git](git-flow.png)


<h2>algunos comandos básicos de la terminal para el manejo de carpetas en sistemas basados en Unix (como Linux o macOS) y también en la línea de comandos de Windows:</h2>

pwd (Print Working Directory):
Muestra la ruta completa del directorio actual.
> `*pwd*`

ls (List):
Lista los archivos y carpetas en el directorio actual.
> `ls`

cd (Change Directory):
Cambia el directorio actual.
> `cd ruta/del/directorio`

mkdir (Make Directory):
Crea un nuevo directorio.
> `mkdir nombre_del_directorio`

rmdir (Remove Directory):
Elimina un directorio vacío.
> `rmdir nombre_del_directorio`

rm (Remove):
Elimina archivos o directorios.
> `rm nombre_del_archivo`

eliminar directorio y su contenido
> `rm -r nombre_del_directorio`

cp (Copy):
Copia archivos o directorios.
> `cp origen.txt destino/`

copiar directorio y su contenido
> `cp -r origen/ destino/`

mv (Move):
Mueve archivos o directorios.
> `mv archivo.txt destino/`
> `mv directorio/ destino/`

_*Cambiar al directorio superior:*_
> `cd ..`

Volver al directorio de inicio:
> `cd ~`

Listar detalles (incluyendo archivos ocultos):
> `ls -la`

<br>
---
___
***
__________________________________________________________________________________________________________
**********************************************************************************************************

<H2>CREANDO PROYECTO DESDE CERO 0</H2>
creamos una carpeta en el escritorio.
abrimos la terminal en ese directorio y creamos los siguientes archivos.

- > `*touch README.md*`
- > `*touch .gitignore*`
<br>

- > `git init`
- > `git add .`
- > `git commit -m "first commit"`
- > `git branch -M main`
- > `git remote add origin https://github.com/diegotvramos/******.git`
- > `git push -u origin main`

_despues es rutinario hacer esto cuando quieras guardar un commit:_
- > `git add .`
- > `git commit -m "Descripcion"`
- > `git push`


<H2>EN CASO DE QUE YA TENGAS UN PROYECTO ABIERTO EN 2 O MAS PCS</H2>

_ANTES DE INICIAR LA PROGRAMACION ASEGURATE DE USAR ESTE COMANDO PARA descargar los cambios del repositorio remoto al local_

- > `git pull` 
- > `git add .`
- > `git commit -m "Descripcion"`
- > `git push` 

<h2>EN CASO DE QUE QUIERAS CLONAR UN REPOSITORIO EN TU PC LOCAL</h2>

- > `git clone https://github.com/usuario/repositorio.git`


