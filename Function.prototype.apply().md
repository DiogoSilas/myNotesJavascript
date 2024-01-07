Utiliza **apply()** para adicionar todos os elementos de um [[Array - JavaScript]] para outro [[Array - JavaScript]].

#### Exemplo:
```js
var vegetais = ["cenoura", "batata"];
var maisVegetais = ["aipo", "beterraba"];

// Adiciona o segundo array no primeiro
// Equivalente a vegetais.push('aipo', 'beterraba');
Array.prototype.push.apply(vegetais, maisVegetais);

console.log(vegetais); // ['cenoura', 'batata', 'aipo', 'beterraba']
```

---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Function/apply

Tags: #softwaredevelopment 