# _design_system

Biblioteca editable de estilos base para crear sistemas de diseño. 

Este proyecto fue construido con node v18.13.0


## ambiente local
Clona el repositorio
`git clone git@github.com:flkt/_design_system.git`

Instala las dependencias
`npm install`

Levanta el entorno local
`npm run dev`

`http://localhost:3000/`


## notas

### texto tamaño accesible
La única variable que se debería tener que editar para ajustar el tamaño deberia ser `--main-font-size` en el archivo `_variables_accesibilidad.scss`

Para lograrlo, se necesitan utilizar todas las demás variables de tamaño de tipografía en `rem` para elementos en bloque y `em` para elementos en linea; esto para que cuando cambie la variable de tipogragía base, por el menú accesibilidad, las tipografías de todos los elementos se reajusten y no tener que sobreescribir todas las demás.

Se resetearon a `1rem` todos los heading, para evitar el uso de la etiqueta como estilo en lugar de semántica.
