# SSH and GPG Keys

Las SSH keys y los Personal Access Tokens (PATs) son dos métodos diferentes que se utilizan para la autenticación en GitHub, y cada uno tiene sus propios usos y ventajas.

## SSH Keys

* Las SSH keys se utilizan para establecer una conexión segura entre tu ordenador y GitHub.
* Permiten el acceso de lectura y escritura a tus repositorios.
* Son útiles cuando quieres evitar introducir tu contraseña regularmente.
* Sin embargo, las SSH keys no tienen permisos limitados.

## Personal Access Tokens (PATs)

* Los PATs son similares a las SSH keys, pero tienen más restricciones.
* Pueden tener permisos limitados, lo que significa que puedes controlar a qué partes de tu cuenta de GitHub puede acceder un token.
* Esto es útil, por ejemplo, cuando quieres permitir que aplicaciones de terceros accedan a tus repositorios con restricciones.
* GitHub recomienda tokens sobre SSH keys debido a su modelo de permisos más detallado.

## Pasos para configurar SSH

### Abrir desde github

1. Settings
2. SSH and GPG keys
3. New SSH key
4. ->Abrir terminal / [Documentación GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

    1. —> ssh-keygen -t rsa -b 4096 -C “mi-llave-ssh”
    2. ——> enter x 3
    3. ——> Esto generara una llave
    4. —> cat ~/.ssh/id_rsa.pub  (esto nos mostrara la llave publica)
    5. —> ssh -T <git@github.com> (comprobando el enlace)
