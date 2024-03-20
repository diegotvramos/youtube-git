# Curso de _Git_ & _GitHub_

Hola soy tu amigo y docente digital Jhonatan mircha, bienvenid@s a mi curso

Agregando mas contenido al _README.md_

Este commit es para oficializar nuestra version *1.0.0*

el enlace de la rama git pages creada ==> https://diegotvramos.github.io/youtube-git/ 

Quieres dominar el uso de _git_?

Mira este [enlace](https://jonmircha.com/git)

![flujo de Git](git-flow.png)


**algunos comandos básicos de la terminal para el manejo de carpetas en sistemas basados en Unix (como Linux o macOS) y también en la línea de comandos de Windows:**

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

***

## CREANDO PROYECTO DESDE CERO 0

creamos una carpeta en el escritorio.
abrimos la terminal en ese directorio y creamos los siguientes archivos.


- > `touch README.md`
- > `touch .gitignore`   


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

---

## SUBIENDO A LA RAMA GH-PAGES

**gh-pages** es una rama especial para crear un sitio web a tu proyecto alojado directamente en tu repositorio de GitHub.

>- URL del repositorio: https://github.com/usuario/repositorio
>- URL del sitio: https://usuario.github.io/repositorio
> _**Aclaracion** ya debemos tener un repositorio en GitHub.  ``git remote add origin https://github.com/usuario/repositorio.git``_



_podemos colocar un link que nos redirija a la pagina `gh-pages`_

- > `[link](https://diegotvramos.github.io/nombre-del-proyecto/)`


Para crear esta rama especial en GitHub ejecutamos los siguientes comandos:

> Nota _estando en la rama **MAIN** hacemos los comandos rutinarios._

- > `git add .`
- > `git commit -m "Descripcion"`
- > `git push`

### Creamos por primera y unica vez la rama con el nombre:  `gh-pages`.

- > `git branch gh-pages`
- > `git checkout gh-pages`

_las dos lineas de comandos anteriores se puede **simplificar** en la siguiente linea, (b) crear una rama y (checkout)cambiarte a ella_
    
- > `git checkout -b gh-pages`

_lo subimos a nuestra rama remota_

- > `git push origin gh-pages`

_para descargar los cambios del repositorio remoto al local_

- > `git pull origin gh-pages`

 _volvemos a nuestra rama MAIN_

- > `git checkout main`


### Cuando realizamos cambios y queremos que esos cambios se vean en la rama gh-pages

_estando en la rama `MAIN` hacemos todo los cambios que querramos._

- > `git checkout main`

_Hacemos los cambios a los archivos. y al final hacemos los comandos rutinarios._

- > `git add .`
- > `git commit -m "Descripcion"`
- > `git push`

**Me posiciono en la rama gh-pages** porque lo vamos a fusionar.

1. situarnos en la rama que se quedará con el **contenido** fusionado, en este caso `gh-pages`

- > `git checkout gh-pages`

2. Ejecutamos el comando `Merge` con la rama a fusionar

- > `git merge main`

_Si se fusionó, pero esta fusion se dio en mi maquina local, lo que falta es subirla al la rama gh-pages del repositorio_

> **Nota** no es necesario agregar `git add .` o `git commit -m ""`

- > `git push origin gh-pages`

 _Volvemos a nuestra rama **MAIN**_

- > `git checkout main`

> **Nota** Observar siempre la rama en la que nos encontremos, para que podamos subir y acualizar sin incomvenientes.


### Reemplazando la Rama Master por Main (en repositorios existentes)

Primero ejecutamos los comandos rutinarios.

- > ``git add .``
- > ``git commit -m "Second commit"``
- > ``git push``

ahora realizamos los siguientes pasos 
1. Crea la rama local main y pásale el historial de la rama master.
2. Haz un push de la nueva rama local main en el repositorio remoto de GitHub.
3. Cambia el HEAD actual a la rama main.
4. Cambia la rama default de master a main en tu repositorio de GitHub . 
5. Elimina la rama master del repositorio remoto.

- > `git branch -m master main`
- > `git push -u origin main`
- > `git symbolic-ref refs/remotes/origin/HEAD refs/remotes/origin/main`
- > [enlace](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-branches-in-your-repository/changing-the-default-branch)
- > `git push origin --delete master`
