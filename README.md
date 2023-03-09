# _guanabana__scss

Normalizador de estilos en etiquetas de HTML con variables configurables para la creación de clases, creación de temas de color, retículas (grid) y funciones de accesibilidad. 
Para creacion y configuracion de sistemas de diseño a medida.


*Este proyecto fue construido con [sass](https://sass-lang.com/dart-sass) 1.57.1*

*El entorno de desarrollo se levanta con [node](https://nodejs.org/en/) 18.13.0*




## ambiente local
Clona el repositorio
```ssh
git clone git@github.com:flkt/_guanabana__scss.git
```

Instala las dependencias
```ssh
npm install
```

Levanta el entorno local
```ssh
npm run dev
```

Abre cualquier navegador con la ruta `http://localhost:3000/`




## para compilar los archivos de distribución

Genera el archivo sin comprimir
```ssh
npm run build
```

ó el archivo minificado con

```ssh
npm run build-compress
```




## estructura

```text
index.js   <- solo pa levantar el entorno local
_guanabana.scss  
├── dist/
    _guanabana.css
    _guanabana.css.map
├── docs/  <- pa ver como se ven los estilos al final
    index.html
└── src/
    _base.scss  <-  estilos generales o que comparten varias etiquetas
    _variables_accesibilidad.scss  <-  variables de css que se necesitan editar al vuelo para crear las herramientas de accesibilidad
    _variables_color.scss  <-  variables de color de cualquier etiqueta, clase, spseudo clase
    _variables_generales.scss  <-  variables para homologar, crear arreglos de clases y un monton de cosas mas. (quizas deberia dividirla.. jeje)
    ├── elemento/
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
