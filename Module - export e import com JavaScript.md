São arquivos que vamos exportar e depois importar em pontos específicos para reutilizar.
#### Sintaxe:
Na tag com o script precisa falar que o tipo é _module_:
```html
<script type="module" src=""></script>
```
##### Sintaxe no arquivo .js para exportar apenas uma function
```js
//Em um arquivo adicionar a palavra "export"
export function nomeDaFunction() {
}
```

```js
//No arquivo que deseja reutilizar o bloco de código
import { nomeDaFunction } from './caminha-do-arquivo-que-esta-a-function/arquivo.js'
```
- from : de onde

#### Exportar várias function:
no final do script js adicionar a palavra export abrir chave e colocar o nome das funções
```js
//bloco de códigos
// No final do código:
export { nomeDaFunction1, nomeDaFunction2, nomeDaFunction2 } 
```

```js
inport { nomeDaFunction1, nomeDaFunction2, nomeDaFunction2 } from './caminha-do-arquivo-que-esta-a-function/arquivo.js'

console.log(nomeDaFunction1)
console.log(nomeDaFunction2)
console.log(nomeDaFunction3)
```
---
Fontes: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Modules
Links: [[Export default e Export nomeado]]
Tags: #softwaredevelopment 