# 🔒 Mantenimiento de Repositorios Seguros

Mantener un repositorio seguro es esencial para proteger datos sensibles, evitar vulnerabilidades y garantizar buenas prácticas en el desarrollo. A continuación, se detallan las estrategias para lograrlo:

## 🌐 Cambio de Visibilidad del Repositorio

Puedes cambiar la visibilidad de un repositorio de público a privado desde:

1. **Settings > Danger Zone**.
2. Selecciona la primera opción para modificar la visibilidad.

Esto garantiza que el acceso al repositorio sea limitado y más seguro.

## 📁 Uso de `.gitignore`

El archivo `.gitignore` permite excluir ciertos archivos o carpetas del control de versiones.

- **Definición:** Ubícalo en la raíz del proyecto y define patrones de exclusión.
  Ejemplo:

  ```bash
  # Ignorar archivos con extensión .sln
  *.sln

  # Ignorar la carpeta bin/
  bin/
  ```

- **Plantillas Predefinidas:** Para facilitar su creación, puedes consultar:
  - [GitHub GitIgnore](https://github.com/github/gitignore)
  - [Plantillas para GitIgnore](https://www.toptal.com/developers/gitignore)
