Hoisting é o comportamento padrão do JavaScript de mover [[Declaração de variáveis]]  e [[Function - JavaScript]] para o topo.

>Uma das vantagens do JavaScript em colocar declarações de função na memória antes de executar qualquer segmento de código é que ele permite que você use uma função antes de declara-la em seu código.

Em JavaScript, uma variável pode ser declarada após ter sido usada. Em outras palavras; uma variável pode ser usada antes de ser declarada.
### Fornece o mesmo resultado:
#### Exemplo 1
```js
x = 5; // atribuir 5 para x  
  
elem = document.getElementById("demo"); // Encontre um elemento 
elem.innerHTML = x; // Exibir x no elemento
  
var x; // Declare x
```
#### Exemplo 2
```js
var x; // Declare x
x = 5; // atribuir 5 para x

elem = document.getElementById("demo");// Encontre um elemento
elem.innerHTML = x;// Exibir x no elemento
```

>**Hoisting** é o comportamento padrão do JavaScript de mover todas as [[Declaração de variáveis]] para o topo do escopo atual (para o topo do script atual ou da [[Function - JavaScript]] atual).

## As palavras-chave "let" e "const"
Variáveis ​​definidas com let e const são içadas para o topo do bloco, mas não inicializadas. O bloco de código conhece a variável, mas não pode ser usado até que seja declarado. **Usar uma let variável antes de ser declarada resultará em um arquivo ReferenceError.**

A variável está em uma "zona morta temporal" desde o início do bloco até ser declarada.
**Isso resultará em ReferenceError**:
```js
carName = "Volvo";  
let carName;
```
Usar uma **const** variável antes de ser declarada é um erro de sintaxe, portanto o código simplesmente não será executado.
```js
carName = "Volvo";  
const carName;
```

---
Fontes:
- https://www.w3schools.com/js/js_hoisting.asp
- https://developer.mozilla.org/pt-BR/docs/Glossary/Hoisting

Tags: #softwaredevelopment 