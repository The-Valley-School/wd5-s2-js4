### **Timeout**

El método **setTimeout()** establece un **temporizador** que ejecuta una función o una porción de código después de que transcurra el tiempo indicado en **milisegundos**. El valor **devuelto** por la función **setTimeout()** es **numérico** e identifica el temporizador creado con la llamada a **setTimeout()**. Este valor puede pasarse a la función **clearTimeout()** para cancelar el temporizador. Veamos un ejemplo con código.


```jsx
let mensaje = () => {
    console.log("Hola Mundo");
}
  
const timeoutId = setTimeout(mensaje, 3000);
clearTimeout(timeoutId);
```


### **Intervalos**

Función muy parecida a la anterior salvo que su **comportamiento** se repite en forma de **bucle**: **setInterval()** ejecuta una función o un fragmento de código que recibe por parámetro de forma repetitiva cada vez que termina el periodo de tiempo determinado (también en milisegundos). 


```jsx
let mensaje = () => {
    console.log("Hola Mundo");
}
  
const timeoutId = setInterval(mensaje, 3000);
clearTimeout(timeoutId);
```