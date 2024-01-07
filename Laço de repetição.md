Laços oferecem um jeito fácil e rápido de executar uma ação repetidas vezes.
Você pode pensar em um laço de repetição como um jogo onde você manda o seu personagem andar X passos em uma direção e Y passos em outra; por exemplo, a ideia "vá 5 passos para leste" pode ser expressa em um laço desta forma:
##### Exemplo:
```js
var passo;
for (passo = 0; passo < 5; passo++) {
  // Executa 5 vezes, com os valores de passos de 0 a 4.
  console.log(`Andou ${passo} passos para o leste.`);
}
```

### For
Um laço **for** é repetido até que a condição especificada seja falsa. Uma declaração **for** é feita da seguinte maneira:
```js
for (expressaoInicial; condicao; incremento) {
    < bloco de declaracao >
}
```
#### Quando um for é executado, ocorre o seguinte:
1. A expressão **expressaoInicial** é inicializada e, caso possível, é executada. Normalmente essa expressão inicializa um ou mais contadores, mas a sintaxe permite expressões de qualquer grau de complexidade. Podendo conter também [[Declaração de variáveis]].
2. A expressão **condicao** é avaliada. **caso o resultado de "condicao" seja verdadeiro, o laço é executado.** Se o valor de **condicao** é falso, então o laço terminará. **Se a expressão "condicao" é omitida, a condicao é assumida como verdadeira.**
3. A instrução é executada. Para executar múltiplas declarações, use uma declaração em bloco ({ ... }) para agrupá-las:
4. 
```js
for (expressaoInicial; condicao; incremento) {
	{ < bloco de declaracao >}
	{ < bloco de declaracao >}
}
```

>A atualização da expressão incremento, se houver, executa, e retorna o controle para o passo 2.

### For ... in
A declaração **for...in** executa iterações a partir de uma variável específica ([[Declaração de variáveis]]), percorrendo todas as propriedades de um [[Objetos - JavaScript]]. Para cada propriedade distinta, o JavaScript executará uma iteração.
```js
function dump_props(obj, obj_name) {
  var result = "";
  for (var i in obj) {
    result += `${obj_name} . ${i} = ${obj[i]} <br>`;
  }
  result += "<hr>";
  return result;
}
```
##### Arrays
Embora seja tentador usar esta forma para interagir com os elementos de um Array, a declaração for...in irá retornar o nome pré-definido da propriedade ao invés do seu index numérico. Assim é melhor usar o tradicional for com index numérico quando interagir com arrays, pois o **for...in** interage com as propriedades definidas pelo programador ao invés dos elementos do array.

### For...of
A declaração **for...of** cria uma laço com objetos interativos (incluindo: [[Array - JavaScript]], [[Map - trabalhar com arrays]] , set, assim por conseguinte ), executando uma iteração para o valor de cada propriedade distinta.
```js
for (variavel of objeto) {
  bloco de declaracoes
}
```

#### Diferença entre for...in & for...of:
Enquanto o for...in interage com o nome das propriedades, o for...of interage com o valor das propriedades.
```js
let arr = [3, 5, 7];
arr.foo = "hello";

for (let i in arr) {
  console.log(i); // logs "0", "1", "2", "foo"
}

for (let i of arr) {
  console.log(i); // logs "3", "5", "7"
}
```
### Do...While
A instrução do...while repetirá até que a condição especificada seja falsa:
```js
do {
  < bloco de declaracao >
} while (condicao);
```

A instrução será executada uma vez antes da condição ser verificada. Para executar multiplas instruções utilize uma declaração de bloco ({ ... }) para agrupá-las.
>Caso a  "while (condicao)" seja verdadeira, então o laço será executado novamente. Ao final de cada execução, a "while (condicao)" é verificada.

Quando a condição contida no while for falsa a execução do laço é terminada e o controle é passado para a instrução seguinte a "do...while".
##### Exemplo:
```js
do {
  i += 1;
  console.log(i);
} while (i < 5);
```

### While
Uma declaração while executa suas instruções, desde que uma condição especificada seja avaliada como verdadeira. Segue uma declaração while:
```js
while (condicao) {
  bloco de declaracao
}
```
A "condicao" pode ser variáveis ([[Declaração de variáveis]]) ou  [[Function - JavaScript]].

---
Se a condição se tornar falsa, a declaração dentro do laço para a execução e o controle é passado para a instrução após o laço.

O teste da condição ocorre antes que o laço seja executado. Desta forma se a condição for verdadeira o laço executará e testará a condição novamente. Se a condição for falsa o laço termina e passa o controle para as instruções após o laço.

>Para executar múltiplas declarações, use uma declaração em bloco ({ ... }) para agrupar essas declarações.

---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Loops_and_iteration

Tags: #softwaredevelopment 