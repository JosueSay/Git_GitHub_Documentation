# 📚 Curso de Git y GitHub

![Banner del Curso](../images/banner.png "Banner Curso Git y GitHub")

**Fecha:** 26/11/2024

**Enlace del Curso:** [Git y GitHub en Platzi](https://platzi.com/cursos/gitgithub/ "Enlace Curso Git y GitHub")

**Profesor:** amin Espinoza

## 🗂 Estructura del Repositorio
```bash
Git & GitHub/
├── commands/               # Carpeta que contiene documentación sobre comandos de Git
│   ├── commands.pdf
│   └── commands.md
├── documentation/          # Carpeta que contiene la documentación completa del curso
│   └── course.md
└── images/                 # Carpeta con las imágenes usadas en course.md
```

## 🔍 Información General

Git es un **controlador de versiones** que permite a los desarrolladores trabajar de forma colaborativa en proyectos de software. Fue creado por **Linus Torvalds** y es **Open Source**.  

Git puede usarse tanto en máquinas locales como en IDEs como **Visual Studio Code**, y ofrece varios eventos importantes como **push**, **pull**, **commits**, entre otros.

## ⚙️ Configuración Inicial

En sistemas **Linux** y **WSL**, **Git** viene preinstalado. Para verificar la versión de Git, ejecuta el siguiente comando:

```bash
git --version
```

Esto debería devolver la versión de Git instalada en tu sistema.

### 🌱 Inicialización de un Repositorio

Para comenzar, utilizaremos esta carpeta para realizar prácticas con **Git** y **GitHub**. Ejecuta el siguiente comando para inicializar un repositorio Git en tu proyecto:

```bash
git init
```

Esto creará una rama por defecto llamada `master`, pero actualmente Git utiliza **`main`** como nombre por defecto para la rama principal. Para cambiar esto, ejecuta el siguiente comando:

```bash
git config --global init.defaultBranch main
```

No obtendrás una respuesta en la terminal, pero este comando hará que **`main`** sea la nueva rama predeterminada al inicializar un repositorio.

Para cambiar el nombre de la rama principal de `master` a `main`, ejecuta:

```bash
git branch -m main
```

### 📜 Documentación de Comandos

Para obtener ayuda sobre los comandos de Git, puedes usar:

```bash
git --help
```

Esto mostrará una guía breve de los comandos disponibles directamente en la terminal.

### 🧑‍💻 Configuración del Usuario

Es importante configurar tu nombre y correo electrónico para que Git registre correctamente quién está realizando los cambios en el repositorio. Ejecuta los siguientes comandos para configurarlos:

```bash
git config --global user.name "Tu Nombre"
```

```bash
git config --global user.email "usuario@correo.com"
```

⚠️ **Nota:** El parámetro **`--global`** aplica esta configuración a todos los repositorios de tu máquina, no solo a este repositorio específico.

### 🧐 Verificación de la Configuración

Para verificar que todo esté configurado correctamente, ejecuta:

```bash
git config --list
```

Esto mostrará todas las configuraciones activas de Git en tu sistema.

## 🛠️ Comandos Básicos

### 📂 Inicialización de Git

En la sección anterior, inicializamos un repositorio de Git con el comando:

```bash
git init
```

Este comando crea una carpeta oculta llamada `.git` en el directorio donde se ejecutó. Para visualizarla, puedes usar el siguiente comando:

```bash
ls -a
```

Este comando muestra todas las carpetas, incluidas las ocultas. Verás la carpeta **`.git`**, que es donde Git almacena un registro detallado de los cambios realizados en los archivos del proyecto.

### 📝 Creando Archivos para la Práctica

1. Crea una carpeta llamada **`practice/`** para almacenar los ejercicios del curso.
2. Dentro de esa carpeta, crea un archivo llamado **`test.txt`** y escribe "Hola Mundo" en él.

Ahora que tienes nuevos archivos y cambios, verifica el estado del repositorio con:

```bash
git status
```

La terminal mostrará algo como esto:

```plaintext
On branch main          # Rama actual

No commits yet          # Aún no se han realizado commits

Untracked files:        # Archivos/carpetas no rastreados
  (use "git add <file>..." to include in what will be committed)
        ../commands/
        ../documentation/
        ../images/
        ./practice/test.txt

                        # Sugerencia de comandos
nothing added to commit but untracked files present (use "git add" to track)
```

### ➕ Añadiendo Archivos al Área de Staging

Para registrar los cambios, utiliza uno de los siguientes comandos:  

- Para añadir **todos los cambios** del directorio:  
  ```bash
  git add .
  ```

- Para añadir un archivo específico:  
  ```bash
  git add <ruta_del_archivo>
  ```

Tras ejecutar estos comandos, verifica nuevamente el estado del repositorio:  

```bash
git status
```

Deberías ver algo similar a esto:

```plaintext
On branch main

No commits yet

Changes to be committed: # Archivos en el área de staging
  (use "git rm --cached <file>..." to unstage)
        new file:   commands/commands.md
        new file:   commands/commands.pdf
        new file:   documentation/course.md
        new file:   images/banner.png
        new file:   practice/test.txt
```

### 🔄 Entendiendo el Área de Staging

El área de **staging** es como un "limbo" donde los archivos esperan a ser confirmados con un commit o descartados.  

#### Opciones:
- **Retirar un archivo del área de staging:**  
  ```bash
  git rm --cached <file>
  ```

- **Confirmar los cambios con un commit:**  
  ```bash
  git commit -m "Mensaje descriptivo"
  ```

### 🔁 Flujo de Trabajo en Git

![Staging](../images/staging.png "Staging")

En el flujo de trabajo típico:  
1. **Directorio de trabajo:** Los archivos se editan aquí.  
2. **Área de staging:** Los cambios se preparan con `git add`.  
3. **Repositorio:** Los cambios se confirman con `git commit`.  

![Flow Git](../images/flow.png "Flow Git")

### 🧾 Verificando el Historial de Cambios

Para revisar el historial de commits y asegurarte de que todo está funcionando correctamente, usa:

```bash
git log
```

Esto mostrará una lista de los commits realizados, con detalles como el autor, la fecha y el mensaje del commit.


## 🌿 Ramas en Git

Las **ramas** se utilizan para trabajar de manera aislada, sin interferir con el trabajo de otros. Esto permite que cada miembro del equipo realice cambios sin afectar el código principal.

![Branch Git](../images/branchs.png "Branch Git")

### 📋 Verificando la Rama Actual

Para ver en qué rama te encuentras, usa el siguiente comando:

```bash
git branch
```

Este comando listará todas las ramas del repositorio, y te indicará con un **asterisco** (`*`) la rama en la que estás trabajando actualmente.

### ➕ Creando una Nueva Rama

Para crear una nueva rama y cambiarte a ella de inmediato, usa:

```bash
git checkout -b nombre_rama
```

Por ejemplo, si creas una rama llamada **`josue`**, el comando será:

```bash
git checkout -b josue
```

Al ejecutar `git branch` después, verás que ahora estás en la rama **`josue`** en lugar de **`main`**.

### 📝 Trabajando en una Rama

Imagina que creas un archivo llamado **`test3.txt`** dentro de la carpeta **`practice/`** y lo añades al repositorio. Este cambio solo afectará a la rama **`josue`** y no se verá en **`main`**. Esto permite que cada rama sea independiente.

Para que los demás integrantes del equipo vean estos cambios, necesitas fusionar la rama **`josue`** con **`main`**. Para ello, primero regresa a la rama **`main`**:

```bash
git checkout main
```

O usa el comando alternativo:

```bash
git switch main
```

### 🔄 Fusionando las Ramas

Una vez en la rama **`main`**, fusiona los cambios de **`josue`** con:

```bash
git merge josue
```

Este comando fusionará las ramas utilizando un **Fast-forward**, lo que significa que los archivos modificados en **`josue`** se añadirán a **`main`** sin crear un commit adicional.

Para asegurarte de que la fusión fue exitosa, puedes revisar el historial de commits con:

```bash
git log
```

Esto te mostrará los commits en la rama **`main`**, asegurándote de que los cambios de **`josue`** se han integrado correctamente.

### 🗑️ Eliminar Ramas Después de Fusionarlas

Una vez que una rama individual haya cumplido su propósito y sus cambios se hayan fusionado con **`main`**, es una buena práctica eliminarla para evitar tener ramas innecesarias. Para eliminar la rama **`josue`**, usa:

```bash
git branch -D josue
```

Esto eliminará la rama **`josue`** de manera segura. El objetivo de las ramas es crearlas con un propósito específico y, una vez cumplido, eliminarlas para evitar conflictos en el futuro.

#### 🔄 Ejemplo de Flujo de Trabajo con Ramas:

1. **Crear una nueva rama**:  
   `git checkout -b josue`
2. **Realizar cambios**:  
   Crear un archivo o modificar archivos.
3. **Añadir los cambios**:  
   `git add .`
4. **Hacer un commit**:  
   `git commit -m "Descripción del cambio"`
5. **Fusionar la rama con `main`**:  
   Cambiar a `main` (`git checkout main`) y hacer el merge (`git merge josue`).
6. **Eliminar la rama**:  
   `git branch -D josue`

## ⏪ Volver en el tiempo (Reset y Revert)

### 🔄 Git Revert

El comando **`git revert`** se utiliza para revertir los cambios de un commit específico y crear un nuevo commit que deshace esos cambios.

1. Primero, consulta el historial de commits con:

   ```bash
   git log
   ```

   En el historial, verás un commit marcado como **(HEAD -> main)**, lo que indica que es el último commit realizado y el puntero actual.

2. Supongamos que creas un archivo llamado **`error.txt`** en la carpeta **`practice/`** y lo subes al repositorio. El commit generado podría ser similar al siguiente:

   ```bash
   commit d36f1ecda1ccee7c29d3d20c095a22b3b6a91c24 (HEAD -> main)
   Author: JosueSay <106031855+JosueSay@users.noreply.github.com>
   Date:   Mon Dec 9 11:35:24 2024 -0600

       ft. archivo especial subido
   ```

3. Si decides que este archivo no debería estar en el repositorio, primero necesitas identificar el commit que lo introdujo, usando su hash (la cadena que aparece después de la palabra **commit**).

4. Luego, ejecuta el siguiente comando para revertir el commit:

   ```bash
   git revert d36f1ecda1ccee7c29d3d20c095a22b3b6a91c24
   ```

   Este comando abrirá un editor de texto donde podrás modificar el mensaje del commit, lo que se recomienda para indicar quién realizó el **revert**.

5. Al ejecutar `git log` nuevamente, verás un nuevo commit que revierte los cambios del commit con el hash indicado. Ten en cuenta que **`git revert` no elimina el commit original**, solo crea un nuevo commit que deshace los cambios realizados en el commit revertido.

6. Para verificar que el archivo **`error.txt`** ha sido eliminado, puedes usar `ls` en la carpeta **`practice`**. Si el archivo ya no aparece, significa que los cambios se han revertido correctamente.

### ⚡ Git Reset

El comando **`git reset`** permite mover el puntero de commits a un estado anterior, deshaciendo los commits posteriores.

1. Para ilustrar esto, creamos un archivo llamado **`reset.txt`** y lo subimos al repositorio. El historial de commits podría verse así:

   ```bash
   commit 08f5e06609bde67cea00bc19e4a464e0f9ee85db (HEAD -> main)
   Author: JosueSay <106031855+JosueSay@users.noreply.github.com>
   Date:   Mon Dec 9 11:48:49 2024 -0600

       Revert "ft. archivo especial subido" por Josué
       
       Correspondiente al commit con hash "d36f1ecda1ccee7c29d3d20c095a22b3b6a91c24"

   commit c4e383c481c883768a63ef093354b53245212e3f
   Author: JosueSay <106031855+JosueSay@users.noreply.github.com>
   Date:   Mon Dec 9 11:43:49 2024 -0600

       ft. cambios en documentación

   commit d36f1ecda1ccee7c29d3d20c095a22b3b6a91c24
   Author: JosueSay <106031855+JosueSay@users.noreply.github.com>
   Date:   Mon Dec 9 11:35:24 2024 -0600

       ft. archivo especial subido

   commit 8033ba076fc2c6655186bf482de10b81292f198e
   Author: JosueSay <106031855+JosueSay@users.noreply.github.com>
   Date:   Mon Dec 9 11:14:02 2024 -0600

       dc. Nueva documentación actualizada
   ```

2. Para hacer un **reset** a un commit anterior, toma el **hash** del commit antes de los cambios no deseados (por ejemplo, **`8033ba076fc2c6655186bf482de10b81292f198e`**).

3. Ejecuta el siguiente comando para realizar el **reset**:

   ```bash
   git reset --hard 8033ba076fc2c6655186bf482de10b81292f198e
   ```

   El parámetro **`--hard`** elimina tanto los **archivos** como el **historial de commits** posteriores al commit especificado, lo que puede afectar tanto a tu trabajo como al de otros si ya se han hecho cambios importantes.

4. Después de realizar el **reset**, el historial de commits se actualizará, y el puntero **HEAD** se moverá al commit especificado. Ejecuta `git log` para confirmar:

   ```bash
   commit 8033ba076fc2c6655186bf482de10b81292f198e (HEAD -> main)
   Author: JosueSay <106031855+JosueSay@users.noreply.github.com>
   Date:   Mon Dec 9 11:14:02 2024 -0600

       dc. Nueva documentación actualizada
   ```

#### Tipos de reset:

| **Comando**                      | **Puntero HEAD**             | **Área de Staging**                             | **Directorio de Trabajo**                          | **¿Qué se pierde?**                                                     |
|-----------------------------------|------------------------------|-------------------------------------------------|---------------------------------------------------|-------------------------------------------------------------------------|
| **`git reset --soft <commit>`**   | Mueve a `<commit>`           | Los cambios posteriores al commit se mantienen en staging. | Los archivos no se modifican.                    | Los commits posteriores, pero los cambios están listos para un nuevo commit. |
| **`git reset --mixed <commit>`**  | Mueve a `<commit>`           | Los cambios posteriores se eliminan de staging.  | Los archivos se mantienen como están.             | Los commits posteriores, pero los cambios permanecen en el directorio de trabajo. Debes agregar los cambios a staging manualmente si quieres hacer commit de ellos. |
| **`git reset --hard <commit>`**   | Mueve a `<commit>`           | El área de staging se limpia.                   | Los archivos se restauran al estado del commit.   | Los commits posteriores y los cambios no comprometidos se pierden completamente. |

#### Resumen de los tipos de reset:
- **`--soft`**: Mueve HEAD, conserva cambios en staging y en tu directorio de trabajo.
- **`--mixed`**: Mueve HEAD, limpia staging, pero mantiene los archivos modificados en tu directorio de trabajo.
- **`--hard`**: Mueve HEAD, limpia staging y elimina los cambios en el directorio de trabajo.

### 📌 Conclusión

- **`git revert`**: Crea un nuevo commit que deshace los cambios de un commit anterior, sin eliminar el historial. Ideal para deshacer cambios indeseados sin afectar a otros colaboradores.
- **`git reset`**: Deshace los commits y mueve el puntero de **HEAD** a un commit anterior. Usado principalmente para limpiar el historial de commits o regresar a un estado anterior del proyecto.

### 🛠️ ¿Cuándo usar cada uno?

- **Corrección de errores**: Si un archivo fue subido incorrectamente y necesitas revertirlo, **`git revert`** es la mejor opción. Si varios colaboradores necesitan revertir sus cambios, **`git reset`** puede ser más adecuado.
- **Limpieza del historial**: Cuando tienes un historial largo con muchos commits irrelevantes, puedes usar **`git reset`** para limpiar el historial de forma más drástica.
- **Manejo de conflictos entre ramas**: Si no puedes resolver un conflicto entre ramas, un **`git reset`** podría ser útil para regresar a un punto funcional del proyecto.

> **Nota**: El uso de **`git reset --hard`** debe ser la última opción, ya que puede causar pérdida de trabajo si no se usa correctamente.

## 🛠️ Documentación Integrada: **Uso de Git Tag y Checkout**

### 🏷️ **Git Tag**

El comando `git tag` se utiliza para asignar etiquetas a los commits, facilitando su identificación en el futuro. Las etiquetas son útiles para marcar **versiones específicas** de un proyecto o **hitos importantes** en el historial de commits.

#### 🚀 **Uso básico:**

1. **Crear una etiqueta:**  
   Para asignar una etiqueta a un commit reciente:
   ```bash
   git tag -a v1.0 -m "Mi primera versión"
   ```
   - `-a v1.0`: Crea una etiqueta con el nombre "v1.0".
   - `-m "Mi primera versión"`: Mensaje descriptivo para la etiqueta.

2. **Ver etiquetas existentes:**  
   Muestra todas las etiquetas del repositorio:
   ```bash
   git tag
   ```

3. **Obtener detalles de una etiqueta:**  
   Para ver información detallada del commit asociado a una etiqueta:
   ```bash
   git show <etiqueta>
   ```

4. **Eliminar una etiqueta:**  
   Borra una etiqueta localmente sin afectar el historial:
   ```bash
   git tag -d <etiqueta>
   ```

#### 📝 **Ejemplo práctico:**  
Si tienes el siguiente commit:
```bash
commit dc6fff31021852d394873ff869dd9a8d682bedb0 (HEAD -> main)
Author: JosueSay <106031855+JosueSay@users.noreply.github.com>
Date:   Mon Dec 9 12:37:13 2024 -0600

    dc. documentación sobre reset y revert
```
Puedes etiquetarlo como "v1.0":
```bash
git tag -a v1.0 -m "Mi primera versión"
```
Esto permite identificar este commit fácilmente en el futuro al ejecutar `git tag`.

---

### 🔄 **Git Checkout**

El comando `git checkout` permite cambiar entre **ramas** o explorar un **commit específico** sin modificar la rama principal. Esto es útil para evaluar cambios o realizar pruebas en puntos específicos del historial.

#### 🔍 **Cambiar a un commit específico:**

1. **Identifica el hash del commit** que deseas explorar:
   ```bash
   git log
   ```
2. **Cambia a ese commit:**
   ```bash
   git checkout <hash>
   ```
   Esto moverá tu `HEAD` al commit especificado, colocándote en un estado de **HEAD detached**.

#### 🔙 **Regresar a la rama principal:**  
Después de explorar, vuelve al estado actual de la rama principal con:
```bash
git checkout main
```

#### 💡 **Ejemplo práctico:**  
Imagina este historial de commits:
```bash
commit f3e384197dec8e2f611d3fa79512aec484f020e9 (HEAD -> main)
Author: JosueSay <106031855+JosueSay@users.noreply.github.com>
Date:   Mon Dec 9 21:15:25 2024 -0600

    dc. pre documentación de checkout

commit dc6fff31021852d394873ff869dd9a8d682bedb0 (tag: v1.0)
Author: JosueSay <106031855+JosueSay@users.noreply.github.com>
Date:   Mon Dec 9 12:37:13 2024 -0600

    dc. documentación sobre reset y revert
```
Para explorar el segundo commit:
```bash
git checkout dc6fff31021852d394873ff869dd9a8d682bedb0
```
Esto mostrará:
```bash
HEAD detached at dc6fff3
```
Puedes realizar pruebas en este estado. Una vez terminado, vuelve a la rama principal:
```bash
git checkout main
```

#### ⚠️ **Notas importantes:**
- Los cambios realizados en el estado de **HEAD detached** no se reflejarán en ninguna rama, a menos que los guardes explícitamente.
- Si deseas conservar los cambios, crea una nueva rama:
  ```bash
  git switch -c <nombre-nueva-rama>
  ```

### ✅ **Conclusión:**
- **🏷️ Git Tag:** Ideal para marcar puntos importantes en el historial de commits, como versiones de software.
- **🔄 Git Checkout:** Perfecto para explorar y probar cambios en commits específicos sin afectar la rama principal.

## ⚔️ Resolución de Conflictos en Git

Los **conflictos** en Git ocurren cuando dos o más desarrolladores modifican el mismo archivo y se intenta fusionar las ramas que contienen estos cambios. Git no puede decidir automáticamente qué modificaciones conservar, por lo que requiere intervención manual para resolver el conflicto.

![Conflicto en Merge](../images/merge.png "Conflicto en Merge")

### 🛠️ Reproduciendo un Conflicto

1. **Crear un archivo base:**  
   Creamos un archivo llamado **`conflict.txt`**, añadimos contenido inicial y guardamos los cambios en Git:

   ```bash
   echo "Línea original" > practice/conflict.txt
   git add .
   git commit -m "Agregar archivo conflict.txt"
   ```

2. **Generar cambios en ramas distintas:**  
   - Creamos una nueva rama llamada **`developer`**:
     ```bash
     git checkout -b developer
     ```
   - Modificamos el archivo **`conflict.txt`**, añadimos y guardamos los cambios:
     ```bash
     echo "cambios desde la rama developer" >> practice/conflict.txt
     git add .
     git commit -m "Cambios desde developer"
     ```
   - Volvemos a la rama **`main`** y realizamos otros cambios en el mismo archivo:
     ```bash
     git checkout main
     echo "segundo cambio desde main" >> practice/conflict.txt
     git add .
     git commit -m "Cambios desde main"
     ```

3. **Intentar fusionar las ramas:**  
   Cuando intentamos fusionar **`developer`** con **`main`**, Git detecta un conflicto:

   ```bash
   git merge developer
   ```

   Resultado en la terminal:
   ```bash
   Auto-merging practice/conflict.txt
   CONFLICT (content): Merge conflict in practice/conflict.txt
   Automatic merge failed; fix conflicts and then commit the result.
   ```

### 🧐 Analizando el Conflicto

Al abrir el archivo **`conflict.txt`**, veremos una marca especial que indica el conflicto:

```txt
Línea original

<<<<<<< HEAD
segundo cambio desde main
=======
cambios desde la rama developer
>>>>>>> developer
```

- **`HEAD`**: Representa los cambios en la rama **`main`**.
- **`developer`**: Representa los cambios en la rama **`developer`**.

### ✅ Resolviendo el Conflicto

1. Decide cuál contenido conservar o si es necesario fusionar ambos cambios manualmente.
2. Edita el archivo para dejar únicamente el contenido deseado. Por ejemplo:

   ```txt
   Línea original

   segundo cambio desde main
   cambios desde la rama developer
   ```

3. Guarda el archivo después de resolver el conflicto.

4. Marca el conflicto como resuelto y realiza el commit:

   ```bash
   git add practice/conflict.txt
   git commit -m "Resolver conflicto en conflict.txt"
   ```

### 📋 Verificando la Resolución

Puedes verificar el estado del repositorio antes y después de resolver el conflicto con:

```bash
git status
```

Antes de resolver:
```txt
On branch main
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   practice/conflict.txt
```

Después de resolver:
```txt
On branch main
All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)
```

### 🗑️ Eliminando Ramas Innecesarias

Una vez que los cambios se han fusionado y el conflicto está resuelto, elimina la rama para evitar conflictos futuros:

```bash
git branch -D developer
```

### 📝 Notas Adicionales

- Si te sientes perdido durante el proceso de resolución, puedes **abortar el merge** con:
  ```bash
  git merge --abort
  ```
- Usa `git log` para verificar que el último commit incluye los cambios fusionados de ambas ramas:

  ```bash
  git log
  ```





















