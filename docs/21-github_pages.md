# 🌐 GitHub Pages

**GitHub Pages** es una herramienta que permite hospedar sitios web directamente desde un repositorio de GitHub, ya sea para proyectos estáticos o dinámicos.

## 🚀 ¿Cómo usar GitHub Pages?

1. **Accede a Gist GitHub:**  
   Dirígete a la página de [GitHub Pages](https://pages.github.com/ "GitHub Pages") y sigue el tutorial.

2. **Crea un repositorio**:  
   Crea un repositorio con el formato `usuario.github.io`.

3. **Prepara los archivos del sitio**:  
   Coloca los archivos de tu sitio web en una carpeta llamada `docs`. Esta carpeta será utilizada para almacenar el contenido del sitio.

4. **Configura GitHub Pages**:  
   - Ve a la pestaña `Settings` de tu repositorio.
   - En la sección **Pages**, selecciona la rama que contiene los archivos del proyecto, usualmente `main`, y selecciona la carpeta `docs` como la fuente.
   - Guarda los cambios.

5. **Accede al sitio**:  
   Después de guardar la configuración, podrás acceder a tu sitio web en una URL proporcionada por GitHub. Esta URL será algo como `https://usuario.github.io`.

6. **Personaliza el dominio (opcional)**:  
   Si deseas usar un dominio personalizado, puedes configurarlo para que la URL de tu sitio web sea más amigable y personalizada.

## 🔧 Configuración Avanzada de GitHub Codespaces

### 🌟 Uso de Plantillas en Codespaces

Los Codespaces pueden configurarse con plantillas para entornos personalizados. En lugar de vincular un repositorio específico, puedes crear un entorno limpio, como para trabajar con **Django**, utilizando configuraciones predefinidas.

#### 📁 `devcontainer.json`

El archivo `devcontainer.json`, ubicado en la carpeta **.devcontainer**, almacena las configuraciones necesarias para el entorno, como:

- **Extensiones** a instalar.
- Configuraciones específicas del contenedor.  

Este archivo permite que el Codespace esté listo para usar inmediatamente tras su creación.

### 💻 Ejecución Local en Visual Studio Code

Puedes abrir un Codespace en la aplicación de escritorio de **Visual Studio Code**:

1. Al abrir un Codespace por primera vez, se te pedirá instalar una extensión específica.
2. Git debe estar configurado en tu máquina local para trabajar con el repositorio.

⚠️ **Problema común:** Si el Codespace en la web utiliza el mismo puerto que tu entorno local, puede causar conflictos.  
**Solución:**

- Detén la ejecución del Codespace en el navegador.
- Reinicia la ejecución en Visual Studio Code local.

### 🚀 Ventajas de GitHub Codespaces

- Configuración rápida de entornos para múltiples lenguajes.
- Elimina la necesidad de instalar herramientas localmente.
- Acelera la colaboración en equipo con entornos consistentes.  

## 🤝 Pair Programming con VS Code y Codespaces

**Pair Programming** (programación en pareja) se puede realizar fácilmente utilizando la extensión **Live Share** en Visual Studio Code, incluso dentro de un Codespace. Esta herramienta permite que varios desarrolladores trabajen simultáneamente en el mismo código en tiempo real, con los siguientes beneficios:

### 🌐 Configuración y Uso de Live Share

1. **Instalar Live Share:**
   - Descarga la extensión **Live Share** desde el marketplace de Visual Studio Code y agregarla al devcontainer.

2. **Iniciar una Sesión:**
   - En VS Code, inicia Live Share y genera un enlace para compartir.
   - Los colaboradores podrán unirse seleccionando entre continuar en **Visual Studio Code** o en un navegador web.

3. **Ediciones en Tiempo Real:**
   - Una vez conectados, los participantes podrán ver y editar el código en tiempo real.
   - Los cambios realizados por los colaboradores se reflejarán directamente en el entorno compartido.

### 📋 Commits Colaborativos

Cuando se realizan cambios en el entorno compartido:

- Los commits generados incluirán un mensaje de **coautor**, asegurando que quede registrada la contribución de todos los desarrolladores involucrados.

### 🛠️ Requisitos en un Codespace

Si el entorno compartido es un Codespace:

- Asegúrate de que las extensiones necesarias estén instaladas en el Codespace para que todos puedan trabajar sin inconvenientes.
- Como anfitrión, puedes detener la sesión de **Live Share** en cualquier momento para finalizar la colaboración.

### 🚀 Ventajas de Pair Programming con Live Share

- **Colaboración en Tiempo Real:** Ideal para resolver problemas complejos y compartir conocimientos.
- **Sincronización de Cambios:** Todos los participantes trabajan sobre el mismo entorno y código, reduciendo errores.
- **Registro de Autores:** Los commits reflejan el trabajo colaborativo automáticamente.
- **Trabajo en la Nube:** Dado que es una máquina virtual los colaboradores no tienen acceso al sistema sino solo al codespace compartido.

## ✏️ GitHub Dev Editor

GitHub ofrece una herramienta integrada para editar código directamente desde la web: el **GitHub Dev Editor**, una versión ligera y funcional que facilita realizar ediciones rápidas en los repositorios sin necesidad de configurar un entorno local.

### 🚀 Cómo Acceder al GitHub Dev Editor

1. Abre un repositorio en GitHub.
2. Presiona la tecla **"."** (punto) o selecciona la opción correspondiente en el menú. Esto abrirá el editor integrado.
3. El editor se asemeja a **Visual Studio Code**, pero está optimizado para ediciones rápidas desde la web.

![GitHub Dev Editor](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/dev_editor.png "GitHub Dev Editor")

### 🌟 Características del Dev Editor

- **Ediciones Directas:** Permite editar archivos en texto plano directamente en el navegador.
- **Navegación Sencilla:** Puedes regresar al repositorio utilizando el menú de tres líneas horizontales y seleccionando la opción para volver al repositorio.
- **Sin Configuración:** No requiere instalación ni configuración previa.

### 🛠️ Diferencias entre GitHub Dev Editor y Codespaces

| Característica             | GitHub Dev Editor                     | Codespaces                          |
|----------------------------|----------------------------------------|-------------------------------------|
| **Funcionalidad**          | Editor de texto para cambios rápidos y gratis. | Entorno de desarrollo completo con costo adicional si sobrepasan las horas gratis.    |
| **Acceso a Terminal**      | No disponible.                        | Incluye terminal integrada.        |
| **Uso de Recursos**        | Ligero, no requiere infraestructura.  | Utiliza una máquina virtual.       |
| **Ideal para**             | Ediciones simples y rápidas.          | Desarrollo avanzado y colaborativo.|

### 📌 Nota Importante

Aunque el Dev Editor tiene una apariencia similar a **VS Code**, **no es un Codespace**. Si intentas usar funcionalidades avanzadas, como la terminal, GitHub te pedirá crear un Codespace para continuar.
