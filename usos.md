Codespaces/Solución de problemas/Clientes de codespaces
Solución de problemas de clientes de GitHub Codespaces
En este artículo
Solución de problemas del cliente web de Visual Studio Code
En este artículo se proporciona información para solucionar problemas que puedes encontrar con el cliente que usas para GitHub Codespaces.

Tool navigation
JetBrains IDEs (Beta)
Visual Studio Code
Web browser
Solución de problemas del cliente web de Visual Studio Code
Si tienes problemas al usar GitHub Codespaces en un explorador que no está basado en Chromium, intenta cambiar a un explorador basado en Chromium, como Google Chrome o Microsoft Edge. De forma alternativa, puedes buscar incidencias conocidas con el explorador en el repositorio microsoft/vscode; para ello, busca incidencias etiquetadas con el nombre del explorador, como firefox o safari.

Si tienes problemas al usar GitHub Codespaces en un explorador basado en Chromium, puedes comprobar si experimenta otra incidencia conocida con VS Code en el repositorio microsoft/vscode.

Diferencias al trabajar en VS Code localmente
Al abrir un codespace en el explorador, con el cliente web de VS Code, observarás algunas diferencias con respecto a trabajar en un área de trabajo local en la aplicación de escritorio de VS Code. Por ejemplo, algunas uniones de teclas serán diferentes o no estarán y algunas extensiones podrían comportarse de forma diferente. Para obtener un resumen, consulta: "Limitaciones conocidas y adaptaciones" en la documentación de VS Code.

Puedes comprobar si hay incidencias conocidas y registrar nuevas incidencias con la experiencia de VS Code en el repositorio microsoft/vscode.

Visual Studio Code Insiders
Visual Studio Code Insiders es el lanzamiento más frecuente de VS Code. Tiene todas las características y correcciones de errores más recientes, pero también podría contener, ocasionalmente, problemas nuevos que podrían dar como resultado una compilación rota.

Si estás utilizando una compilación de Insiders y notas un comportamiento anormal, te recomendamos cambiar a la versión estable de Visual Studio Code e intentarlo de nuevo.

Haz clic en  en la parte inferior izquierda del editor y selecciona Cambiar a versión estable... . Si el cliente web de VS Code no se carga o  no está disponible, puedes forzar el cambio a Visual Studio Code estable si anexas ?vscodeChannel=stable a la dirección URL de tu codespace y lo cargas en ella.

Si la incidencia no se ha corregido en Visual Studio Code Estable, comprueba si hay incidencias conocidas y, si es necesario, registra una nueva incidencia con la experiencia de VS Code, en el repositorio microsoft/vscode.

Solución de problemas de Simple Browser
Cuando hayas iniciado una aplicación web en un codespace, puedes obtener una vista previa de la aplicación en ejecución en el explorador Simple Browser insertado en VS Code. En algunos proyectos, la aplicación se abre automáticamente en una pestaña de Simple Browser en el editor cuando se inicia la aplicación. Esto sucede si, en el archivo de configuración devcontainer.json del codespace, la propiedad onAutoForward del puerto en el que se ejecuta la aplicación está establecida en openPreview.

"portsAttributes": {
  "3000": {
    "label": "Application",
    "onAutoForward": "openPreview"
  }
}
Si la pestaña de Simple Browser no se abre automáticamente, puedes abrir Simple Browser de forma manual para ver la aplicación.

En VS Code, haz clic en la pestaña Puertos.

Haz clic con el botón derecho en el puerto y, luego, haz clic en Vista previa en el Editor.
