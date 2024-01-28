## Solución de problemas de Simple Browser
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
