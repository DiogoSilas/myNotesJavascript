Vamos ver sobre essas 2 funções do JavaScript: **setInterval()** e **setTimeout()**;  ambas são [[Higher Order Functions - JavaScript]] e métodos do elemento window.

**setTimeout(function, milliseconds):** Executa uma função, depois de aguardar um número especificado de milissegundos.
**setInterval(function, milliseconds):** O mesmo que setTimeout(), mas repete a execução da função continuamente.

Os parâmetros de tempo são indicados no formato de milissegundos:
>1s = 1000
>2s = 2000
>3s = 3000
>4s = 4000
>...
#### Exemplo setTimeout():
```js
setTimeout(function() {
	alert.('Olá mundo!')
}, 3000)
```
O alerta aparecerá após três segundos.

#### Exemplo setInterval():
```js
setInterval(() => {}, interval);

setInterval(() => {
	console.log('Executando a cada 2 segundos')
}, 2000);
```
Abra o dev. tools para ver a execução deste exemplo.

#### Parar o setInterval():
```js
const idDoIntervalo = setInterval(() => {
					console.log('Executando a cada 2 segundos')
				}, 2000);
console.log(idDoIntervalo)
clearInterval(idDoIntervalo)
```

Adicionamos o parâmetro **clearInterval()** e o identificador que contem o bloco de código do **setInterval()**  para parar a execução.

#### Parar o setTimeout():
O método é o mesmo  do **setInterval()** para parar o **setTimeout()**, mas temos que adicionar o **clearTimeout()**:
```js
const idDoIntervalo = setTimeout(function() => {
					alert.('Olá mundo!')
				}, 3000)

console.log(idDoIntervalo)
clearTimeout(idDoIntervalo)
```

---
Fontes:
- https://www.w3schools.com/js/js_timing.asp
Tags: #softwaredevelopment 