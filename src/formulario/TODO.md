# formulario

* input
* output
* select
* textarea
* meter
* ::file-selector-button
* [type="button"], [type="submit"], [type="reset"]
* fieldset
* legend
* label
* radio
* checkbox
* switch


## ... esto es lo que habia empezado antes
```
// button, .boton, ::file-selector-button, [type="button"], [type="submit"], [type="reset"] {
//     background-color: var(--button-background-color);
//     border-color: var(--button-border-color);
//     display: inline-flex;
//     align-content: center;
//     align-items: center;
//     text-decoration: none;
// }

// button, .boton, fieldset, input, select, textarea, ::file-selector-button {
//     border-width: 1px; // const
//     border-style: solid; // const
//     border-color: #777; // let
//     border-radius: 3px; // const
// }
// ::file-selector-button {
//     // line-height: calc(2rem - 6px); // const
//     // margin: 2px; // const
//     border-width: 0 1px 0 0;
//     margin: 0;
// }

// input, output, select, textarea, meter, [disabled] {
//     background-position: calc(100% - .25rem) 50%;
//     background-repeat: no-repeat;
//     background-size: 1rem;
// }

// select {
//     appearance: none;
//     -moz-appearance: none;
//     -webkit-appearance: none;
//     background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' height='24' width='24' viewBox='0 0 24 24'%3E%3Cpath d='M 2 10 l 9 8 l 9 -8' fill='none' stroke='%23000' stroke-width='2'/%3E%3C/svg%3E");
//     padding: 2px 1.25rem 2px .5rem;
// }

```