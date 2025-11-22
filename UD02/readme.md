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