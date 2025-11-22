# guia de inicio de sistemas informaticos

## Unidade 1

[Unidade 1](/UD01/introduccion.md)

## Unidade 2

[Unidade 2](/UD02/harwdware.md)
<br>

[Unidade 2 Conversiones](/UD02/conversiones.md)

## Unidade 3
 
```js
let x = 0;
let y= 2;
let z= x +y; // Total 2

```
```mermaid
flowchart TD
    A['Configurar usuario en Git']
    B['git config --global user.name TuNombre']
    C['git config --global user.email tuemail@example.com']

    D['Clonar repositorio remoto']
    E['git clone https://github.com/usuario/repositorio.git']

    F['Modificar o crear archivos en el proyecto']

    G['Ver estado de archivos']
    H['git status']

    I['Añadir archivos al staging']
    J['git add <archivo>']
   J2['git add . todos los archivos']
    K['Confirmar cambios en local']
    L['git commit -m mensaje del commit']
    M['Autenticarse con GitHub si es la primera vez']
    N['git remote set-url origin https://github.com/usuario/repositorio.git']
    O['git push origin main']
    P['Cambios visibles en GitHub']

    A --> B --> C --> D --> E --> F --> G --> H --> I --> J --> J2 --> K --> L --> M --> N --> O --> P
```
#### Cuando usar git push origin main?


* Después de hacer un commit en local Cada vez que confirmas cambios con git commit -m "mensaje", esos cambios solo están en tu repositorio local. Para que aparezcan en GitHub, necesitas hacer git push origin main.

* Cuando tu rama local está adelantada respecto al remoto Si git log muestra commits en HEAD -> main que no están en origin/main, significa que aún no los has subido. Ahí es cuando debes hacer el push.

* Al iniciar un proyecto nuevo Una vez que configuras el remoto (git remote add origin **URL** o git remote set-url origin **URL>**), el primer git push origin main sube todo tu historial al repositorio en GitHub.
  
```mermaid
  flowchart TD
    A[Configurar usuario<br> git config --global user.name / user.email<br> → Define tu identidad en los commits] --> B[Crear repositorio local<br> git init<br> → Inicializa un nuevo repositorio en tu carpeta]
    B --> C[Modificar archivos<br> → Edita o crea archivos en tu proyecto]
    C --> D[Ver estado<br> git status<br> → Muestra qué archivos están modificados o sin seguimiento]
    D --> E[Agregar al staged<br> git add <archivo> / .<br> → Prepara archivos para el commit]
    E --> F[Guardar cambios<br> git commit -m 'mensaje'<br> → Crea una instantánea del proyecto]
    F --> G[Historial<br> git log<br> → Lista los commits realizados]
    G --> H[Crear ramas<br> git branch <nombre><br> → Crea una nueva rama]
    H --> I[Cambiar de rama<br> git checkout / git switch<br> → Mueve el trabajo a otra rama]
    I --> J[Fusionar ramas<br> git merge <rama><br> → Une cambios de una rama en otra]
    J --> K[Conectar con remoto <br> git clone / git remote -v <br> → Clona o enlaza repositorios en GitHub]
    K --> L[Enviar cambios<br> git push origin main<br> → Sube commits al remoto]
    K --> M[Traer cambios<br> git pull / git fetch<br> → Descarga y aplica cambios del remoto]
    L --> N[Autenticación<br> Token PAT / Claves SSH<br> → Métodos seguros para conectarse a GitHub]
    N --> O[Fork en GitHub <br> → Copia un repositorio en tu cuenta]
    O --> P[Crear rama en fork<br> git checkout -b <rama><br> → Rama específica para tus cambios]
    P --> Q[Subir rama <br> git push -u origin <rama> <br> → Envía tu rama al fork]
    Q --> R[Pull Request<br> → Solicita integrar tus cambios en el repositorio original]
```