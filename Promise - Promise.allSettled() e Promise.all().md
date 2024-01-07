O que é uma promise? [[Promises]]

### Promise.allSettled()
O **Promise.allSettled()** método estático recebe um iterável de promessas como entrada e retorna um único [[Promises]]. **Essa promessa retornada é cumprida quando todas as promessas da entrada são satisfeitas** (inclusive quando um iterável vazio é passado), com uma matriz de objetos que descreve o resultado de cada promessa.
### Promise.all()
O Promise.all() método estático recebe um iterável de promessas como entrada e retorna um único [[Promises]]. **Esta promessa retornada é cumprida quando todas as promessas da entrada são cumpridas** (inclusive quando um iterável vazio é passado), com uma matriz de valores de cumprimento. Ele rejeita quando qualquer uma das promessas da entrada é rejeitada, com este primeiro motivo de rejeição.


---
Fontes:
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/allSettled
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/all
Tags: #softwaredevelopment 