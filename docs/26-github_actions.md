# 🚀 Usar GitHub Actions para Editar Perfil de GitHub

Puedes automatizar la actualización de tu perfil de GitHub utilizando una **GitHub Action** llamada "recent-activity". Esta acción permite obtener la actividad reciente de tu cuenta de GitHub y reflejarla en tu archivo `README.md`. A continuación, te guiaré a través del proceso para configurar esta acción.

## 🛠️ Pasos para Configurar la Action

1. **Crea la Carpeta y el Archivo de Workflow:**

   En tu repositorio de usuario o de portada, crea la siguiente estructura de carpetas y archivo:

   ```bash
   .github/workflows/update-readme.yml
   ```

2. **Agrega el Workflow en el archivo `update-readme.yml`:**

   Copia y pega la siguiente plantilla en el archivo `update-readme.yml`:

   ```yml
   name: Update README

   on:
     schedule:
       - cron: '*/30 * * * *'  # Actualización cada 30 minutos
     workflow_dispatch:

   jobs:
     build:
       runs-on: ubuntu-latest
       name: Update Profile README

       steps:
         - uses: actions/checkout@v3
         - uses: Readme-Workflows/recent-activity@v2.0.0
           env:
             GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
   ```

   Este workflow se ejecutará automáticamente cada 30 minutos, y también puedes ejecutarlo manualmente utilizando `workflow_dispatch`.

3. **Crea el Archivo de Configuración de Actividad Reciente:**

   Crea un archivo llamado `recent-activity.config.yml` con la siguiente configuración:

   ```yml
   username: JosueSay
   max_lines: 3
   readme_file: ./README.md
   disabled_events: []
   timezone: America/Guatemala
   commit_text: ":zap: Update recent activity"
   ```

   - `username`: Especifica tu nombre de usuario de GitHub.
   - `max_lines`: El número máximo de actividades que deseas mostrar.
   - `readme_file`: La ubicación del archivo `README.md` que deseas actualizar.
   - `disabled_events`: Puedes deshabilitar ciertos eventos si no los deseas mostrar.
   - `timezone`: Define la zona horaria de tu actividad.
   - `commit_text`: El mensaje de commit que se utilizará al realizar la actualización.

4. **Modifica tu archivo `README.md`:**

   Dentro de tu archivo `README.md`, crea un apartado para mostrar la actividad reciente, e inserta los siguientes comentarios para identificar donde se actualizará la actividad:

   ```markdown
   <!--RECENT_ACTIVITY:start-->

   <!--RECENT_ACTIVITY:last_update-->
   ```

## 🏃‍♂️ Ejecutando el Workflow

1. **Sube los Cambios:**
   Una vez hayas configurado los archivos, sube los cambios a tu repositorio.

2. **Ejecuta Manualmente el Workflow:**
   La primera vez que se ejecuta el workflow, deberás ejecutarlo manualmente desde la interfaz de GitHub. Después de esa primera ejecución, el workflow se ejecutará automáticamente según el cron especificado (en este caso, cada 30 minutos).

## 🔐 Configuración Adicional de Permisos

Para permitir que la acción pueda editar el archivo `README.md`, debes asegurarte de que GitHub Actions tenga permisos de **lectura y escritura**:

1. Dirígete a `Settings > Actions > General > Workflow Permissions`.
2. Marca la opción **"Read and Write permissions"**.
