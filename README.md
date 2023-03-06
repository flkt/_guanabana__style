# _design_system__scss

Biblioteca editable de estilos base para crear sistemas de diseño. 

*Este proyecto fue construido con [node](https://nodejs.org/en/) 18.13.0 y [sass](https://sass-lang.com/dart-sass) 1.57.1*


## ambiente local
Clona el repositorio
```ssh
git clone git@github.com:flkt/_design_system__scss.git
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


## notas

### texto tamaño accesible
La única variable que se debería tener que editar para ajustar el tamaño deberia ser `--main-font-size` en el archivo `_variables_accesibilidad.scss`

Para lograrlo, se necesitan utilizar todas las demás variables de tamaño de tipografía en `rem` para elementos en bloque y `em` para elementos en linea; esto para que cuando cambie la variable de tipogragía base, por el menú accesibilidad, las tipografías de todos los elementos se reajusten y no tener que sobreescribir todas las demás.

Se resetearon a `1rem` todos los heading, para evitar el uso de la etiqueta como estilo en lugar de semántica. Peeeeeero en caso de que seas bien chingona y prefieras utilizar las etiquetas ya con los estilos finales finalazos, puedes agregar los tamaños para cada etiqueta en el archivo `_variables_generales.scss` en el arreglo de la variable `$heading-font` agregando cada etiqueta, ej. `h1` en el sub-arreglo de `elements`.
