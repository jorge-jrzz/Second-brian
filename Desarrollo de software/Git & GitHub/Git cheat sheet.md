---
banner_icon: 🐙
banner: "![[earth-and-moon-by-osiris-rex_23544781998_o.jpg]]"
banner_y: 0.064
---


# Git Cheat Sheet

### <mark class="hltr-purple">Configuración inicial</mark>

para la configuración inicial de Git en e nuestro dispositivo debemos seguir los siguientes pasos expuestos en la siguiente pagina: [[Configuracion]]. 

### <mark class="hltr-purple">Comando básicos </mark>

- **Inicializar repositorio**: Crea un nuevo repositorio Git.
```bash
git init
```

- **Clonar repositorio**: Clona un repositorio existente en tu directorio actual.
```bash
git clone <url_repositorio>
```

+ **Muestra el estatus del repositorio:** Muestra los archivos modificados en el directorio de trabajo, preparado para si próxima corfirmación.
```bash
git status
```

- **Agregar cambios**: Agrega los cambios al área de preparación (stage) para un commit.
```bash
git add <archivo(s)>
```

- **Realizar commit**: Crea un nuevo commit con los cambios agregados.
```bash
git commit -m "mensaje_del_commit"
```

- **Actualizar y fusionar**: Actualiza tu repositorio local y fusiona los cambios del repositorio remoto.
```bash
git pull origin <rama>
```

- **Enviar cambios**: Envía tus commits locales al repositorio remoto.
```bash
git push origin <rama>
```

### <mark class="hltr-purple">Ramas</mark>

- **Listar ramas**: Muestra una lista con las ramas del repositorio.
```bash
git branch
```

- **Crear rama**: Crea una nueva rama en el repositorio.
```bash
git branch <nombre_rama>
```

- **Cambiar de rama**: Cambia a una rama específica.
```bash
git checkout <nombre_rama>
```

- **Fusionar ramas**: Fusiona una rama con la rama actual.
```bash
git merge <nombre_rama>
```

- **Eliminar rama**: Elimina una rama específica del repositorio.
```bash
git branch -d <nombre_rama>
```

### <mark class="hltr-purple">Compartir y actualizar</mark>

- **Agregar repositorio remoto**: Agrega un repositorio remoto con un nombre específico.
```bash
git remote add <nombre_remoto> <url_repositorio>
```

- **Obtener cambios del repositorio remoto**: Descarga los cambios del repositorio remoto sin fusionarlos.
```bash
git fetch <nombre_remoto>
```


### <mark class="hltr-purple">Control de cambios</mark>

- **Ver cambios**: Muestra los cambios realizados en los archivos modificados.
```bash
git diff
```

- **Historial de commits**: Muestra el historial de commits del repositorio.
```bash
git log
```

- **Mostrar resumen de commits**: Muestra un resumen de los cambios en los commits, incluyendo estadísticas de archivos renombrados.
```bash
git log --stat -M
```

- **Ver detalles de un commit**: Muestra los detalles y los cambios de un commit específico.
```bash
git show <hash_commit>
```

- **Deshacer cambios**: Descarta los cambios realizados en un archivo específico.
```bash
git checkout -- <archivo>
```

- **Eliminar archivo**: Elimina un archivo del repositorio y del directorio de trabajo.
```bash
git rm <archivo>
```

- **Mover o renombrar archivo**: Mueve o cambia el nombre de un archivo en el repositorio.
```bash
git mv <nombre_archivo_actual> <nuevo_nombre_archivo>
```

- **Revertir commit**: Revierte un commit específico y crea un nuevo commit de reversión.
```bash
git revert <hash_commit>
```

- **Restablecer cambios**: Deshace los cambios en el área de preparación (stage) y en el directorio de trabajo.
```bash
git reset <archivo>
```

- **Rebase**: Aplica los commits de una rama en la punta de otra rama.
```bash
git rebase <rama_destino>
```

### <mark class="hltr-purple">Commits temporales</mark>

- **Guardar cambios**: Guarda los cambios en un commit temporal.
```bash
git stash save "nombre_del_stash"
```

- **Listar cambios guardados**: Muestra una lista de los cambios guardados en los stashes.
```bash
git stash list
```

- **Aplicar cambios**: Aplica los cambios de un stash específico al directorio de trabajo.
```bash
git stash apply <stash>
```

- **Aplicar y eliminar cambios**: Aplica los cambios de un stash específico y lo elimina de la lista de stashes.
```bash
git stash pop <stash>
```

- **Eliminar cambios guardados**: Elimina un stash específico de la lista de stashes.
```bash
git stash drop <stash>
```

- **Limpiar stashes**: Elimina todos los stashes guardados.
```bash
git stash clear
```

Los comandos anteriores te permitirán guardar temporalmente los cambios en un stash, aplicarlos cuando sea necesario y gestionar tus stashes de manera efectiva. Recuerda que los stashes son útiles cuando necesitas cambiar de tarea rápidamente y quieres guardar tus cambios en un estado temporal antes de trabajar en otra cosa.
