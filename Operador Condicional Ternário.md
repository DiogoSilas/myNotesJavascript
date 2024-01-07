O operador condicional (ternário) é o único operador JavaScript que possui três operandos. Este operador é frequentemente usado como um atalho para a instrução [[Condicionais - if...else & else...if]].

### Sintaxe:
```js
condition ? expr1 : expr2
```
#### Parâmetros:
**condition**
- Uma expressão que é avaliada como **true** ou **false**.
**expr1, expr2**
- Expressões com valores de qualquer tipo.
Se condition é true, o operador retornará o valor de expr1; se não, ele retorna o valor de exp2.
### Mais de uma operação
> Também são possíveis múltiplas avaliações ternárias.

```js
var firstCheck = false,
  secondCheck = false,
  access = firstCheck
    ? "Access denied"
    : secondCheck
      ? "Access denied"
      : "Access granted";

console.log(access); // logs "Access granted"
```

Posso usar avaliações ternárias no espaço livre de modo a fazer diferentes operações ou pode fazer mais do que uma única operação em cada caso, separando-os por vírgula:
```js
var age = 16;

var url =
  age > 18
    ? (alert("OK, you can go."),
      // alert returns "undefined", but it will be ignored because
      // isn't the last comma-separated value of the parenthesis
      "continue.html") // the value to be assigned if age > 18
    : (alert("You are much too young!"),
      alert("Sorry :-("),
      // etc. etc.
      "stop.html"); // the value to be assigned if !(age > 18)

location.assign(url); // "stop.html"
```

---
Fontes:
1. https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Conditional_operator

Tags: #softwaredevelopment 