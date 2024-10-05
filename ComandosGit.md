# Subir archivos a GitHub usando HTTP desde la consola en Android Studio

## Configura tu nombre de usuario y correo electrónico
Si no lo has hecho antes, configura tu nombre de usuario y correo electrónico para Git.

```bash
git config --global user.name "TuNombre"
git config --global user.email "TuCorreo@example.com"
```

## Clona tu repositorio desde GitHub
Si ya tienes un repositorio en GitHub, clónalo con el siguiente comando.

```bash
git clone https://github.com/TuUsuario/TuRepositorio.git
```

## Navega a la carpeta de tu repositorio local

```bash
cd TuRepositorio
```

## Agrega los archivos que deseas subir al repositorio

Si los archivos ya están en la carpeta, utiliza el siguiente comando para agregar todos los archivos nuevos o modificados:

```bash
git add .
```

O, si quieres agregar un archivo específico:

```bash
git add nombre_del_archivo.ext
```

## Confirma los cambios con un mensaje de commit

```bash
git commit -m "Descripción de los cambios que realizaste"
```

## Sube los cambios a GitHub

Si es la primera vez que subes archivos, usa:

```bash
git push https://github.com/TuUsuario/TuRepositorio.git main
```

Si ya lo has configurado previamente, simplemente usa:

```bash
git push origin main
```

> **Nota**: GitHub podría solicitarte tus credenciales. Desde 2021, GitHub ya no acepta la autenticación por contraseña, por lo que necesitarás usar un **token de acceso personal** en lugar de la contraseña.

---

## Cómo usar el token de acceso personal en Android Studio

1. **Genera un token en GitHub:**
   - Ve a [GitHub Settings](https://github.com/settings/tokens).
   - Genera un nuevo token de acceso personal, asegurándote de seleccionar los permisos necesarios, como `repo` para poder gestionar repositorios.

2. **Usa el token en la consola de Android Studio:**
   - Abre la terminal dentro de Android Studio (`View` > `Tool Windows` > `Terminal`).
   - Realiza el `git push` como de costumbre:

   ```bash
   git push origin main
   ```

   - Cuando Git te pida el nombre de usuario, ingresa tu nombre de usuario de GitHub.
   - Cuando te pida la contraseña, en lugar de ingresar tu contraseña de GitHub, **pega el token de acceso personal** generado anteriormente.

> **Nota**: Copia el token desde GitHub y pégalo cuando te solicite la contraseña en la consola.

---

## Almacenar el token para no tener que ingresarlo siempre

Si no quieres ingresar el token cada vez que hagas un `git push`, puedes configurar Git para que almacene las credenciales.

### Almacenar las credenciales temporalmente (durante una sesión):

```bash
git config --global credential.helper cache
```

### Almacenar las credenciales permanentemente:

```bash
git config --global credential.helper store
```

---

¡Con estos pasos deberías poder subir tus archivos a GitHub desde Android Studio utilizando la consola!
