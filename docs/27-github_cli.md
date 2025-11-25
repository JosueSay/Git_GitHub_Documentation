# GitHub CLI

GitHub CLI es una herramienta que permite interactuar con GitHub directamente desde la línea de comandos. A continuación, te explicamos cómo instalarla, configurarla y usarla.

## 📥 Instalación de GitHub CLI

1. **Descargar GitHub CLI**:  
   Descarga la aplicación de acuerdo al sistema operativo que uses. Puedes encontrar los instaladores oficiales en el sitio de GitHub CLI:

   - [Documentación](https://github.com/cli/cli)
   - [Instalación en Windows](https://cli.github.com/)
   - [Manual de GitHub CLI](https://cli.github.com/manual/gh)

2. **Verificar la instalación**:  
   Una vez instalada, abre la terminal o consola y ejecuta el siguiente comando para asegurarte de que GitHub CLI esté correctamente instalada:

   ```bash
   gh --version
   ```

3. **Autenticación**:  
   Para usar GitHub CLI, necesitas autenticarte con tu cuenta de GitHub. Ejecuta el siguiente comando para iniciar el proceso de autenticación:

   ```bash
   gh auth login
   ```

   El comando te guiará a través de un formulario. Aquí debes completar los siguientes pasos:

   - Seleccionar el protocolo SSH o HTTPS para las operaciones de Git.
   - Si eliges SSH, debes proporcionar una **clave SSH** diferente a la que usas para los repositorios normales. Esta clave se utiliza específicamente para la autenticación de la aplicación GitHub CLI.
   - Si eliges autenticación por token, asegúrate de usar un token diferente al que usas para autenticarte con GitHub en el navegador.

   **Ejemplo de comandos de autenticación:**

   ```bash
   ? Where do you use GitHub? GitHub.com
   ? What is your preferred protocol for Git operations on this host? SSH
   ? Upload your SSH public key to your GitHub account? KEY
   ? Title for your SSH key: (GitHub CLI) NAME SSH KEY

   ? Title for your SSH key: NAME SSH KEY
   ? How would you like to authenticate GitHub CLI? Login with a web browser

   ! First copy your one-time code: CODE
   Press Enter to open https://github.com/login/device in your browser...
   ✓ Authentication complete.
   - gh config set -h github.com git_protocol ssh
   ✓ Configured git protocol
   ✓ SSH key already existed on your GitHub account: C:\Users\josue\.ssh\key_git.pub
   ✓ Logged in as JosueSay
   ```

## ⚙️ Usando GitHub CLI

Una vez configurada, puedes usar GitHub CLI para realizar varias acciones sin tener que acceder a la interfaz web. Algunos comandos útiles incluyen:

- **Crear repositorios desde la consola**:

  ```bash
  gh repo create
  ```

  Este comando abrirá un formulario para que configures el nuevo repositorio directamente desde la línea de comandos.

- **Crear un nuevo issue**:

  ```bash
  gh issue create
  ```

  Este comando permite crear un *issue* en tu repositorio, llenando el formulario directamente en la terminal.

## 🖥️ Escenarios de Uso

GitHub CLI es muy útil en escenarios de automatización. Por ejemplo, puedes usarla en un script para crear issues o interactuar con tu repositorio sin tener que usar el navegador.

Otro escenario común es utilizar el botón verde de "Code" en el repositorio de GitHub, donde se ofrece una opción de **CLI** para clonar el repositorio directamente usando GitHub CLI.
