# 💡 Tips Adicionales

Cuando trabajamos con *Pull Requests* en GitHub, podemos utilizar ciertas extensiones de la URL para obtener información útil en formato de texto plano. Estas extensiones permiten compartir los detalles del pull request de manera más sencilla, especialmente en situaciones donde capturas de pantalla o enlaces no son ideales.  

## 🌐 Extensiones Útiles en URLs de Pull Requests

1. **`.diff`**  
   Agregar `.diff` al final de la URL de un pull request muestra los cambios realizados en formato plano, listando únicamente las diferencias de los archivos afectados.  

2. **`.patch`**  
   Agregar `.patch` al final de la URL muestra:  
   - La información proporcionada por `.diff`.  
   - Detalles adicionales sobre el repositorio y el contexto del pull request.  

## 🔍 Ejemplo de Uso

Supongamos que tienes un pull request con esta URL:

```markdown
https://github.com/usuario/repositorio/pull/123
```

Al agregar `.diff` o `.patch` al final, obtendrás:

- **Formato `.diff`:**  

  ```markdown
  https://github.com/usuario/repositorio/pull/123.diff
  ```

  Este enlace genera un archivo de texto plano con las diferencias de los archivos afectados.  

- **Formato `.patch`:**  
  
  ```markdown
  https://github.com/usuario/repositorio/pull/123.patch
  ```

  Este enlace incluye el contenido de `.diff` junto con metadatos del pull request.  

## 📌 ¿Para Qué Sirve?

Estos formatos son útiles para:

- **Compartir Cambios:** Enviar información en texto plano en lugar de capturas de pantalla o enlaces directos.  
- **Análisis Rápido:** Revisar los cambios sin necesidad de abrir GitHub en el navegador.  
- **Uso Offline:** Guardar los cambios en un archivo local para análisis posterior.  

## 💬 Consejo

Estos tips se mencionan en algunas secciones de GitHub como "ProTips":

![ProTip](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/protip.png "ProTip")
