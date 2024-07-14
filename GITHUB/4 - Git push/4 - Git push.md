# Git push

Es un comando de Git que se utiliza para enviar los commits locales a un repositorio remoto. Este comando actualiza la rama remota con los cambios realizados en la rama local. Es esencial para colaborar en proyectos con otros desarrolladores, ya que permite compartir el trabajo y actualizar el repositorio remoto con las últimas modificaciones.

## Haciendo push

Abrimos el proyecto clonado y modificamos el código.py y lo guardamos.

![alt text](<img/Screenshot 2024-05-19 at 19.13.12.png>)

vemos `git status`

![alt text](<img/on branch main.png>)

Utilizamos `git add <file>` y `git commit -m ""`

![alt text](<img/jimmyrampage curso-de-git-y-github $ git commit -m.png>)

### Subiendo al servidor

Revisamos las configuraciones.

![alt text](img/filter-process.png)

>El correo configurado debe ser el mismo que de la cuenta de github.

### `git push origin main`

* origin hace referencia a que quiero realizar un push al repositorio de origen.
* main hace referencia a la rama que estoy subiendo un cambio.

![alt text](<img/jimmyrampage curso-de-git-y-github $ git push origin main.png>)
>Nos solicitara información adicional.
>
>Esto por haber utilizado sistema de HTTPS
>
>El user name: en mi caso es JimmyRampage
>
>El password es un token de seguridad, no es el password de inicio de sesión.

## Para obtener el token

1. Vamos a settings

    ![alt text](<img/James Ovalle.png>)

2. Bajamos hasta <> Developer settings

    ![alt text](img/Security.png)

3. Vamos a personal access tokens -> tokens (classic)

    ![alt text](<img/Personal access tokens.png>)

4. Generamos un token personal

    ![alt text](<img/quick access to the GitHub API..png>)

5. Pasamos esta capa de seguridad

    ![alt text](<img/Signed in as @JimmyRampage.png>)

6. Configuración del token
    * Definimos detalles como una referencia a que es el token
    * Definimos cuando expira el token, (mientras menos días es más seguro)
    * Y también permisos para el token

    ![alt text](img/prueba-de-token-curso-git.png)

7. Generamos el token

    ![alt text](<img/Generate token.png>)

    ![alt text](<img/Personal access tokens (classic).png>)

8. Copiamos y pegamos el token en la terminal

    ![alt text](<img/Username for.png>)

9. Confirmamos el cambio en github (el tiempo de 24minutes ago | se debe a que el commit fue hecho en mi computadora hace 24 minutos)

    ![alt text](<img/curso-de-git-y-github Public.png>)

    ![alt text](<img/JimmyRampage cambiando el name.png>)
