A desestruturação nos permite extrair variáveis de objetos e arrays.

### Desestruturação de um Objeto: **{}**
Primeiro: Criamos um tipo de variável, [[Declaração de variáveis]].
Segundo: Abrimos e fechamos chaves **{}** e dentro declaramos as variáveis.
Terceiro: atribuímos a variável ao objeto. Neste exemplo, "pessoa".

```
let pessoa = { nome: 'Roberto', sobrenome: 'Dias', idade: 33}

let {nome: nome, idade: idade, sobrenome: sobrenome} = pessoa

console.log(nome)
console.log(idade)
console.log(sobrenome)
```

### Desestruturação de um Array: **[]**
Para desestruturar um array é preciso utilizar colchetes **[]** para as variáveis.
A localização dos conteúdos dentro da desestruturação do **array** é com base em sua posição.

Se eu adicionar um **console.log(quatro)** com o valor "quatro", o resultado será indefinido. ([[console.log() e Comentários no código JavaScript]])
```
const numero = [1, 2, 3];

const [um, dois, tres] = numero

console.log(um)
console.log(dois)
console.log(tres)
console.log(quatro)
```
---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment
Tags: #softwaredevelopment 