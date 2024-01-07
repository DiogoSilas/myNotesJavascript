
Estrutura da repetição que serve para percorrer [[Array - JavaScript]]

O método **forEach()** executa uma dada função em cada elemento de um array.

#### Sintaxe:
```js
arr.forEach(callback(currentValue [, index [, array]])[, thisArg]);
```

[[Função Callback]] - Função para executar em cada elemento, é invocado com três argumentos:
1. currentValue: O **valor atual** do elemento sendo processado no [[Array - JavaScript]].
2. index: O índice do elemento atual sendo processado no [[Array - JavaScript]].
3. [[Array - JavaScript]]: O array que **forEach()** está sendo aplicado.

O **forEach()** executa o **callback** fornecido uma vez para cada elemento da ordem com um valor atribuído.

```js
const array1 = ['a', 'b', 'c'];

array1.forEach((element) => console.log(element));

// Expected output: "a"
// Expected output: "b"
// Expected output: "c"
```
---
Fontes:
- https://youtu.be/Q3tiAEvWhOE?si=cutND_3AcZpXVJpI
Tags: #softwaredevelopment 