Poder copiar um [[Array - JavaScript]] sem modificar o array original.
#### Exemplo:
```js
const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];

console.log(animals.slice(2));
// Expected output: Array ["camel", "duck", "elephant"]

console.log(animals.slice(2, 4));
// Expected output: Array ["camel", "duck"]

console.log(animals.slice(1, 5));
// Expected output: Array ["bison", "camel", "duck", "elephant"]

console.log(animals.slice(-2));
// Expected output: Array ["duck", "elephant"]

console.log(animals.slice(2, -1));
// Expected output: Array ["camel", "duck"]

console.log(animals.slice());
// Expected output: Array ["ant", "bison", "camel", "duck", "elephant"]
```

### Sintaxe:
```js
slice()
slice(start)
slice(start, end)
```
---
Quando o segundo parâmetro não é definido, o **slice** pegara todos os valores até o final o [[Array - JavaScript]].
```js
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1, 3);

// fruits contains ['Banana', 'Orange', 'Lemon', 'Apple', 'Mango']
// citrus contains ['Orange','Lemon']
```
O **segundo parâmetro (end)** não possui o valor atribuídos a ele incluso na seleção dos conteúdos do array.
>Pegue todos até "X", mas não adicione "X".

---
Fontes:
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice

Tags: #softwaredevelopment 