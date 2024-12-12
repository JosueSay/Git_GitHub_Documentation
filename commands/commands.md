# 🛠️ Guía de Comandos en la Terminal 🛠️

## Configuración de Git :octocat:

Para configurar tu nombre y correo en Git:

```bash
git config user.name "JosueSay"
git config user.email "josuesay770@gmail.com"
git config --global user.name "JosueSay"
git config --global user.email "josuesay770@gmail.com"
```

## Crear Rama :evergreen_tree:

Para crear una nueva rama y cambiar a ella:

```bash
git checkout -b backend
```

## Hacer Fusión :twisted_rightwards_arrows:

Para fusionar una rama en la rama actual:

```bash
git merge nueva-caracteristica
```

## Saber el Enlace del Repositorio :globe_with_meridians:

Para ver el enlace remoto del repositorio:

```bash
git remote -v
```

## Documentación :memo:

Tipos de mensajes de commit:

- `feat:` Para nuevas características o funcionalidades.
- `fix:` Para correcciones de errores.
- `docs:` Para cambios relacionados con la documentación.
- `style:` Para cambios que no afectan al funcionamiento del código (como cambios en el formato, espaciado, etc.).
- `refactor:` Para cambios en el código que no corrigen errores ni agregan nuevas funcionalidades, pero mejoran su estructura o legibilidad.
- `test:` Para la adición o modificación de pruebas.
- `chore:` Para tareas de mantenimiento o cambios en la configuración del proyecto.

## Restaurar Archivo :recycle:

Para restaurar un archivo al último commit:

```bash
git restore archivo
```

## Hacer merge

Cambiar de rama:

```bash
git checkout rama_donde_se_hara_merge
```

Asegurar en que rama se cambio:

```bash
git branch
```

Hacer merge de toda la rama:

```bash
git merge rama_a_traer_codigo
```

Hacer merge de una ruta o carpeta:

```bash
git checkout rama_traer_codigo -- ruta/especifica
```

## Abortar merge

```bash
git merge --abort
```

## Ver los cambios que se harán antes de merge

En caso de que no hay carpetas con el nombre de la rama

```bash
git diff rama_recibe_codigo rama_que_manda_codigo
```

En caso de que hay carpetas con el nombre de la misma rama

```bash
git diff rama_recibe_codigo...rama_que_manda_codigo
```

## Clonación de Repositorios por SSH :electric_plug:

Para clonar un repositorio usando SSH, sigue estos pasos según tu rol:

### Para Colaboradores

1. **Genera un par de llaves SSH**: Si aún no tienes un par de llaves SSH, debes generarlo.

2. **Verifica la conexión**: Confirma que tu clave SSH funciona correctamente ejecutando el siguiente comando:

   ```bash
   ssh -T git@servidor.com
   ```

   Si la configuración es correcta, deberías recibir un mensaje de bienvenida o una notificación de autenticación exitosa.

3. **Clona el repositorio**: Usa el siguiente comando para clonar el repositorio en tu máquina local:

   ```bash
   git clone git@servidor.com:/ruta/del/repositorio.git
   ```

### Para Propietarios

1. **Configura el acceso a tu repositorio**: Asegúrate de haber añadido las claves públicas de tus colaboradores en la configuración del repositorio en el servidor o proveedor. Esto es esencial para que ellos puedan acceder al repositorio.

## Configuración de SSH para Múltiples Claves :key:

Si trabajas con múltiples claves SSH y quieres especificar cuál usar para un repositorio específico, sigue estos pasos:

### 1. **Editar el archivo de configuración de SSH**

- Abre o crea el archivo `~/.ssh/config`:

```bash
nano ~/.ssh/config
```

### 2. **Agregar una configuración personalizada**

Añade una entrada para especificar la clave privada que se usará para un servidor o repositorio específico:

```ssh
Host github.com
   HostName github.com
   User git
   IdentityFile ~/.ssh/key_git
```

### 3. **Explicación de los campos**

- **Host**: Un alias o nombre para identificar al servidor.
- **HostName**: El nombre real del servidor.
- **User**: El usuario con el que se conecta (por lo general, `git`).
- **IdentityFile**: La ruta a la clave privada que se usará.

### 4. **Permisos de la clave privada**

Asegúrate de que la clave privada tenga los permisos correctos:

```bash
chmod 600 ~/.ssh/key_git
```

### 5. **Probar la conexión**

Puedes verificar la conexión con:

```bash
ssh -T git@servidor.com
```

## Staging

Para sacar un archivo de la etapa de staging

```bash
git rm --cached <file>
```

## Eliminación de ramas

### 1. Eliminar una rama local

Elimina la rama local especificada de forma forzada, incluso si no ha sido fusionada.

```bash
git branch -D <branch>
```  

### 2. Eliminar una rama remota

Elimina la rama remota especificada en el repositorio remoto.

```bash
git push origin --delete <branch>
```  

### 3. Eliminar una rama remota localmente

Elimina las ramas remotas que ya no existen en el repositorio remoto.

```bash
git fetch -p
```

### 4. Eliminar una rama localmente sin forzar  

Elimina una rama local solo si ha sido completamente fusionada con la rama principal.

```bash
git branch -d <branch>
```  

## Unificar historiales de un entorno local y remoto

Este comando se utiliza para unificar historiales en caso de conflicto con repositorios locales y un remoto.

```bash
git pull origin main --allow-unrelated-histories
```
