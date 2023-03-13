# _guanabana__style

Normalizador de estilos en etiquetas de HTML con variables configurables para la creación de clases, creación de temas de color, retículas (grid) y funciones de accesibilidad. 
Para creacion y configuracion de sistemas de diseño a medida.



## UTILIZAR ESTE REPO EN OTRO PROYECTO
instala el repositorio en tu proyecto
```zsh
npm i git@github.com:flkt/_guanabana__scss.git
```

si no necesitas modificarle nada importa el archivo de distribucion en el `main.js` de tu proyecto y listo
```js
import 'guanabana-style/dist/guanabana-style.css'
```

si necesitas cambiarle algun valor, color, tamaño, tipografia, reticula, etc...

  1. copia la carpeta de configuracion

  ```zsh
  cp -R 'node_modules/guanabana-style/config' 'src/styles/config'
  ```
  
  2. agregalo a la hoja general de estilos de tu proyecto
  ```css
  @import 'config/_config';
  @import 'node_modules/guanabana-style/src/_guanabana_style';
  ```

  3. modifica las variables de los archivos dentro de la carpeta `config/` como requieras 


## LEVANTAR EL ENTORNO LOCAL
Clona el repositorio
```zsh
git clone git@github.com:flkt/_guanabana__scss.git
```

Instala las dependencias
```zsh
npm install
```

Levanta el entorno local
```zsh
npm run dev
```

Abre cualquier navegador con la ruta `http://localhost:3000/`




## COMPILAR LOS ARCHIVOS DE DISTRIBUCION

Genera el archivo sin comprimir
```zsh
npm run build
```

ó el archivo minificado con

```zsh
npm run build-compress
```




## estructura

```text
index.js   <- solo pa levantar el entorno local
guanabana-style.scss  
├── dist/
    guanabana-style.css
    guanabana-style.css.map
├── docs/  <- pa ver como se ven los estilos al final
    index.html
    └── assets/
        └── css/
            guanabana-style.css
            guanabana-style.css.map
        └── img/
            guanavena-ico.png
            guanavena.png
├── config/
    _guanabana_config.scss  <-  carga todos los archivos de config/
    accesibilidad.css  <-  variables de css que se necesitan editar al vuelo para crear las herramientas de accesibilidad
    color.css  <-  variables de color de cualquier etiqueta, clase, spseudo clase
    adaptabilidad.scss  <-  arreglos de variables por dispositivo y breakpoints
    elemento.scss
    estructura.scss
└── src/
    _guanabana_styles.scss  <-  carga todos los archivos de src/
    ├── elemento/
        generales.scss  <-  estilos generales o que comparten varias etiquetas
        acordeon.scss
        boton.scss
        enlace.scss
        etiqueta.scss
        imagen.scss
        lista.scss
        menu.scss
        navegacion.scss
        tabla.scss
        texto.scss
        titulo.scss
    ├── estructura/
        contenedor.scss
        margen.scss
        reticula.scss
    └── formulario/
        TODO.md
```



## notas

### texto tamaño accesible
La única variable que se debería tener que editar para ajustar el tamaño deberia ser `--main-font-size` en el archivo `_variables_accesibilidad.scss`

Para lograrlo, se necesitan utilizar todas las demás variables de tamaño de tipografía en `rem` para elementos en bloque y `em` para elementos en linea; esto para que cuando cambie la variable de tipogragía base, por el menú accesibilidad, las tipografías de todos los elementos se reajusten y no tener que sobreescribir todas las demás.

Se resetearon a `1rem` todos los heading, para evitar el uso de la etiqueta como estilo en lugar de semántica. Peeeeeero en caso de que seas bien chingona y prefieras utilizar las etiquetas ya con los estilos finales finalazos, puedes agregar los tamaños para cada etiqueta en el archivo `_variables_generales.scss` en el arreglo de la variable `$heading-font` agregando cada etiqueta, ej. `h1` en el sub-arreglo de `elements`.




__

*Este proyecto fue construido con [sass](https://sass-lang.com/dart-sass) 1.57.1 || levantado con [node](https://nodejs.org/en/) 18.13.0 y [express](https://expressjs.com/) 4.18.2*
