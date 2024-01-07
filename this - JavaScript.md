Em muitos casos, o valor `this` é determinado pela forma como a função é chamada.

#### Contexto global:
No contexto de execução global (fora de qualquer função), this refere-se ao objeto global, seja em modo estrito ou não.
```js
console.log(this.document === document); // true

// Em navegadores web, o objeto window é também o objeto global:
console.log(this === window); // true

this.a = 37;
console.log(window.a); // 37
```

#### Contexto de função:
Dentro de uma função, o valor de this depende de como a função é chamada.

Como o código a seguir não está no [[Strict mode]] , o valor de **this** não é definido pela chamada. Por padrão, this será o objeto global que no navegador, que é o window.
```js
function f1() {
  return this;
}

// No navegador
f1() === window; // true
console.log(f1())
```

Em [[Strict mode]] , o valor de **this** permanece seja qual for o definido ao entrar no contexto de execução, assim, no caso a seguir, this por padrão será indefinido (undefined):
```js
function f2() {
  "use strict"; // assume Strict mode
  return this;
}

f2() === undefined; // true
```
>Portanto, em modo estrito, se this não for definido durante o contexto da execução, ele permanecerá indefinido (undefined).

#### Contexto [[Arrow Function]]:
O **this** é definido como conjunto de palavras, isto é, seu valor é definido pelo contexto de execução onde está inserido.
>Em um código global, this assume o objeto global:
```js
var globalObject = this;
var foo = () => this;
console.log(foo() === globalObject); // true
```
**Não importa como foo é chamado, o this continuará como o objeto global**. Isto continua verdadeiro mesmo se chamá-lo como método de um determinado objeto (o que normalmente definiria seu this ao objeto), com call ou apply ou bind é usado:
```js
var globalObject = this;
var foo = () => this;
console.log(foo() === globalObject); // true
//---------------------------------------------------
// Chama como um método de um objeto
var obj = { foo: foo };
console.log(obj.foo() === globalObject); // true

// Tentativa de definir this usando call
console.log(foo.call(obj) === globalObject); // true

// Tentantiva de definir this usando bind
foo = foo.bind(obj);
console.log(foo() === globalObject); // true
```

---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/this

Tags: #softwaredevelopment 