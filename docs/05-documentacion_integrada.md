# 🛠️ Documentación Integrada: **Uso de Git Tag y Checkout**

## 🏷️ **Git Tag**

El comando `git tag` se utiliza para asignar etiquetas a los commits, facilitando su identificación en el futuro. Las etiquetas son útiles para marcar **versiones específicas** de un proyecto o **hitos importantes** en el historial de commits.

### 🚀 **Uso básico:**

1. **Crear una etiqueta:**  
   Para asignar una etiqueta a un commit reciente:

   ```bash
   git tag -a v1.0 -m "Mi primera versión"
   ```

   - `-a v1.0`: Crea una etiqueta con el nombre "v1.0".
   - `-m "Mi primera versión"`: Mensaje descriptivo para la etiqueta.

2. **Ver etiquetas existentes:**  
   Muestra todas las etiquetas del repositorio:

   ```bash
   git tag
   ```

3. **Obtener detalles de una etiqueta:**  
   Para ver información detallada del commit asociado a una etiqueta:

   ```bash
   git show <etiqueta>
   ```

4. **Eliminar una etiqueta:**  
   Borra una etiqueta localmente sin afectar el historial:

   ```bash
   git tag -d <etiqueta>
   ```

### 📝 **Ejemplo práctico:**

Si tienes el siguiente commit:

```bash
commit dc6fff31021852d394873ff869dd9a8d682bedb0 (HEAD -> main)
Author: JosueSay <106031855+JosueSay@users.noreply.github.com>
Date:   Mon Dec 9 12:37:13 2024 -0600

    dc. documentación sobre reset y revert
```

Puedes etiquetarlo como "v1.0":

```bash
git tag -a v1.0 -m "Mi primera versión"
```

Esto permite identificar este commit fácilmente en el futuro al ejecutar `git tag`.

## 🔄 **Git Checkout**

El comando `git checkout` permite cambiar entre **ramas** o explorar un **commit específico** sin modificar la rama principal. Esto es útil para evaluar cambios o realizar pruebas en puntos específicos del historial.

### 🔍 **Cambiar a un commit específico:**

1. **Identifica el hash del commit** que deseas explorar:

   ```bash
   git log
   ```

2. **Cambia a ese commit:**

   ```bash
   git checkout <hash>
   ```

   Esto moverá tu `HEAD` al commit especificado, colocándote en un estado de **HEAD detached**.

### 🔙 **Regresar a la rama principal:**

Después de explorar, vuelve al estado actual de la rama principal con:

```bash
git checkout main
```

### 💡 **Ejemplo práctico:**

Imagina este historial de commits:

```bash
commit f3e384197dec8e2f611d3fa79512aec484f020e9 (HEAD -> main)
Author: JosueSay <106031855+JosueSay@users.noreply.github.com>
Date:   Mon Dec 9 21:15:25 2024 -0600

    dc. pre documentación de checkout

commit dc6fff31021852d394873ff869dd9a8d682bedb0 (tag: v1.0)
Author: JosueSay <106031855+JosueSay@users.noreply.github.com>
Date:   Mon Dec 9 12:37:13 2024 -0600

    dc. documentación sobre reset y revert
```

Para explorar el segundo commit:

```bash
git checkout dc6fff31021852d394873ff869dd9a8d682bedb0
```

Esto mostrará:

```bash
HEAD detached at dc6fff3
```

Puedes realizar pruebas en este estado. Una vez terminado, vuelve a la rama principal:

```bash
git checkout main
```

### ⚠️ **Notas importantes:**

- Los cambios realizados en el estado de **HEAD detached** no se reflejarán en ninguna rama, a menos que los guardes explícitamente.
- Si deseas conservar los cambios, crea una nueva rama:

  ```bash
  git switch -c <nombre-nueva-rama>
  ```

## ✅ **Conclusión:**

- **🏷️ Git Tag:** Ideal para marcar puntos importantes en el historial de commits, como versiones de software.
- **🔄 Git Checkout:** Perfecto para explorar y probar cambios en commits específicos sin afectar la rama principal.
