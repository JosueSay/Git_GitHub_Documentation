# Seguridad en GitHub

## 🔐 GitHub Tokens

Los **tokens de acceso personal** (PAT, por sus siglas en inglés) en GitHub son claves que permiten interactuar con repositorios de forma segura, especialmente cuando se trabaja con repositorios privados o se automatizan procesos. Estos tokens son una alternativa más segura que compartir contraseñas.

### 🚩 Características Principales

1. **Seguridad:** Permiten acceso sin compartir contraseñas.
2. **Privilegios Ajustables:** Puedes definir qué acciones están permitidas con el token.
3. **Expiración:** Pueden tener una fecha de vencimiento para mayor control y seguridad.
4. **Tipos:**
   - **Fine-grained Tokens:** Mayor granularidad en permisos y control.
   - **Classic Tokens:** Opciones más generales y menos detalladas.

### 🚀 Creación de Tokens

1. Ve a **Settings > Developer Settings > Personal Access Tokens**.
2. Selecciona el tipo de token que deseas crear:
   - **Fine-grained Tokens** (más detallados).
   - **Classic Tokens** (opciones básicas).

#### Creación de un Token Clásico

1. Llena el formulario con:
   - **Nombre del token.**
   - **Fecha de expiración.**
   - **Permisos requeridos.**
2. Genera el token y copia el valor proporcionado.

> ⚠️ **Importante:** El token solo se muestra una vez. Si lo pierdes, deberás eliminarlo y crear uno nuevo.

![Token](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/token.png "Token clásico")
![Formulario de Token](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/token2.png "Formulario de Token")
![Token Generado](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/token3.png "Token Generado")

#### Creación de un Fine-grained Token

1. Llena el formulario con:
   - **Nombre del token.**
   - **Repositorios específicos o globales a los que aplica.**
   - **Permisos ajustados por repositorio.**
   - **Fecha de expiración (no permite opciones de "sin expiración").**

![Fine-grained Token](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/token4.png "Fine-grained Token")

### 🖥️ Uso de Tokens

#### Clonar un Repositorio con Token

Al clonar o acceder a un repositorio con un token se pedirán credenciales:

1. Ingresa tu **username** (nombre de usuario en GitHub).
2. Como **contraseña**, usa el **personal access token** en lugar de la contraseña de tu cuenta.

#### Casos de Uso

- Acceso desde otros dispositivos o equipos.
- Automatización con GitHub Actions o scripts personalizados.
- Creación de flujos de trabajo para CI/CD.
- Acceso seguro a API de GitHub.

### 📌 Diferencias entre Tokens

| Característica                   | Fine-grained Tokens                      | Classic Tokens            |
|----------------------------------|------------------------------------------|---------------------------|
| **Granularidad de Permisos**     | Permisos ajustados por repositorio.       | Permisos generales.       |
| **Aplicación por Repositorio**   | Repositorios específicos o todos.         | Aplica a todos los repositorios. |
| **Expiración**                   | Fecha de expiración obligatoria.          | Puede no tener expiración.|
| **Seguridad Adicional**          | Mayor control y restricciones.            | Menor nivel de detalle.   |

## 🛠️ Gestión de Dependencias con Dependabot

Dependabot es una herramienta de GitHub que ayuda a mantener tus proyectos actualizados y seguros al gestionar las dependencias. Es especialmente útil para detectar y solucionar brechas de seguridad en paquetes de terceros, como los utilizados en **Python** o **npm**.

### 🔒 Habilitación de Dependabot

1. Ve a **Security > Dependabot** en tu repositorio.
2. Dirígete a **Settings > Code security and analysis**.
3. Habilita las opciones disponibles en el apartado de **Dependabot**.

![Dependabot](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/dependabot.png "Dependabot")

### 📄 Configuración del Archivo `dependabot.yml`

Cuando habilitas Dependabot, GitHub genera automáticamente un archivo llamado `dependabot.yml` en la carpeta `.github`. Este archivo permite definir las configuraciones del monitoreo de dependencias, como el intervalo de revisión.

#### Ejemplo de Configuración

```yaml
version: 2
updates:
  - package-ecosystem: "npm"  # Ecosistema del paquete (ej., npm, pip, maven, etc.)
    directory: "/"           # Ubicación del archivo manifiesto
    schedule:
      interval: "weekly"     # Frecuencia: daily, weekly, o monthly
```

#### Parámetros Clave

- **`package-ecosystem`**: Especifica el gestor de paquetes (e.g., `npm`, `pip`, `maven`).
- **`directory`**: Ubicación de los archivos manifiesto de dependencias.
- **`schedule`**: Define el intervalo de revisiones (`daily`, `weekly`, `monthly`).

### 🚨 Cómo Funciona Dependabot

1. **Detección de Problemas**: Dependabot monitorea las dependencias declaradas en tu proyecto. Si detecta vulnerabilidades o paquetes desactualizados, genera una alerta en el apartado de **Security**.

2. **Pull Request Automatizado**: Dependabot crea un Pull Request para actualizar la dependencia afectada. Este PR incluye:
   - Detalles sobre el error.
   - Comparación entre versiones.
   - Información sobre compatibilidad y mejoras.

3. **Revisión y Merge**:
   - Revisa los cambios propuestos.
   - Realiza el merge del Pull Request si todo está en orden.

4. **Limpieza Automática**: Una vez aplicado el cambio, Dependabot elimina automáticamente la rama creada.

### ⚡ Beneficios de Usar Dependabot

- **Seguridad Mejorada:** Monitorea vulnerabilidades conocidas en dependencias.
- **Automatización:** Actualiza paquetes sin intervención manual.
- **Compatibilidad Garantizada:** Verifica las versiones para minimizar conflictos.
- **Fácil Integración:** Compatible con múltiples gestores de paquetes (npm, pip, maven, etc.).
