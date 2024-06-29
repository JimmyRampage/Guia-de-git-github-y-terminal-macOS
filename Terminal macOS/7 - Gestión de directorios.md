# Comandos para la gestión de directorios

La gestión de directorios es importante en Unix/Linux ya que permite a los usuarios organizar, crear y eliminar directorios de manera eficiente. Además, los redireccionamientos de entrada y salida son esenciales para controlar dónde se envía la salida de los comandos y de dónde se leen las entradas. Esta tabla proporciona una lista de comandos esenciales para la gestión de directorios y el uso de redireccionamientos, junto con algunas buenas prácticas para garantizar un manejo seguro y eficiente de los datos.

| Tecla / Comando        | Descripción                                                                    |
| ---------------------- | ---------------------------------------------------------------------------    |
| `mkdir [dir]`          | Crear un nuevo directorio                                                      |
| `mkdir -p [dir]/[dir]` | Crear directorios anidados                                                     |
| `rmdir [dir]`          | Eliminar un directorio (solo funciona en directorios vacíos)                   |
| `rm -R [dir]`          | Eliminar el directorio y su contenido                                          |
| `less [file]`          | Mostrar el contenido del archivo entregado en trozos de tamaño de pantalla     |
| `[command] > [file]`   | Enviar la salida del comando al archivo (sobrescribe el contenido del archivo) |
| `[command] >> [file]`  | Añadir la salida del comando al archivo existente                              |
| `[command] < [file]`   | Indicar al comando que lea el contenido de un archivo                          |

## Buenas prácticas

1. **Verificar antes de eliminar directorios**:
    - Utiliza `rmdir` para eliminar solo directorios vacíos y `rm -R` con precaución para evitar la eliminación accidental de directorios con contenido importante.

2. **Crear directorios anidados de manera segura**:
    - Usa `mkdir -p` para crear estructuras de directorios anidados sin errores si los directorios intermedios ya existen.

3. **Revisar contenidos antes de eliminar**:
    - Antes de eliminar un directorio con `rm -R`, revisa su contenido para asegurarte de que no estás eliminando archivos importantes.

4. **Usar `less` para archivos grandes**:
    - Utiliza `less` en lugar de `cat` para revisar archivos grandes, ya que permite desplazarse por el contenido sin cargar todo el archivo en la memoria.

5. **Redireccionar salidas con precaución**:
    - Cuando uses `>` para redireccionar la salida a un archivo, asegúrate de que está bien sobrescribir el archivo. Usa `>>` para añadir contenido sin sobrescribir.

6. **Documentar comandos importantes**:
    - Mantén una lista de comandos críticos y sus efectos, especialmente los que pueden modificar o eliminar datos, para referencia y evitar errores.

7. **Automatizar tareas repetitivas**:
    - Usa scripts de shell para automatizar la creación y gestión de directorios y redireccionamientos, mejorando la eficiencia y reduciendo errores manuales.

8. **Revisar permisos**:
    - Asegúrate de tener los permisos adecuados para crear o eliminar directorios y archivos, y ajusta los permisos con `chmod` si es necesario.

9. **Realizar copias de seguridad**:
    - Antes de realizar operaciones destructivas como `rm -R`, haz copias de seguridad de los datos importantes.

10. **Utilizar redireccionamientos de entrada con scripts**:
    - Usa `[command] < [file]` para alimentar comandos con datos desde archivos, facilitando la automatización y gestión de tareas repetitivas.
