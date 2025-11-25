# 🌐 Trabajar con Repositorios Remotos

![Comandos de repositorios remotos](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/remote_commands.png "Comandos de repositorios remotos")

## 📤 Git Push

**Sube el contenido del repositorio local al repositorio remoto.**  

Para sincronizar los cambios hechos en tu entorno local, puedes usar **Visual Studio Code**. Una vez que hayas guardado los cambios en tu entorno local, VS Code puede subir automáticamente los cambios al repositorio remoto.

![Push VS Code](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/push_vs_code.png "Push VS Code")

También puedes hacerlo desde la terminal usando el siguiente comando:

```bash
git push -u origin main
```

Aquí, el flag `-u` establece que la rama remota **origin/main** será la rama por defecto para los futuros `git push`. Esto te permite usar simplemente:

```bash
git push
```

Aunque si existe una rama `main` en el repositorio remoto, Git subirá los cambios a esta rama de todos modos si omites el `-u origin main`. Sin embargo, por seguridad, es recomendable usar el comando completo.

## 📥 Git Pull

**Obtén el contenido actualizado del repositorio remoto y actualiza tu repositorio local.**  

Imagina que alguien más editó el archivo **README.md** en el repositorio remoto. Puedes ver esos cambios editando directamente en la web y haciendo el commit desde allí:

![Web Commit](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/web_commit.png "Web Commit")

Una vez realizado el commit, los cambios aparecerán reflejados en la interfaz de **VS Code** con una flecha hacia abajo, lo que indica que hay actualizaciones para sincronizar:

![Web Commit](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/web_commit2.png "Web Commit")

Puedes actualizar tu repositorio local con el siguiente comando:

```bash
git pull
```

Este comando traerá las actualizaciones desde la rama `main` del repositorio remoto por defecto. Ten en cuenta que **no puedes hacer un `git push` si el repositorio remoto no está sincronizado con tu repositorio local**. Siempre debes realizar un `git pull` antes de hacer un `git push`.

## 📥 Git Fetch

**Obtén los cambios del repositorio remoto sin fusionarlos automáticamente con tu repositorio local.**  

Si has hecho cambios en el repositorio remoto desde la web, puedes comprobar el estado de tu repositorio con:

```bash
git status
```

Si no hay cambios locales que necesiten ser subidos, puedes usar el siguiente comando para obtener los cambios desde el repositorio remoto sin fusionarlos automáticamente:

```bash
git fetch origin
```

A diferencia de `git pull`, `git fetch` solo descarga los cambios, pero no los fusiona inmediatamente. Esto te permite revisar qué cambios han sido realizados antes de decidir si deseas aplicarlos.

Para ver los cambios, puedes usar el siguiente comando:

```bash
git log main..origin/main
```

Esto te mostrará los commits del repositorio remoto que aún no se han aplicado en tu repositorio local. Ejemplo:

```plaintext
commit fd360f6b6b73a3ef37d42e51bdc4d423d495190a (origin/main)
Author: Josué Say <106031855+JosueSay@users.noreply.github.com>
Date:   Wed Dec 11 11:57:42 2024 -0600

    Update README.md
```

Si decides que deseas aceptar esos cambios, puedes fusionarlos con el siguiente comando:

```bash
git merge origin/main
```

Esto fusionará la rama remota con la local, permitiéndote decidir si deseas aceptar o no esos cambios.
