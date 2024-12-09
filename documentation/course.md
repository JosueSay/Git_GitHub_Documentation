# 📚 Curso de Git y GitHub

![Banner del Curso](../images/banner.png "Banner Curso Git y GitHub")

**Fecha:** 26/11/2024

**Enlace del Curso:** [Git y GitHub en Platzi](https://platzi.com/cursos/gitgithub/ "Enlace Curso Git y GitHub")

**Profesor:** Amin Espinoza

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

## Ramas

Las ramas se crearon con el fin de trabajar sin obstaculizar el trabajo de los demás.

![Branch Git](branch.png "Branch Git")

Primero se puede observar la rama en que se encuentra mediante el comando "git branch" esto listara las ramas que tengo en el repositorio y con un asterisco "*" se identificará la rama en la cual estoy actualmente.

Para crear una nueva rama se puede hacer "git checkout -b name_branch" esto creará una nueva rama y se moverá a esa rama correspondiente por ejemplo al crear la rama "amin con el comando anterior y hacer git branch veremos que estamos en la rama amin y no main.

Creamos un archivo test3.txt en practice y lo metemos al repositorio y esto significa que hemos metido cambios en la rama amin y no se mirarán en main. Por lo tanto para que todos los integrantes puedan ver esos cambios se debe unir la rama amin con la main mediante un merge o fusión con esto lograremos que tendremos la rama principal main con el contenido de la rama individual amin.

Para ello volvemos a la rama que queremos guardar todo el contenido, en este caso main con el comando git checkout main o el comando git switch main. una vez estando en esa rama se hace un merge con git merge amin con esto indicaremos que gracias a un método de unificación Fast-forward los archivos modifcados se han agregado a la rama actual. Para asegurarnos de eso podemos hacer un git log para ver que los commits de la bitacora en main sean los esperados.

Una buena práctica despues de unificar la rama principal con la individual, esta rama individual ya no tiene ningún sentido, esto quiere decir que esa rama ya no se necesita tener.
