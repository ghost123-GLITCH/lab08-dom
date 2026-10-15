# lab08-dom

Bitacora de JavaScript interactivo: DOM, eventos y objetos

| Instruccion                  | Que cambio en la pantalla                                                   | Se mantiene al recargar (Si/No) |
| ---------------------------- | --------------------------------------------------------------------------- | ------------------------------- |
| textContent desde la consola | El título h1 cambió a "Hola desde la consola"                               | No                              |
| textContent desde app.js     | El título h1 cambió a "Hola TECSUP"                                         | Sí                              |
| style.color                  | El color del título h1 cambió a azul                                        | Sí                              |
| classList.add                | El fondo del párrafo "Este texto va a cambiar" se puso amarillo (destacado) | Sí                              |
| createElement + appendChild  | Se agregó "JavaScript" a la lista HTML y CSS                                | Sí                              |

| Tipo de evento | Que accion lo dispara                           | Cuanto suma por accion |
| -------------- | ----------------------------------------------- | ---------------------- |
| click          | Un solo clic izquierdo sobre el botón           | Suma 1                 |
| dblclick       | Dos clics izquierdos rápidos sobre el botón     | Suma 1                 |
| mouseover      | Pasar el puntero del mouse por encima del botón | Suma 1                 |

- **evento.type**: Muestra en la consola el nombre exacto del evento que ocurrió (por ejemplo, "click", "dblclick" o "mouseover").
- **evento.target**: Muestra en la consola el elemento HTML específico que recibió la acción (en este caso, el botón `<button id="btnSumar">Sumar 1</button>`).

| Prueba                                  | Que paso en la pantalla                                                   | Se recargo la pagina (Si/No) |
| --------------------------------------- | ------------------------------------------------------------------------- | ---------------------------- |
| Escribir en el campo nombre             | El saludo "Hola, ..." se actualiza letra por letra con el nombre escrito. | No                           |
| Enviar sin preventDefault               | El texto "Enviado" aparece un instante y desaparece, el campo se borra.   | Sí                           |
| Enviar con preventDefault, correo sin @ | Aparece el mensaje "Correo no valido: falta @" en color rojo.             | No                           |
| Enviar con preventDefault, correo con @ | Aparece el mensaje "Enviado: [correo]" sin formato de error.              | No                           |

| Objeto  | nombre    | precio | descripcion()         | conDescuento(0.25) |
| ------- | --------- | ------ | --------------------- | ------------------ |
| laptop  | "Laptop"  | 2500   | "Laptop - S/ 2500.00" | 1875               |
| mouse   | "Mouse"   | 45     | "Mouse - S/ 45.00"    | 33.75              |
| teclado | "Teclado" | 120    | "Teclado - S/ 120.00" | 90                 |
| monitor | "Monitor" | 680    | "Monitor - S/ 680.00" | 510                |

La ventaja de usar la clase es que el HTML se mantiene limpio y reutilizable. Si queremos agregar un nuevo producto (como el monitor), solo lo añadimos en JavaScript y el código se encarga de crear el elemento `<li>` y calcular su descripción automáticamente, sin tener que escribir HTML a mano por cada producto.

| Prueba          | Total que muestra la pagina           | Correcto (Si/No)                                                 |
| --------------- | ------------------------------------- | ---------------------------------------------------------------- |
| Cuaderno 12.50  | 12.50                                 | Sí                                                               |
| + Lapicero 3.20 | 15.70                                 | Sí                                                               |
| + Mochila 89.90 | 105.60                                | Sí                                                               |
| Sin Number()    | No se muestra el producto ni el total | No (Da error en consola `this.precio.toFixed is not a function`) |

| Pieza  | Linea de tu codigo donde aparece              | Para que sirve                                                         |
| ------ | --------------------------------------------- | ---------------------------------------------------------------------- |
| DOM    | `document.createElement("li");`               | Para crear un nuevo elemento de lista visualmente en la página.        |
| Evento | `formProducto.addEventListener("submit", ...` | Detecta cuando el usuario presiona "Agregar" o Enter en el formulario. |
| Objeto | `new Producto(prodNombre.value, ...);`        | Crea una instancia individual con el nombre y precio ingresados.       |
