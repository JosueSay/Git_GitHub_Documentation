# Pull Requests y Ramas en GitHub

En este apartado, aprenderás a trabajar con **pull requests**, ramas, y plantillas de pull request para mantener un flujo de trabajo estructurado y eficiente.

## 📝 Uso de una plantilla de Pull Request

Para estandarizar la creación de pull requests, podemos usar una plantilla llamada `pull_request_template.md`. Este archivo asegura que cada pull request siga una estructura definida.

## 🚀 Ejemplo práctico

1. **Configuración inicial**:
   - Usaremos los archivos del repositorio [git-github](https://github.com/platzi/git-github).
   - Copia los archivos de `API_PYTHON` a la carpeta `practice/API`.

2. **Instalación de dependencias**:
   En la terminal, dirígete a la carpeta `practice/API` y ejecuta el siguiente comando para instalar las dependencias:

   ```bash
   pip install -r requirements.txt
   ```

3. **Ejecución de la API**:
   Ejecuta el siguiente comando para iniciar el servidor de desarrollo usando **Uvicorn**:

   ```bash
   uvicorn app:app --reload
   ```

   **Salida esperada**:

   ```bash
   (.venv) PS D:\GitHub Repositorios\Aprendizaje\Git & GitHub\practice\API> uvicorn app:app --reload
   INFO:     Will watch for changes in these directories: ['D:\\GitHub Repositorios\\Aprendizaje\\Git & GitHub\\practice\\API']
   INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
   INFO:     Started reloader process [776] using WatchFiles
   INFO:     Started server process [32516]
   INFO:     Waiting for application startup.
   INFO:     Application startup complete.
   INFO:     127.0.0.1:57343 - "GET / HTTP/1.1" 404 Not Found
   INFO:     127.0.0.1:57369 - "GET /familia HTTP/1.1" 200 OK
   ```

4. **Probar la API**:
   Abre tu navegador y visita las siguientes URLs para explorar los datos obtenidos:

   - [http://127.0.0.1:8000/familia](http://127.0.0.1:8000/familia)
   - [http://127.0.0.1:8000/superheroesDC](http://127.0.0.1:8000/superheroesDC)

   Cuando hayas terminado, detén la ejecución de la API.

## 📤 Subir cambios y crear un Pull Request

1. **Subir cambios al repositorio**:
   Luego de realizar tus cambios, súbelos al repositorio usando los comandos de Git. Al hacerlo, deberías ver una salida similar a esta:

   ```bash
   Enumerating objects: 14, done.
   Counting objects: 100% (14/14), done.
   Delta compression using up to 12 threads
   Compressing objects: 100% (9/9), done.
   Writing objects: 100% (10/10), 1.74 KiB | 593.00 KiB/s, done.
   Total 10 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
   remote: Resolving deltas: 100% (5/5), completed with 4 local objects.
   remote: 
   remote: Create a pull request for 'josue/tarea01' on GitHub by visiting:
   remote:      https://github.com/JosueSay/GitDocumentation/pull/new/josue/tarea01
   remote:
   To https://github.com/JosueSay/GitDocumentation.git
    * [new branch]      josue/tarea01 -> josue/tarea01
   branch 'josue/tarea01' set up to track 'origin/josue/tarea01'.
   ```

2. **Crear el Pull Request**:
   Sigue el enlace proporcionado en la salida para crear el pull request.

3. **Llenar el formulario del Pull Request**:
   Al crear el pull request, se cargará automáticamente la plantilla que configuraste en `pull_request_template.md`. Llena los campos según las indicaciones para estructurar tu pull request correctamente.

## 🌟 Ejemplo de la plantilla de Pull Request

Aquí tienes un ejemplo visual de cómo luciría la plantilla aplicada en un pull request:

![Plantilla Pull Request](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/pull_request2.png "Plantilla Pull Request")

![Plantilla Pull Request](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/pull_request3.png "Plantilla Pull Request")
