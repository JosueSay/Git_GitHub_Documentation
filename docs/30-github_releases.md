# 🚀 GitHub Releases

Explorando la documentación de [npm express](https://www.npmjs.com/package/express) y su [repositorio en GitHub](https://github.com/expressjs/express), podemos notar cómo los autores de paquetes descargables publican su código como **Releases**. Esto no solo permite que otros colaboren en el proyecto, sino que también facilita el manejo de versiones y la integración con herramientas como Dependabot.

## 🔧 Creación de un Paquete y Configuración para Releases

Supongamos que queremos crear un paquete básico para subirlo a GitHub como un release. A continuación, se describe el proceso paso a paso:

### 📁 Estructura del Proyecto

1. Crea un archivo `setup.py`:

   ```python
   from setuptools import setup, find_packages

   setup(
      name="TestRelease",                                # Nombre del paquete
      version="0.1.0",                                   # Versión inicial
      packages=find_packages(),                          # Paquetes a incluir
      description="Un paquete pip simple de saludo",     # Breve descripción
      author="Josue Say",                                # Autor del paquete
      author_email="josuesay770@gmail.com",              # Email del autor
      url="https://github.com/josuesay/TestRelease",     # URL del proyecto
   )
   ```

2. Crea un archivo `requirements.txt`:

   ```bash
   setuptools
   ```

3. Crea una carpeta con el nombre del proyecto y crea un archivo `__init__.py`:

   ```python
   def saludar(nombre):
      return "Hola " + nombre + ", este es mi primer paquete pip!"
   ```

### 🔨 Construcción del Paquete

1. Instala los requerimientos del archivo `requirements`.  

2. Genera los archivos necesarios para el paquete ejecutando:

   ```bash
   python setup.py bdist_wheel sdist
   ```

   Esto generará carpetas como `dist` y `build` con los archivos listos para el release.

## 🌟 Publicación de Paquetes en GitHub Releases y PyPI

### 📤 Creación del Release en GitHub

1. Dirígete al repositorio y selecciona el apartado de **Releases** en la parte media derecha.

   ![Releases](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/release.png "Releases")

2. Llena el formulario:  
   - **Tag:** Debe coincidir con la versión en `setup.py` (e.g., `v0.1.0`).  
   - **Título:** Repite el nombre del tag.  
   - **Archivos:** Sube los binarios generados en la carpeta `dist`.  

3. Una vez completado, publica el release.

   ![Releases](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/release2.png "Releases")

### 📦 Consumo del Paquete

1. Ve al release publicado y copia el enlace del archivo `.whl`.  
2. Instala el paquete desde la terminal:

   ```bash
   pip install https://github.com/JosueSay/TestRelease/releases/download/v0.1.0/TestRelease-0.1.0-py3-none-any.whl
   ```

3. Verifica la instalación ejecutando:  

   ```bash
   pip list
   ```

   Deberías ver algo como:

   ```bash
   TestRelease        0.1.0
   ```

### 🛠️ Uso del Paquete

Para usar el paquete, crea un archivo en `practice/app/app.py` con el siguiente contenido:

```python
from TestRelease import saludar

print(saludar("Josue"))
```

Ejecuta el código y obtendrás:  

```bash
Hola Josue, este es mi primer paquete pip!
```
