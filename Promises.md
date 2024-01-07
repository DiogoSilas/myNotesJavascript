Uma **Promise** é um objeto que representa a eventual conclusão ou falha de uma operação assíncrona [[Síncrono vs Assíncrono - JavaScript]].
Essencialmente, uma **promise** é um objeto retornado para o qual você adiciona callback, em vez de passar callbacks para uma função.

- Quando é uma promise precisa adicionar o [[Async e Await - Function]]

>Ele permite que você associe manipuladores ao valor de sucesso ou motivo de falha de uma ação assíncrona. Isso permite que métodos assíncronos retornem valores como métodos síncronos: em vez de retornar imediatamente o valor final, o método assíncrono retorna uma _promise_ para fornecer o valor em algum momento no futuro.
### Os estados do promises:
- Pendente: Foi criada mas não executada
- Realizada - **resolve**: sucesso na execução
- Recusada - **reject**: Falha na execução da **promises**
- Estabelecida: Quando ela foi **realizada** ou **recusada**
#### Uma Promise está em um destes estados:
- pending: estado inicial, nem cumprido nem rejeitado.
- fulfilled: significa que a operação foi concluída com sucesso.
- rejected: significa que a operação falhou.

![[Pasted image 20231218205549.png]]
#### Sintaxe:
```js
new Promise((resolve, reject)=>{

})
```

#### Exemplo:
```js
let chaleiraEstaNoFogo = true
let fogaoEstaLigado = true
let ferverAgua = () => {
	return new Promise((resolve, reject) => {
		if(chaleiraEstaNoFogo && fogaoEstaLigado) {
			console.log(`começando o processo de ferver água`)
			resolve()
		} else {
			console.log(`é necessário ligar o fogão e colocar a chaleira no fogão para ferver a água.`)
			reject()
		}
	});
}

ferverAgua(chaleiraEstaNoFogo, fogaoEstaLigado)
console.log(`Fazendo café`)
```


---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Using_promises
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Promise
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Promise/then
Tags: #softwaredevelopment 