Retorna uma lista de elementos presentes no documento (usando ordenação em profundidade, pré-ordenada e transversal dos nós do documento) que coincidam com o grupo de seletores especificado.
### Sintaxe:
```js
elementList = document.querySelectorAll(selectors);
```
- **Selectors** é uma string contendo um ou mais seletores CSS separados por vírgulas.
- Será retornado todos os elementos do documento que coincidam com os seletores especificados [[Class e Id]] . Se a string selectors conter um CSS PseudoElements, o retorno será uma NodeList vazia.

---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/API/Document/querySelectorAll

Tags: #softwaredevelopment 