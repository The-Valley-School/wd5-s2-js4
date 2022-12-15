Podemos realizar pequeños templates en javascript e ir añadiendo o quitando dichos elementos a nuestro gusto o necesidades.


```jsx
let name = 'Edu';
let job = 'Profesor';

// old school
console.log('Hola mi nombre es ' + name + ' y trabajo de ' + job);
// new wave
console.log(`my name is ${name} and my job is ${job}`);

// Add to HTML
const contentApp = document.querySelector('div');
let html = `<ul>
	<li>name: ${name}</li>
	<li>job: ${job}</li>
</ul>`;
contentApp.innerHTML = html;
```