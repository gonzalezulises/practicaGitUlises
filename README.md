# Práctica Git & GitHub //Ulises Gonzalez
Se deberá crear un repositorio y realizar una serie de operaciones desde la consola de comandos sobre el mismo para posteriormente subir el repositorio a Github. Se deberá entregar a través del formulario de prácticas indicando la URL del repositorio.
En el repositorio, deberá existir un archivo readme.md con las respuestas a las siguientes preguntas:

## Respuestas a las Preguntas

### Paso 11) 

**Comando utilizado:**
```bash
git reset --hard HEAD~1
```

**Razón:**
- `git reset --hard` descarta todos los cambios en el working copy y en el staging area.
- `HEAD~1` indica el commit anterior al último.

### Paso 12) 

**Comandos utilizados:**
1. **Encontrar el hash del commit deshecho:**
   ```bash
   git reflog
   ```
2. **Rehacer el commit:**
   ```bash
   git checkout <hash_del_commit>
   ```
3. **Crear un nuevo commit con los mismos cambios:**
   ```bash
   git add git-nuestro.md
   git commit -c ORIG_HEAD
   ```

**Razón:**
- `git reflog` muestra el historial de cambios, incluyendo commits que han sido deshechos.
- `git checkout <hash_del_commit>` cambia al commit deshecho.
- `git add git-nuestro.md` añade el archivo al staging area.
- `git commit -c ORIG_HEAD` crea un nuevo commit con el mensaje del commit original.

### Paso 13) 

**Comando utilizado:**
```bash
git merge main
```

**Razón:**
- `git merge main` combina los cambios de la rama `main` en la rama `styled`.
- Si no hay conflictos, Git realiza un merge fast-forward.

### Paso 19) 

**Comando utilizado:**
```bash
git merge htmlify
```

**Razón:**
- `git merge htmlify` combina los cambios de la rama `htmlify` en la rama `styled`.
- Si no hay conflictos, Git realiza un merge fast-forward.

### Paso 21) 

**Comando utilizado:**
```bash
git merge styled
```

**Razón:**
- `git merge styled` combina los cambios de la rama `styled` en la rama `main`.
- Si hay conflictos, Git los marca y debe ser resuelto manualmente.

### Paso 25) 

**Comando utilizado:**
```bash
git log --oneline --graph --all
```

**Razón:**
- `git log --oneline --graph --all` muestra un resumen gráfico de todos los commits y ramas.

### Paso 26) 

**Comando utilizado:**
```bash
git merge --no-ff title
```

**Razón:**
- `git merge --no-ff title` fuerza a Git a crear un commit de merge, incluso si es posible hacer un merge fast-forward.

### Paso 27) 

**Comando utilizado:**
```bash
git reset --soft HEAD~1
```

**Razón:**
- `git reset --soft HEAD~1` deshace el último commit pero mantiene los cambios en el staging area.

### Paso 28) 

**Comandos utilizados:**
```bash
git clean -fd
git reset --hard HEAD
```

**Razón:**
- `git clean -fd` elimina archivos no rastreados.
- `git reset --hard HEAD` descarta todos los cambios en el working copy y el staging area.

### Paso 29) 

**Comando utilizado:**
```bash
git branch -d title
```

**Razón:**
- `git branch -d title` elimina la rama `title` si está fusionada con la rama actual.

### Paso 30) 

**Comando utilizado:**
```bash
git merge --no-ff title
```

**Razón:**
- `git merge --no-ff title` vuelve a fusionar la rama `title` en `main` con un commit de merge.

### Paso 32) 

**Comandos utilizados:**
1. **Stashear los cambios:**
   ```bash
   git stash
   ```
2. **Cambiar al commit inicial:**
   ```bash
   git checkout 41dee7b
   ```

**Razón:**
- `git stash` guarda los cambios locales sin hacer un commit.
- `git checkout 41dee7b` cambia al commit inicial sin perder los cambios stasheados.

### Paso 33) 

**Comandos utilizados:**
1. **Volver al último commit en `main`:**
   ```bash
   git checkout main
   ```
2. **Aplicar los cambios stasheados:**
   ```bash
   git stash apply
   ```

**Razón:**
- `git checkout main` cambia a la rama `main`.
- `git stash apply` aplica los cambios stasheados al working copy sin eliminar el stash.

- Para el desarrollo de la práctica utilicé:
* consola: warp v0.2025.01.15.08.02.stable_03
* soporte de IA: Venice AI - Safari 18.2 (20620.1.16.11.8)
* formato de markdown: chatGPT
