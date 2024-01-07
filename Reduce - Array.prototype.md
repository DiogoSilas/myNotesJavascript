Use **reduce()** quando: é preciso encontrar um valor cumulativo ou concatenado com base em elementos de todo o [[Array - JavaScript]].

 O **reduce** recebe dois parâmetros:
 1. O primeiro valor é o valor anterior;
 2. Elemento atual ou valor atual.

```js
const exemplo = array.reduce((prevVal, elem))
```
#### Exemplo:
Nossa missão é descobrir o total de todos os lançamentos:
O reduce vai chegar a um único número, vamos pegar uma série de elementos e **reduzir a uma coisa só**.


 
```js
const rockets = [
	{ country: "Russia", launches: 32},
	{ country: "US", launches: 23},
	{ country: "China", launches: 16},
	{ country: "Europa", launches: 7},
	{ country: "India", launches: 4},
	{ country: "Japan", launches: 3},
]

const totalLaunches = rockets.reduce((prevVal, elem) => prevVal + elem.launches, 0)

console.log(totalLaunches)
```
 
---
Fontes:
- https://youtu.be/dckGT8Rts-4?si=nKlp9nqG9NVsCiqc
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce

Tags: #softwaredevelopment 
