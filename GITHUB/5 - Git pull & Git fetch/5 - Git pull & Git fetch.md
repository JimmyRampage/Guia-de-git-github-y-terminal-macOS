# Git pull & Git fetch

* `git pull` es un comando de Git que se utiliza para actualizar tu repositorio local con los cambios de un repositorio remoto. Este comando combina dos operaciones: git fetch (para descargar los datos del remoto) y git merge (para fusionar esos datos en tu rama actual).

* `git fetch` es un comando de Git que se utiliza para descargar los datos (commits, archivos y referencias) de un repositorio remoto sin fusionarlos automáticamente en tu rama actual. Este comando actualiza tu vista de las ramas remotas en tu repositorio local, permitiéndote ver los cambios antes de fusionarlos.

## Creamos un código en el repositorio desde GitHub

![alt text](img/img_1.png)

### Hacemos commit changes

![alt text](img/img_2.png)

![alt text](img/img_3.png)

### Utilizamos git pull para actualizar todo

![alt text](img/img_4.png)

## Git fetch

>No cambia las ramas locales automáticamente

### Hacemos cambios en github, eliminamos codigo2.py y hacemos commit

![alt text](img/img_5.png)

![alt text](img/img_6.png)

### Ahora editamos codigo.py

![alt text](img/img_7.png)
