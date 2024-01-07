Nos permite representar um numero indefinido de argumentos como parâmetros de uma função. Este parâmetro **rest** será interpretado como um [[Array - JavaScript]].

Recomendado quando não ter noção de quantos parâmetros vai ser passado dentro de uma function.

#### Sintaxe:
```js
function(a, b, ...args) {
	...
}
```

#### Exemplo:
```js
function incentivarQuester(mensagem, ...nomesQuesters) {
	nomesQuesters.map(nomeQuester => console.log(`${mensagem} ${nomesQuesters}`))
}

incentivarQuester('Parabens por ter chegado ao módulo de JavaScript avançado', 'Diogo', 'João', 'Pedro')
```

Links:
- [[Map - trabalhar com arrays]]
- [[Interpolando strings]]

---
Fontes: https://medium.com/@shubham3480/rest-and-spread-operator-in-javascript-3950e16079c8
Tags: #softwaredevelopment 