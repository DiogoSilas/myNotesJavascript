
```js
const meuPedido = {
	item: [
	{nome: 'Poção de vida', valor: 100},
	{nome: 'Espada de prata', valor: 1000},
	{nome: 'Entrega', valor: 40, entrega: true}
	]
}

const calcularValorPedido = pedido => {
	const valorProdutos = pedido.itens
	.filter(item => !item.entraga)
	.reduce((totalPedidos, pedidoAtual) => totalPedidos + pedidoAtual.valor, 0);

	const entrega = pedido.item.filter(item => item.entrega);
if(valorProdutos > 500) {
	return valorProdutos;
} else {
	return valorProdutos + entrega[0].valor
}
}
console.log(calcularValorPedido(meuPedido))
```

O filter na constante **entrega** está retornando um array com uma posição "entrega", ao adicionar o "0", ele pegar o valor.

---
Fontes:
Links:
- [[Arrow Function]]
- [[Array - JavaScript]]
- [[Objetos - JavaScript]]
- [[Desestruturação de objetos e arrays]]
- [[Reduce - Array.prototype]]
- [[Return - Function]]
- [[console.log() e Comentários no código JavaScript]]
- [[Function - JavaScript]]

Tags: #softwaredevelopment 