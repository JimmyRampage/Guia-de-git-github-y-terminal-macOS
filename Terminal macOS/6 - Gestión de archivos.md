# Comandos para la gestión de archivos

La gestión de archivos es fundamental en la terminal de Unix/Linux que permite a los usuarios crear, mover, copiar y eliminar archivos de manera eficiente. Esta tabla proporciona una lista de comandos esenciales para la gestión de archivos, junto con algunas buenas prácticas para garantizar un manejo seguro y eficiente de los datos.

| Tecla / Comando          | Descripción                                                                            |
| ------------------------ | -------------------------------------------------------------------------------------- |
| `touch [file]`           | Crear un nuevo archivo                                                                 |
| `pwd`                    | Ruta completa del directorio actual                                                    |
| `.`                      | Carpeta actual, por ejemplo `ls .`                                                     |
| `..`                     | Carpeta anterior, por ejemplo `ls ..`                                                  |
| `ls -l ..`               | Listado largo de archivos de la carpeta anterior                                       |
| `cd ../../`              | Mover 2 niveles hacia arriba                                                           |
| `cat [file]`             | Mostrar en pantalla el contenido de un archivo                                         |
| `rm [file]`              | Eliminar un archivo, por ejemplo `rm data.tmp`                                         |
| `rm -i [file]`           | Eliminar un archivo con solicitud de confirmación                                      |
| `rm -r [dir]`            | Eliminar un directorio y su contenido                                                  |
| `rm -f [file]`           | Forzar la eliminación de un archivo sin solicitar confirmación                         |
| `cp [file] [newfile]`    | Copiar `file` a `newfile`                                                              |
| `cp [file] [dir]`        | Copiar el archivo al directorio                                                        |
| `mv [file] [newfile]`    | Mover / Renombrar un archivo, por ejemplo `mv file1.ad /tmp`                           |
| `pbcopy < [file]`        | Copiar el contenido del archivo al portapapeles (macOS)                                |
| `pbpaste`                | Pegar contenido del portapapeles (macOS)                                               |
| `pbpaste > [file]`       | Pegar el contenido del portapapeles en un archivo (macOS)                              |

## Buenas prácticas

1. **Verificar antes de eliminar**:
    - Utiliza `rm -i` para que te solicite confirmación antes de eliminar archivos importantes, evitando borrados accidentales.

2. **Hacer copias de seguridad**:
    - Antes de realizar operaciones destructivas como `rm -r`, asegúrate de tener copias de seguridad de los archivos o directorios importantes.

3. **Usar permisos adecuados**:
    - Ajusta los permisos de archivos y directorios usando `chmod` para proteger datos sensibles y evitar modificaciones no autorizadas.

4. **Organizar archivos y directorios**:
    - Mantén una estructura clara y lógica para tus archivos y directorios, facilitando la navegación y gestión de los mismos.

5. **Utilizar `mv` con precaución**:
    - Al renombrar o mover archivos con `mv`, asegúrate de no sobrescribir archivos importantes. Usa la opción `-i` para solicitar confirmación antes de sobrescribir.

6. **Revisar contenido con `cat`**:
    - Antes de editar o eliminar archivos, revisa su contenido usando `cat` para asegurarte de que estás manipulando el archivo correcto.

7. **Automatizar tareas repetitivas**:
    - Usa scripts de shell para automatizar tareas repetitivas de gestión de archivos, mejorando la eficiencia y reduciendo errores manuales.

8. **Aprovechar el portapapeles en macOS**:
    - Utiliza `pbcopy` y `pbpaste` en macOS para copiar y pegar contenidos entre archivos y portapapeles, agilizando la manipulación de datos.

9. **Limitar el uso de `rm -f`**:
    - Evita usar `rm -f` a menos que sea absolutamente necesario, ya que fuerza la eliminación sin confirmación, lo que puede resultar en pérdida de datos accidental.

10. **Revisar rutas con `pwd`**:
    - Antes de ejecutar comandos destructivos, verifica tu ubicación actual en el sistema de archivos con `pwd` para asegurarte de estar en el directorio correcto.
