>Utilize a exportação nomeada

**export nomeado**, que permite exportar vários valores, funções ou objetos de um módulo.
```js
function nomeDaFunction() {
}

export { nomeDaFunction }
```
O import têm que estar sem as chaves:
```js
//No arquivo que deseja reutilizar o bloco de código
import { nomeDaFunction } from './caminha-do-arquivo-que-esta-a-function/arquivo.js'
```
### Sintaxe:
#### Há dois tipos de exportação:
Exportações Explícitas (Named Exports) (Zero ou mais exports por módulo)
Exportações Padrão (Default Exports) (Uma por módulo)

```js
// Exportando recursos individuais
export let name1, name2, …, nameN; // também var, const
export let name1 = …, name2 = …, …, nameN; // também var, const
export function functionName(){...}
export class ClassName {...}

// Lista de exportações
export { name1, name2, …, nameN };

// Renomeando exports
export { variable1 as name1, variable2 as name2, …, nameN };

// Exportando atribuições desestruturadas renomeando
export const { name1, name2: bar } = o;

// Exportações Padrão (Default exports)
export default expression;
export default function (…) { … } // também class, function*
export default function name1(…) { … } // também class, function*
export { name1 as default, … };

// Agregando módulos
export * from …; // não define a exportação padrão
export * as name1 from …; // Draft ECMAScript® 2O21
export { name1, name2, …, nameN } from …;
export { import1 as name1, import2 as name2, …, nameN } from …;
export { default } from …;
```

**export default**, que permite exportar um único valor, função ou objeto como o valor padrão de um módulo.

>Não utilizar pelo motivo de funcionar mesmo se trocar o nome da function, e isto gerará um problema na leitura do código e manutenção. Não dando consistência no código.

```js
export function nomeDaFunction() {
}
```
O import têm que estar sem as chaves:
```js
//No arquivo que deseja reutilizar o bloco de código
import nomeDaFunction from './caminha-do-arquivo-que-esta-a-function/arquivo.js'
```
---
Fontes: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/export
Tags: #softwaredevelopment 