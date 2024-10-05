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

### 3. Añadir la clave privada al agente id_rsa es un nombre por defecto, debe ser reemplazado por el nombre con el cual se guardo la clave
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
