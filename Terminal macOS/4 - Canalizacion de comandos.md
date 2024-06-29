# Canalizando Comandos

En Unix/Linux, la canalización de comandos es una técnica poderosa que permite conectar la salida de un comando directamente a la entrada de otro. Esto es útil para procesar datos de manera eficiente y construir flujos de trabajo complejos a partir de comandos simples.

| Tecla / Comando              | Descripción                                                                                         |
| ---------------------        | -----------------------------------------------------------------------------------------------     |
| `[command-a] \| [command-b]` | Ejecutar el comando A y luego pasar el resultado al comando B, por ejemplo, `ps aux \| grep google` |

## Buenas prácticas

1. **Entender el flujo de datos**:
    - La canalización (`|`) toma la salida estándar (stdout) de `command-a` y la pasa como entrada estándar (stdin) a `command-b`.

2. **Usar comandos especializados para manipular datos**:
    - Comandos como `grep`, `awk`, `sed`, `sort`, y `cut` son ideales para usar en una cadena de canalización. Ejemplo: `cat file.txt | grep "search term" | sort`.

3. **Combinar múltiples comandos en una canalización**:
    - Puedes encadenar múltiples comandos usando canalización para realizar operaciones complejas en un solo paso. Ejemplo: `ps aux | grep httpd | awk '{print $2}' | xargs kill`.

4. **Gestionar la salida de errores**:
    - Para incluir errores en la canalización, redirige `stderr` a `stdout` usando `2>&1`. Ejemplo: `command-a 2>&1 | command-b`.

5. **Evitar el uso excesivo de canalizaciones**:
    - Aunque la canalización es poderosa, un uso excesivo puede complicar la depuración. Mantén las canalizaciones claras y comprensibles.

6. **Optimizar el rendimiento**:
    - Algunos comandos tienen opciones que permiten realizar operaciones internamente sin necesidad de canalización adicional, lo que puede mejorar el rendimiento. Ejemplo: `grep -c "pattern" file` en lugar de `grep "pattern" file | wc -l`.

7. **Probar en pasos**:
    - Cuando crees una cadena de canalización compleja, prueba cada paso individualmente para asegurarte de que produce la salida esperada antes de combinarlos.

8. **Documentar comandos complejos**:
    - Añade comentarios o documentación sobre canalizaciones complejas para facilitar su comprensión y mantenimiento en el futuro.
