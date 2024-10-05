
# Git Commands Cheat Sheet

## Configuración inicial

### Configurar nombre de usuario y correo
```bash
git config --global user.name "TuNombre"
git config --global user.email "TuEmail"
```

### Ver configuración actual
```bash
git config --list
```

## Iniciar y Clonar

### Inicializar un repositorio
```bash
git init
```

### Clonar un repositorio
```bash
git clone https://github.com/usuario/repositorio.git
```

## Trabajar con archivos

### Ver el estado de los archivos
```bash
git status
```

### Añadir archivos al staging area
```bash
git add <archivo>
git add .
```

### Confirmar cambios (commit)
```bash
git commit -m "Mensaje del commit"
```

### Deshacer cambios antes del commit
```bash
git reset <archivo>
git reset .
```

### Deshacer cambios después del commit
```bash
git reset --soft HEAD~1
```

## Ramificación (Branches)

### Crear una nueva rama
```bash
git branch <nombre-rama>
```

### Cambiar a otra rama
```bash
git checkout <nombre-rama>
```

### Crear una nueva rama y cambiar a ella
```bash
git checkout -b <nombre-rama>
```

### Borrar una rama
```bash
git branch -d <nombre-rama>
```

## Fusionar (Merging)

### Fusionar una rama con la actual
```bash
git merge <nombre-rama>
```

### Rebase (reaplicar commits)
```bash
git rebase <rama-base>
```

## Repositorio Remoto

### Añadir un remoto
```bash
git remote add origin https://github.com/usuario/repositorio.git
```

### Ver los remotos
```bash
git remote -v
```

### Subir cambios al remoto
```bash
git push -u origin <rama>
```

### Descargar cambios del remoto
```bash
git pull origin <rama>
```

## Inspección del historial

### Ver historial de commits
```bash
git log
```

### Ver un historial breve
```bash
git log --oneline
```

### Ver diferencias entre archivos
```bash
git diff
```

## Stashing

### Guardar cambios temporalmente
```bash
git stash
```

### Ver stashes
```bash
git stash list
```

### Recuperar cambios de un stash
```bash
git stash apply
```

### Borrar un stash
```bash
git stash drop
```

## Submódulos

### Añadir un submódulo
```bash
git submodule add https://github.com/usuario/repo-submodulo.git
```

### Actualizar un submódulo
```bash
git submodule update --remote
```

## SSH y GitHub

### 1. Generar una clave SSH
```bash
ssh-keygen -t rsa -b 4096 -C "tu_email@example.com"
```
Este comando genera una nueva clave SSH. Usa una frase de contraseña si lo deseas.

### 2. Iniciar el agente SSH
```bash
eval "$(ssh-agent -s)"
```
Este comando inicia el agente SSH en segundo plano.

### 3. Añadir la clave privada al agente
```bash
ssh-add ~/.ssh/id_rsa
```
Añade tu clave privada al agente SSH para que pueda gestionar las conexiones.

### 4. Copiar la clave pública al portapapeles (en Linux)
```bash
cat ~/.ssh/id_rsa.pub | xclip -selection clipboard
```
Esto copia la clave pública al portapapeles para que la puedas agregar a GitHub o cualquier otro servicio.

### 5. Verificar la conexión con GitHub
```bash
ssh -T git@github.com
```
Este comando te ayudará a verificar si la conexión con GitHub a través de SSH funciona correctamente.
