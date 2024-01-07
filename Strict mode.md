### ALERTA:
>Essa sintaxe tem uma armadilha: não é possível concatenar cegamente scripts não conflitantes.
>
>Considere concatenar um script strict mode com um script não-strict mode: a concatenação inteira parece strict! O inverso também é verdade: não-strict mais strict parece não-strict.
>
>Concatenar scripts strict mode com outros é bom, e concatenar scripts não-strict mode é bom. Simplesmente concatenar scripts strict e não-strict é problemático.
>
>Portanto é recomendado que você ative strict mode função-por-função (pelo menos durante o período de transição).

O strict mode faz várias mudanças nas semânticas normais do JavaScript.
1. Primeiro, o strict mode elimina alguns erros silenciosos do JavaScript fazendo-os lançar exceções.
2. Segundo, o strict mode evita equívocos que dificultam que motores JavaScript realizem otimizações: código strict mode pode às vezes ser feito para executar mais rápido que código idêntico não-strict mode.
3. Terceiro, strict mode proíbe algumas sintaxes que provavelmente serão definidas em versões futuras do ECMAScript.
>Strict mode se aplica a scripts inteiros ou funções individuais. Ele não se aplica a declarações de bloco fechadas em chaves {};

#### Invocando Strict Mode:
Para invocar strict mode para um script inteiro, coloque exatamente a declaração **"use strict";** ou **'use strict';** antes de qualquer outra declaração.
```js
// Sintaxe strict mode para todo o script
"use strict";
let scriptMode = "Oi! Eu sou um script strict mode!";
console.log(scriptMode)
```

#### Strict mode para funções:
Da mesma forma, invocar strict mode para [[Function - JavaScript]], coloque exatamente a declaração **"use strict";** ou **'use strict';** antes de qualquer outra declaração.
```js
function strict() {
  // Sintaxe strict mode a nível de função
  "use strict";
  function nested() {
    return "E eu também!";
  }
  return "Oi! Eu sou uma função strict mode!  " + nested();
} console.log(strict(), nested())

function notStrict() {
  return "Eu não sou strict.";
}console.log(notStrict())
```


---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Strict_mode

Tags: #softwaredevelopment 