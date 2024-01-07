
[[Function - JavaScript]] de seta foram introduzidas no ES6, nos permitindo escrever uma sintaxe de função mais curta:
```js
let myFunction = (a, b) => a * b;
```

#### Antes das funções de flexa:
```js
hello = function() {  
  return "Hello World!";  
}
```

#### Com as funções de flexa:
```js
hello = () => {  
  return "Hello World!";  
}
```
Se a [[Function - JavaScript]] tiver apenas uma instrução e a instrução retornar 1 (um) valor, você poderá remover os colchetes e a palavra-chave [[Return - Function]]:
```js
// Valor 'return' por padrão
hello = () => "Hello World!";
```

Se tiver parâmetros, passe-os entre parênteses. **Se tiver apenas um parâmetro, também poderá pular os parênteses:**
```js
// Função de seta sem parênteses:
hello = val => "Hello " + parametro;
```

---
Fontes: https://www.w3schools.com/js/js_arrow_function.asp
Tags: #softwaredevelopment 