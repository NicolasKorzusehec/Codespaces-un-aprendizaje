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
