# 🛡️ Gestión de Datos Sensibles y Políticas de Seguridad

## 🔍 Code Scanning

GitHub permite analizar tu código en busca de vulnerabilidades mediante la herramienta **CodeQL Analysis**:

1. Ve a **Settings > Code security**.
2. En **Code Scanning**, selecciona **Set Up** en Tools.
3. Usa la configuración **default** para analizar el código y ajustar parámetros.

![Code Scanning](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/code_scanning.png "Code Scanning")

## 🔑 Secret Scanning y Protección de Commits

Habilita la opción de **Secrets Scanning** para recibir alertas sobre:

- Llaves API.
- Tokens.
- Secretos filtrados en el código.

Activa también **Push Protection** para prevenir la inclusión de secretos en commits futuros.

![Secret Scanning](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/secret_scanning.png "Secret Scanning")

## 🟡 Flujos de Seguridad Activos

Cada vez que subes cambios, GitHub ejecuta flujos de análisis. Esto se identifica con un indicador amarillo en el encabezado del repositorio. En el apartado de **Security**, se listan las vulnerabilidades detectadas en tres categorías:

1. **Dependabot**: Alertas relacionadas con dependencias desactualizadas o vulnerables.
2. **Secret Scanning**: Detección de secretos o llaves filtradas.
3. **Code Scanning**: Análisis estático del código para detectar vulnerabilidades.

![Security](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/security.png "Security")

## 🛠️ Resolución de Vulnerabilidades

Cuando GitHub detecta problemas de seguridad, proporciona información detallada y pasos para solucionarlos. Algunas recomendaciones incluyen:

1. **Regenerar Llaves o Tokens:**
   - Elimina el token comprometido y genera uno nuevo.
   - Eliminar solo la línea del código no soluciona el problema, ya que permanece en el historial de Git.

2. **Modificar el Código:**
   - Ajusta el código para evitar futuras filtraciones.

![Security Breach](https://raw.githubusercontent.com/JosueSay/ImageDocs/main/Git_GitHub_Documentation/security2.png "Security Breach")

> **Nota:** Aunque GitHub identifica muchas llaves y secretos, no es infalible. Usa un `.gitignore` para evitar exponer archivos sensibles y nombra las claves de forma que no sean fácilmente reconocibles.

## ⚡ Recomendaciones Finales

1. **Habilita todas las herramientas de seguridad disponibles en GitHub.**
2. **Mantén un `.gitignore` actualizado y bien configurado.**
3. **Evita exponer datos sensibles en commits.** Usa secretos gestionados y variables de entorno.
4. **Revisa periódicamente las alertas de seguridad y sigue las recomendaciones.**
