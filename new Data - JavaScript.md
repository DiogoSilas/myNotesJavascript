**Acesso a datas**:
```js
const dataAtual = new Date()
console.log(dataAtual)
```
#### Dia, Mês e Ano:
```js
const dataAtual = new Date()
const dia = dataAtual.getDate();//Dia
const mes = dataAtual.getMonth() +1;//Mês
const ano = dataAtual.getFullYear();//Ano

console.log(dia);
console.log(mes);
console.log(ano);
```
O "+1" na const mes é para retornar o mês em numero.

#### Subtrair ou Adicionar Dias:
```js
const dataAtual = new Date()
dataAtual.setDate(dataAtual.getDate() +7);

console.log(dataAtual)
```
Está pegando o dia e adicionando mais sete.

#### Formatando data para o formato brasileiro dia/mes/ano:
```js
const dataAtual = new Date();
const dataFormatada = dataAtual.toLocaleDateString('pt-BR');

console.log(dataFormatada)
```

---
Fontes:
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/DateTimeFormat
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString
Links:
- [[console.log() e Comentários no código JavaScript]]
- [[Operadores Matemáticos]]
- [[Declaração de variáveis]]
Tags: #softwaredevelopment 