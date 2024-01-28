# Codespaces-un-aprendizaje
Mi acercamiento a codespaces de Github para programar incluso desde una tablet. Con todos los obstaculos que pueden aparecer.
Parti de analizar la documentacion oficial de Github.

# Motivacion
Me compre una tablet para la facultad y busco maneras de ampliar los usos que le puedo dar. En principio la uso para tomar notas con samsung notes, posteriormente incorpore MS 365 para estudiantes y asi poder usar excel lo mas copmpleto posible, siendo que la use en materias como economia. Ahora busco integrar la posibilidad de programar sin grandes dificultades obviando la necesidad de ir con mi computadora de un lado a otro. Quedaria pendiente las aplicaciones de autodesk pero no me resulta inquietante dado que para eso cuento con mi notebook y no pienso sobre exigir las capacidades de mi tablet.

# Programar desde un navegador
Desde un repositorio de github, cambiando la url de ".com" a ".dev" o simplemente clickeando la tecla '.' se inicializa el repo en un VS Code Web.
Desde aqui se trata de abrir una terminal y solicita abrir un codespace.

## Consideraciones
### core-hours
Disponemos de una cantidad de horas de procesamiento por nucleo, en el marco de la suscripcion a github students son 180h/core. Y el minimo de uso aplicado esta en una maquina virtual de 2 Cores.
Con lo cual utilizando la menor cantidad de recursos (8gb RAM, 32gb Almacenamiento y 2 cores) disponemos de 90hs de codespace. Bajo mi disponibilidad de tiempo serian 4h diarias promedio de lunes a viernes, y en funcion de mi disponibilidad horario cumple con mis necesidades.

# Algunos problemas 

## Extensiones 
Una vez que se inicializa el VS Code Web, si no se instancia el codespace no se puede descargar casi ninguna extension, ni siquiera algo tan basico como live server. 

### Investigar:

- VS Code Web, que fallas tiene y como solucionarlas, desde la tablet escribe raro.
- Impactar un template de un codespace de django en el homebanking y la documentacion relacionada. En la que presenta github simplifica mucho la inicializacion de la app. ahorra muchas pasos y establece acciones automaticas para ejecutar la app sin tantos pasos previos desde un json.


### git
Use the VS Code terminal to commit the file change by entering the following commit message:
```shell
git commit -a -m "Adding hello from the codespace!"
```
Push the changes back to your repository. From the VS Code terminal, enter:
```shell
git push
```
- Cuantos codespaces puedo crear, como crear plantillas y customizarlas con las extensiones predefinidas.
Profundizar dev container
- Que limitaciones hay en cuanto al uso y cuando empieza a ser pago. Github students y codesspaces y github pro.
Github copilot
MS 365 copilot
Notion


### complementar codespaces:
https://dotfiles.github.io/tutorials/
https://code.visualstudio.com/docs/editor/settings-sync
https://docs.github.com/en/codespaces/customizing-your-codespace



# Relacion entre codespaces, contenedores, deploy
ALgun punteo de cosas interesantes de la docu de codespaces:
Git partial clone y Shallow clone

Un detalle: para implementar un codespace que ejecute django la plantilla especifica en su dev container los hostrequirement, a lo cual figura cpus: 4 (cores). Es valido reducirlo a 2? fuera de velocidad tiene otras consecuencias?

## Git Hooks: 
Dentro del devcontainer.json se especifican varias cosas como por ejemplo la VM que ocupara el codespace (Hay mejores? y costos agregados?), entiendase


## Add a custom image to your codespace!
You can configure the development container for a repository so that any codespace created for that repository will give you a tailored development environment, complete with all the tools and runtimes you need to work on a specific project.

**What are development containers?** Development containers, or dev containers, are Docker containers that are specifically configured to provide a fully featured development environment. Whenever you work in a codespace, you are using a dev container on a virtual machine.

A dev container file is a JSON file that lets you customize the default image that runs your codespace, VS code settings, run custom code, forward ports and much more!

## Add a .devcontainer.json file to customize your codespace
1. Navigating back to your **Code** tab of your repository, click the **Add file** drop-down button, and then click `Create new file`.
1. Type or paste the following in the empty text field prompt to name your file.

   ```
   .devcontainer/devcontainer.json
   ```

1. In the body of the new **.devcontainer/devcontainer.json** file, add the following content:

   ```jsonc
   {
     // Name this configuration
     "name": "Codespace for Skills!",
     // Use the base codespace image
     "image": "mcr.microsoft.com/vscode/devcontainers/universal:latest",

     "remoteUser": "codespace",
     "overrideCommand": false
   }
   ```

1. Click **Commit changes** and then select **Commit changes directly to the `main` branch**.
1. Create a new codespace by navigating back to the **Code** tab of your repository.
1. Click the green **Code** button located in the middle of the page.
1. Click the **Codespaces** tab on the box that pops up.
1. Click the **Create codespace on main** button OR click the `+` sign on the tab. This will create a new codespace on the main branch. (Notice your other codespace listed here.)

   > Wait about **2 minutes** for the codespace to spin itself up.

1. Verify that your new codespace is is running, as you did previously.

   Note the image being used is the default image provided for GitHub Codespaces. It includes runtimes and tools for Python, Node.js, Docker, and more. See the full list here: https://aka.ms/ghcs-default-image. Your development team can use any custom image that has the necessary prerequisites installed. For more information, see [codespace image](https://aka.ms/configure-codespace).
