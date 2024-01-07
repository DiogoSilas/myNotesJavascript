>Ao criar uma [[Function - JavaScript]] e não retorno esse valor, pode gerar um erro no código.
#### Return:
Quando o JavaScript atinge uma instrução **return** , a função para de ser executada.

Se a função foi invocada a partir de uma instrução, o JavaScript “retornará” para executar o código após a instrução invocada. As funções geralmente calculam um **return value**. O valor de retorno é "devolvido" ao "chamador":

```js
// A função é chamada, o valor de retorno terminará em x
let x = myFunction(4, 3);  
  
function myFunction(a, b) {  
//Função retorna o produto de a e b 
  return a * b;  
}
```
---
Fontes: https://www.w3schools.com/js/js_functions.asp
Tags: #softwaredevelopment 