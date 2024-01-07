A partir do ES6 temos 03 (três) formas de declarar variáveis. var, const e let
```js
	1. var nomeExplicativo = valor inicial desejado;
	2. const naoPodeMudarOValor = Valor unico;
	3. let nomeExplicativo = valor inicial desejado;
```

A *const* só pode receber um valor e não poderá ser alterado
O *let* pode receber um valor inicial e no decorrer do código é permitido reatribuir outro valor.
A *var* pode receber um valor inicial e no decorrer do código é permitido reatribuir outro valor. Mas é recomendado utiliza-la dentro de [[Function - JavaScript]].

## Escopos:
O escopo determina a acessibilidade (visibilidade) das variáveis.
Variáveis ​​JavaScript têm 3 tipos de escopo:
- Escopo do bloco
- Escopo da função
- Âmbito global
- Variáveis ​​declaradas dentro de um bloco { } não podem ser acessadas de fora do bloco:


---
Fontes: https://www.w3schools.com/js/js_scope.asp
Notas:
- Para utilizar a depuração no VS Code com arquivos JavaScript é necessário baixar o **Node.js**: https://nodejs.org/en/download
Tags: #softwaredevelopment 