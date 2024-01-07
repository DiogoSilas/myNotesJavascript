A condicional switch avalia uma expressão, combinando o valor da expressão para um cláusula case, e executa as instruções associadas ao case.
#### Exemplo:
```js
const expr = 'Papayas';
switch (expr) {
  case 'Oranges':
    console.log('Oranges are $0.59 a pound.');
    break;
  case 'Mangoes':
  case 'Papayas':
    console.log('Mangoes and papayas are $2.79 a pound.');
    // Expected output: "Mangoes and papayas are $2.79 a pound."
    break;
  default:
    console.log(`Sorry, we are out of ${expr}.`);
}
```
### Sintaxe:
```js
switch(expressão) {
  case valor1:
    //Instruções executadas quando o resultado da expressão for igual á valor1
    break;
  case valor2:
    //Instruções executadas quando o resultado da expressão for igual á valor2
    break;
  ...
  case valueN:
    //Instruções executadas quando o resultado da expressão for igual á valorN
    break;
  default:
    //Instruções executadas quando o valor da expressão é diferente de todos os cases
    break;
}
```
#### Exemplo:
No exemplo a seguir, **expr** é avaliado como "**Bananas**", o programa corresponde o valor com o **case "Bananas"** e executa a instrução associada. Quando [[break]] for encontrado, o programa para ([[break]]), saindo de switch e executa a instrução localizada após o switch. **Se [[break]] fosse omitido, a instrução para "Cherries" também seria executada.**
```js
switch (expr) {
  case "Laranjas":
    console.log("As laranjas custam $0.59 o quilo.");
    break;
  case "Maçãs":
    console.log("Maçãs custam $0.32 o quilo.");
    break;
  case "Bananas":
    console.log("Bananas custam $0.48 o quilo.");
    break;
  case "Cerejas":
    console.log("Cerejas custam $3.00 o quilo.");
    break;
  case "Mangas":
  case "Mamões":
    console.log("Mangas e mamões custam $2.79 o quilo.");
    break;
  default:
    console.log(`Desculpe, estamos sem nenhuma ${expr}.`);
}

console.log("Tem algo mais que você gostaria de levar?");
```

## Multi-Caso - Com Switch
Esse método toma vantagem do fato de não existir um break após um case e irá continuara executar o próximo case independentemente se o case corresponde ao critério.
Esse é um exemplo de uma operação sequencial simples com a instrução switch, onde quatro valores diferentes fazem a mesma coisa:
```js
var Animal = "Girafa";
switch (Animal) {
  case "Vaca":
  case "Girafa":
  case "Cachorro":
  case "Porco":
    alert("Esse animal irá para Arca de Noé");
    break;
  case "Dinossauro":
  default:
    alert("Esse animal não vai.");
}
```

Esse é um exemplo de múltiplas operações sequenciais usando a instrução switch, onde, dependendo do número inteiro, você poderá receber outputs diferentes.

Isso mostra que você pode alterar a ordem que você insere as instruções de case, e isso não precisa ser uma sequência numérica.

Em JavaScript, você pode até mesmo misturar definições de strings dentro desses cases ([[O que é algoritmo]]).

```js
var foo = 1;
var output = "Output: ";
switch (foo) {
  case 10:
    output += "Então ";
  case 1:
    output += "Qual ";
    output += "É ";
  case 2:
    output += "O Seu ";
  case 3:
    output += "Nome";
  case 4:
    output += "?";
    alert(output);
    break;
  case 5:
    output += "!";
    alert(output);
    break;
  default:
    alert("Favor escolher um número de 0 à 6!");
}
```

|Value|Alert Text|
|---|---|
|foo é NaN ou não é 1, 2, 3, 4, 5 ou 10|Favor escolher um número de 0 à 6!|
|10|Output: Então Qual É O Seu Nome?|
|1|Output: Qual É O Seu Nome?|
|2|Output: Seu Nome?|
|3|Output: Nome?|
|4|Output: ?|
|5|Output: !|

---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/switch

Tags: #softwaredevelopment 