O método push() adiciona um ou mais elementos ao final de um [[Array - JavaScript]] e retorna o novo comprimento desse array.
### Sintaxe:
```js
array.push(elemento1, ..., elementoN)
```
#### Exemplos:
```js
var numeros = [1, 2, 3];
numeros.push(4);

console.log(numeros); // [1, 2, 3, 4]

numeros.push(5, 6, 7);

console.log(numeros); // [1, 2, 3, 4, 5, 6, 7]
```
#### Função com dois [[Array - JavaScript]]:
```js
var vegetais = ["cenoura", "batata"];
var maisVegetais = ["aipo", "beterraba"];

// Adiciona o segundo array no primeiro
// Equivalente a vegetais.push('aipo', 'beterraba');
Array.prototype.push.apply(vegetais, maisVegetais);

console.log(vegetais); // ['cenoura', 'batata', 'aipo', 'beterraba']
```
Nota: Sobre o [[Function.prototype.apply()]].

---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/push

Tags: #softwaredevelopment 