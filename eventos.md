Toca repasar eventos, como ya sabéis, los evento nos van a permitir que dada una acción, lancemos las funciones que les indiquemos. Por ejemplo, tenemos eventos de:

- **RATÓN**: Hacer click [click], pasar el ratón sobre un elemento [mouseover], sacar el ratón de un elemento [mouseout] …
- **TECLADO**: Cuando pulsamos por ejemplo una tecla [keypress]…
- **ELEMENTOS**: Cuando quitamos el foco [blur], lo ponemos [focus], cambiamos el contenido de un output [change]…
- **FORMULARIOS**: Cuando pulsamos el [submit] o el [reset]…
- **VENTANA:** Un cambio de tamaño [resize] o un scroll [scroll]

**onclick**

La forma más fácil de trabajar con el elemento CLICK es mediante el atributo **onclick** en HTML. 

Lo podemos usar en cualquier etiqueta, no hace falta que sea un botón.

```html
<body>
	<p>Si pulsas en el botón saldrá un mensaje por consola</p> 
	<button onclick="mensajeConsola()">Haz click</button>
</body>
```

```jsx
function mensajeConsola () {
	console.log('Aquí está el mensaje por consola');
}
```

**eventListener**

Otra manera de tratar con eventos en JS sería mediante el uso de eventListeners, escuchadores de eventos. Lo que hacemos con ello es dejar preparada una función que salta cuando se produzca ese evento. Por ejemplo:

```html
<body>
	<p>Si pulsas en el botón saldrá un mensaje por consola</p> 
	<button id="btn">Haz click</button>
</body>
```

```jsx
function mensajeConsola () {
	console.log('Aquí está el mensaje por consola');
}

document.getElementById("btn").addEventListener("click", mensajeConsola);
```

A nivel de buenas prácticas, deberíamos usar estos eventos en lugar de el onclick y así mantener

toda la lógica en javascript.

En caso de que quisiésemos pasar argumentos mediante la función dentro del addEventListener debemos usar una función anónima para ello:

```jsx
document.getElementById("btn").addEventListener("click", funcion () { mensajeConsola ('Hola') });
```
