De igual manera que podemos acceder a un elemento del DOM, podemos crear, añadir propiedades y modificar esos elementos.


### **createElement(name)**

Nos permitirá crear un nombre con el elemento que le pasemos por parámetro.


```jsx
let elementTitulo = document.createElement('h1');
```


### **appendChild(node)**

Agrega un nuevo nodo al final de la lista de un elemento hijo de un elemento padre especificado.


```jsx
elementPadre.appendChild(elementHijo);
```


Vamos a crear por ejemplo, un título que vamos a añadir a un div:


```jsx
let elementoPadre = document.getElementById('containter');
let elementoHijo = document.createElement('h1');

elementoPadre.appendChild(elementoHijo);
```


```html
<body>
	<div id="containter">
	</div>
</body>
```


### **createTextNode(text)**

Nos permitirá crear un nodo de texto que puede ser añadido a un elemento HTML


```jsx
let newText = document.createTextNode('HOLA');
let p1 = document.getElementById("p1");

p1.appendChild(newtext);
```
 

### innerHTML

Podemos también usar directamente valores de propiedad para incluir textos


```jsx
let newText = document.createElement('h1');
let newText = document.createElement('h1');
newText.innerHTML = 'AAAAA';

let a = document.getElementById('a').appendChild(newText);
```


### insertBefore / insertAdjacentHTML

Con **insertBefore** podemos añadir el elemento antes de otro elemento que decidamos:

 
```html
<div id="parentElement"><span id="childElement">prueba</span></div>
```

```jsx
let newNode = document.createElement("span");
newNode.innerHTML ='Souy una ';
let parentDiv = document.getElementById("parentElement");

let sp2 = document.getElementById("childElement");
parentDiv.insertBefore(newNode, sp2);
```


Con **insertAdjacentHTML** podemos introducir un trozo de código


```html
<div id="parentElement"><span id="childElement">prueba</span></div>
```

```jsx
let div1 = document.getElementById('parentElement');
div1.insertAdjacentHTML('beforebegin', '<div><p>Holaaa</p></div>');

// beforebegin - insertado justo antes del elemento, a la misma altura .
// afterbegin - insertado dentro del elemento, antes del primer hijo.
// beforeend - insertado dentro del elemento, después del último hijo.
// afterend - insertado justo después del elemento, a la misma altura.
```
  

### r**emoveAttribute(attribute)**

Elimina el atributo seleccionado del nodo que le llama.


```html
<div id="parentElement"><span id="childElement">prueba</span></div>
```

```jsx
let div1 = document.getElementById('parentElement');
div1.removeAttribute('id');
```
   

### **removeChild(child)**

Elimina el hijo seleccionado


```html
<div id="parentElement"><span id="childElement">prueba</span></div>
```

```jsx
let parentNode = document.getElementById('parentElement');
let childNode = document.getElementById('childElement');
parentNode.removeChild(childNode);
```
 

### **replaceChild(new, old)**

Cambia el hijo


```html
<div id="parentElement"><span id="childElement">prueba</span></div>
```


```jsx
let parentNode = document.getElementById('parentElement');
let childNode = document.getElementById('childElement');
let newChildNode = document.createElement('h1');
newChildNode.innerHTML = 'AAA';
parentNode.replaceChild(newChildNode, childNode);
```

   