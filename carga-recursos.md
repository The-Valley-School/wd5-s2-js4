El ciclo de vida de una página HTML tiene 3 eventos importantes:


### **DOMContentLoaded**

El navegador HTML está completamente cargado y el árbol DOM está construido, pero es posible que los recursos externos no se hayan cargado.


```html
<img id="img" src="https://thevalley.es/wp-content/themes/salient-child/imgs/streaming.jpg">
```

```jsx
document.addEventListener("DOMContentLoaded", () => console.log('DOM is ready | Image size: ' + img.offsetWidth + 'x' + img.offsetHeight));
```


**¿Qué pasaría si…?**


```html
<script>
	document.addEventListener("DOMContentLoaded", () => console.log('DOM is ready | Image size: ' + img.offsetWidth + 'x' + img.offsetHeight));
</script>
<script>
	console.log('¿Me cargo antes?');
</script>

<img id="img" src="https://thevalley.es/wp-content/themes/salient-child/imgs/streaming.jpg">
```
  

Esto ocurre ya que el DOM tiene que esperar a ve si alguno de los scripts modifica el DOM y por tanto el DOM no estará listo hasta que verifique tal cosa.


**¿Y qué pasa con las hojas de estilos?**

Pues DOMContentLoaded no las espera salvo que estén justo delante de un script ya que este puede hacer referencia a algo de esa hoja.



### LOAD

Ya se ha cargado el HTML y los recursos externos. El evento load en el objeto window se activa cuando se carga toda la página, incluidos estilos, imágenes y otros recursos. 
 

```html
<img id="img" src="https://thevalley.es/wp-content/themes/salient-child/imgs/streaming.jpg">
```

```jsx
window.onload = () => console.log('Page is ready | Image size: ' + img.offsetWidth + 'x' + img.offsetHeight);
```
  

### **Beforeunload**

El usuario se va a ir, todavía estamos a tiempo de mantener al usuario o preguntarle si quiere guardar los cambios


```jsx
window.addEventListener("beforeunload", function (event) {
    event.preventDefault();
});
```