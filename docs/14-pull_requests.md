# 🔄 Pull Request

Cuando trabajas de manera colaborativa en un proyecto, es crucial evitar sobrescribir los cambios de otros sin querer. Si bien es posible subir cambios directamente a la rama **main**, esto puede ocasionar la pérdida de cambios no sincronizados con el equipo. Para evitarlo, se recomienda trabajar en **ramas separadas** y, después, combinar esos cambios en una **revisión previa** utilizando **pull requests**.

Un **pull request** (PR) es una notificación que se envía al equipo, informando sobre los cambios realizados en una rama específica. Cualquier miembro del equipo puede revisar esos cambios, un proceso conocido como **code review**. Una vez que los cambios son aprobados por el equipo, el PR se cierra y los cambios se fusionan con la rama **main**.

![Pull request](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/pull_request.png "Pull request")

## ✅ Buen hábito: Crear ramas para trabajar

Un buen hábito es crear una **rama** dedicada para cada tarea o conjunto de cambios. Por ejemplo, al editar el **README**, es recomendable:

1. Crear una nueva rama para trabajar en los cambios.
2. Realizar los cambios en el entorno local.
3. Subir esos cambios tanto al repositorio local como remoto utilizando el comando **git push** hacia la rama recién creada.

## 📝 Crear el Pull Request

Una vez que los cambios están listos y sincronizados, dirígete al repositorio en GitHub, selecciona la rama creada y haz clic en el botón **"Pull Request"**. Aquí, deberás:

- Colocar un **título** claro y descriptivo del PR.
- Escribir una **descripción detallada** de los cambios realizados en ese código.

Recuerda ser lo más detallado posible para facilitar la revisión del equipo.

Luego de crear el PR, GitHub verificará si existen **conflictos** entre las ramas. El siguiente paso es esperar a que un miembro del equipo valide el PR. Si el código es aprobado, se **fusionará** con la rama **main**. Finalmente, se eliminará la rama de trabajo una vez que el PR haya sido completado y fusionado.
