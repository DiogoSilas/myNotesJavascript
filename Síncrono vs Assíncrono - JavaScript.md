O código síncrono é executado em sequência, já o assíncrono é executado em paralelo. Isso significa que uma operação pode ocorrer enquanto outra ainda está sendo processada.

#### Síncrono:
O código síncrono é executado em sequência. Isso significa que cada operação deve aguardar a conclusão da anterior antes de ser executada.
```js
console.log('One');
console.log('Two');
console.log('Three');
// LOGS: 'One', 'Two', 'Three'
```
#### Assíncrona:
O código assíncrono é executado em paralelo. Isso significa que uma operação pode ocorrer enquanto outra ainda está sendo processada.
```js
console.log('One');

setTimeout(() => console.log('Two'), 100);

console.log('Three');
// LOGS: 'One', 'Three', 'Two'
```
Sobre o setTimeout: [[SetInterval e SetTimeout - JavaScript]].
A execução assíncrona de código costuma ser preferível em situações em que a execução pode ser bloqueada indefinidamente. Alguns exemplos disso são solicitações de rede, cálculos de longa execução, operações do sistema de arquivos, etc. O uso de código assíncrono no navegador garante que a página permaneça responsiva e que a experiência do usuário não seja afetada.


---
Fontes:
- https://www.30secondsofcode.org/js/s/sync-async/
Tags: #softwaredevelopment 