Uso comum do **spread** é concatenar dois [[Array - JavaScript]].

#### O que é o spread?
Sintaxe de Espalhamento (Spread syntax) permite que um objeto iterável, como uma expressão de [[Array - JavaScript]] ou uma string seja expandido para ser usado onde zero ou mais argumentos (para chamadas de **function**) ou elementos são esperados, ou que um objeto seja expandido onde zero ou mais pares _propriedade: valor_  são esperados.

Para utilizar o **spread** adiciono **três pontos** antes do nome da variável dento do array: 
```js
let pessoas1 = ['Diogo', 'Pedro', 'Ricardo']
let pessoas1 = ['Marcos', 'Lucas', 'Igor']

let pessoas1 = [...pessoas1, ...pessoas2]
console.log(pessoas1)
```

Agora a variável **pessoas1** tem seis valores no [[Array - JavaScript]].

#### Com o concat:
O **spread** tem a mesma função que o **concat**. Mas é recomendado usar o spread devido sua praticidade ao adicionar novos arrays.
```js
let pessoas1 = ['Diogo', 'Pedro', 'Ricardo']
let pessoas1 = ['Marcos', 'Lucas', 'Igor']

let pessoas1 = pessoas1.concat(pessoas2)
console.log(pessoas1)
```

### Clonar  [[Objetos - JavaScript]]:
```js
const pessoa1 = { nome: 'Roberto', idade: 33}

const objetoClonado = {...pessoa1}
console.log(objetoClonado)
console.log(pessoa1)
```

Ao clonar o **objeto** podemos mexer nele livremente sem afetar o original.

---
Fontes: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Spread_syntax
Tags: #softwaredevelopment 