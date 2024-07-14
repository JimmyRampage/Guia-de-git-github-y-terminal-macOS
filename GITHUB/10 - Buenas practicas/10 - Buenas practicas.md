# Buenas practicas

* agregar un .gitignore
* configurar username
* configurar email

* branch
  * cada rama es creada para un objetivo
  * una rama soluciona un problema
  * objetivo cumplido, rama fusionada, limpiada y eliminada
  * nombres descriptivo
  * kebab-case
  * no trabajar en la rama main
  * Estrategias de branch

    * merge: conserva todos los commits en tu rama e intercala los commits con los de la rama base. Es la práctica más común seguida por los desarrolladores ya que es simple y fácil de entender. Sin embargo, el historial puede volverse confuso con commits dummy y la depuración usando `git bisect` puede ser más difícil, especialmente si la rama Master es muy activa.

    * squash: conserva los cambios pero omite los commits individuales del historial. Actúa como merge pero crea un nuevo commit squashed que engloba todos los commits en la rama de la característica. Los merges más grandes y difíciles pueden ser complicados de hacer con un squash y merge.

    * rebase: mueve toda la rama de la característica para comenzar en la punta de la rama Master, incorporando efectivamente todos los nuevos commits en Master. Cuando haces rebase, rebobina tus commits y vuelve a reproducir esos commits desde la punta de la rama Master. Esto resulta de dos cambios principales. Dado que tus commits ahora se ramifican desde un nodo padre diferente, sus hashes se recalcularán, y cualquiera que haya clonado tu repositorio puede tener ahora una copia rota del repositorio. Por lo tanto, no se sugiere usar rebase para actualizar tu rama de características si se comparte con otros miembros del equipo.

* Commits

  * commits significativos

    * no son como checkpoints para ir a hacer otras cosas
    * se hacen de manera atomica pero significativos
    * cambios a nivel micro

  * no se dejan cambios a medias

* git pull seguidos
* uso de tags
