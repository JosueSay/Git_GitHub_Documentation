# 🔗 Integración de Git y GitHub  

Aunque **Git** y **GitHub** son herramientas diferentes, se pueden vincular para trabajar en equipo y gestionar proyectos de forma eficiente.  

![Flow Git](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/flow%20github.png "Flow Git")  

## 🛠️ **Crear un repositorio**  

1. Ve a la opción del ícono de **"+"** en la parte superior derecha.  
   ![Crear repositorio](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/step1.png "Crear repositorio")  

2. Llena el formulario para crear el repositorio:  
   - **Nombre del repositorio.**  
   - **Descripción:** Explica el propósito del proyecto.  
   - **Visibilidad:** Selecciona si será **público** o **privado**.  
   - **Inicializar con un README:** Recomendado para documentar el proyecto.  
   - **GitIgnore:** Excluye archivos específicos según el lenguaje o herramienta.  
   - **Licencia:** Define los permisos y restricciones de uso del código.  

   ![Formulario crear repositorio](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/step2.png "Formulario crear repositorio")  

3. **Crear el repositorio:**  
   Haz clic en el botón para finalizar la creación.  

## 👥 **Agregar colaboradores**  

1. Ve a **"Settings"** en el repositorio.  
2. En la sección de **"Collaborators"**, agrega personas como colaboradores (estas personas deben tener una cuenta de GitHub).  
3. El colaborador recibirá una invitación que debe aceptar para poder colaborar en el proyecto.  

   ![Colaboradores](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/step3.png "Colaboradores")  

## 🌐 **Clonar el repositorio**  

En el repositorio encontrarás una rama principal llamada **main**. Para trabajar localmente, puedes clonar el repositorio usando el botón **"Code"**, eligiendo entre tres opciones:

- 🌍 **HTTPS.**
- 🔒 **SSH.**  
- 💻 **GitHub CLI.**  

### **Clonar usando HTTPS:**

1. Copia la URL proporcionada, por ejemplo:

   ```plaintext
   https://github.com/JosueSay/GitDocumentation.git
   ```

2. En la terminal, ejecuta el comando:

   ```bash
   git clone <url>
   ```  

   ![Clonando repositorio](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/step4.png "Clonando repositorio")  

3. Una vez clonado, verás que el repositorio aparece como una carpeta en tu equipo. Dentro de esta carpeta, encontrarás archivos como el `README.md`.  
4. Adicional se agrega una pagina para ver los [Planes de GitHub](https://github.com/pricing "Planes de GitHub") y comparar precios.

## 🔗 Fusionar entorno local y remoto  

Para unificar tu entorno local de Git con un repositorio remoto en GitHub, puedes usar el siguiente comando:  

```bash
git remote add origin <URL_DEL_REPOSITORIO_REMOTO>
```  

### Pasos

1. **Agregar el repositorio remoto:**  
   Reemplaza `<URL_DEL_REPOSITORIO_REMOTO>` con la URL de tu repositorio en GitHub. Esto vincula tu repositorio local con el remoto.  

2. **Verificar la conexión:**  
   Usa el comando:

   ```bash
   git remote -v
   ```

   Esto mostrará las URLs configuradas para las conexiones remotas. Verifica que la URL listada coincida con la del repositorio remoto que quieres usar.  
