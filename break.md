## Declaração break
Use break para terminar [[Laço de repetição]] ou um conjunto que utiliza **break label** **(nome da condição que deseja parar)**.
- Quando você utiliza **break** sem um label (nome da condição que deseja parar), ele encerrará imediatamente o laço mais interno **while, do-while, for, ou switch** e transferirá o controle para a próxima instrução.
- Quando você utiliza **break** com um **label (nome da condição que deseja parar)**, ele encerrará o label específico.
### Segue a sintaxe do break:
- break;
- break label;
#### Códigos de Exemplos:
##### break:
```js
for (i = 0; i < a.length; i++) {
  if (a[i] == theValue) {
    break;
  }
}
```
##### break label (nome da condição que deseja parar):
```js
var x = 0;
var z = 0;
labelCancelaLaco: while (true) {
  console.log("Laço exterior: " + x);
  x += 1;
  z = 1;
  while (true) {
    console.log("Laço interior: " + z);
    z += 1;
    if (z === 10 && x === 10) {
      break labelCancelaLaco;
    } else if (z === 10) {
      break;
    }
  }
}
```

---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Loops_and_iteration

Tags: #softwaredevelopment 