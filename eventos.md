Una vez visto como  crear y añadir elementos al DOM, vamos a ver una serie de propiedades que podemos utilizar en nuestros desarrollos


### **element.textContent**

Nos permite introducir texto en nuestras etiquetas


```jsx
elementoHijo.textContent = 'Esto es un H1';
```


### **element.setAtributte()**

Que nos permite por ejemplo, incluir la url en una imagen:


```jsx
element.setAttribute('src', url);
```


### **element.style**

Nor permite cambiar el estilo:


```jsx
element.style.display = 'none';
```
 

### **element.classList.add() / element.classList.remove() / element.classList.toogle() / element.classList.contains() /**


```jsx
//element.classList.add()
elementoHijo.classList.add('bold-text', 'red-text');

//element.classList.remove()
elementoHijo.classList.remove('bold-text');

//element.classList.add()
elementoHijo.classList.toogle('visible');

//element.classList.contains()
elementoHijo.classList.contains('visible');
```
  

Los elementos tienen un montón de propiedades añadidas y algunas son muy interesantes


```jsx
// attributes: Nos devuelve el objeto con los atributos que posee un nodo
elemento.attributes

// className: Para conocer o cambiar el nombre de la clase
elemento.className

// classList: Listado de clases
elemento.classList

// id: Para conocer el id
elemento.id

// parentNode, childNodes, firstChild, lastChild, previousSibling, nextSibling: Para conocer elementos padres e hijos
elemento.childNodes...

// tagName: Devuelve la etiqueta HTML
elemento.tagName
```