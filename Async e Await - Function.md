>Trabalhar com [[Promises]], não vamos precisar usar o [[Then - Promise.prototype.then()]].

#### Async:
Esta palavra tem que ser adicionada antes do nome da [[Function - JavaScript]] para a transformar em assíncrona ([[Síncrono vs Assíncrono - JavaScript]]). Podendo dar início ao uso do método **await**.
> Tem que ser sempre na função em que estou trabalhando. A palavra "async" não pode estar na função pai ([[Conceito de pai e filhos]]).
##### Exemplo do Erro:
```js
let ferverAgua = () => {
	return new Promise((resolve, reject) => {
		if(chaleiraEstaNoFogao && fogaoEstaLigado) {
			console.log('Passo 1: Colocar a água para ferver')
			resolve()
		} else {
		console.log('Erro 1')
		reject()
		}
	})
}
let passarOCafe = () => {
	return new Promise((resolve, reject) => {
		if(chaleiraEstaNoFogao && fogaoEstaLigado) {
			console.log('Passo 2: Água foi fervida')
			resolve()
		} else {
		console.log('Erro 2')
		reject()
		}
	})
}
let tomarCafe = () => {
	return new Promise((resolve, reject) => {
		if(chaleiraEstaNoFogao && fogaoEstaLigado) {
			console.log('Passo 3: Tomei o meu café')
			resolve()
		} else {
		console.log('Erro 3')
		reject()
		}
	})

let lavarXicara = () => {
	return new Promise((resolve, reject) => {
			if(chaleiraEstaNoFogao && fogaoEstaLigado) {
				console.log('Passo 4: Lavar a xícara')
				resolve()
			} else {
			console.log('Erro 4')
			reject()
			}
		})
	}
}

let chaleiraEstaNoFogao = true
let fogaoEstaLigado = true
	// Errado
		async function paiComAsyncErrado(){
			function filhoQueDeveTerOAsync() {}
		};
	// Correto
		function paiSemAsyncErrado(){
			async function filhoQueDeveTerOAsync() {}
		};
```
#### Sintaxe:
```js
let ferverAgua = () => {
	return new Promise((resolve, reject) => {
		if(chaleiraEstaNoFogao && fogaoEstaLigado) {
			console.log('Passo 1: Colocar a água para ferver')
			resolve()
		} else {
		console.log('Erro 1')
		reject()
		}
	})
}
let passarOCafe = () => {
	return new Promise((resolve, reject) => {
		if(chaleiraEstaNoFogao && fogaoEstaLigado) {
			console.log('Passo 2: Água foi fervida')
			resolve()
		} else {
		console.log('Erro 2')
		reject()
		}
	})
}
let tomarCafe = () => {
	return new Promise((resolve, reject) => {
		if(chaleiraEstaNoFogao && fogaoEstaLigado) {
			console.log('Passo 3: Tomei o meu café')
			resolve()
		} else {
		console.log('Erro 3')
		reject()
		}
	})

let lavarXicara = () => {
	return new Promise((resolve, reject) => {
			if(chaleiraEstaNoFogao && fogaoEstaLigado) {
				console.log('Passo 4: Lavar a xícara')
				resolve()
			} else {
			console.log('Erro 4')
			reject()
			}
		})
	}
}
let chaleiraEstaNoFogao = true
let fogaoEstaLigado = true

async function iniciarProcessoDeFazerCafe(){
	const aguaFervida = await ferverAgua(chaleiraEstaNoFogao && fogaoEstaLigado)
	const cafePassado =  await passarOCafe(aguaFervida)
	const cafeTomado = await tomarCafe(cafePassado)
	const xicaraLavada = await lavarXicara(cafeTomado)
	if(xicaraLavada) console.log('Finalizado o ritual de tromar o café, bora trabalhar')
};
iniciarProcessoDeFazerCafe()
```

### Await:
> Só vou conseguir passar a palavra chave "await" se a function tiver a palavra chave "async".

Quando uma **função assíncrona** em JavaScript é invocada, ela resulta em uma [[Promises]]. Quando a **função assíncrona** produz um valor, a [[Promises]] é resolvida com esse valor. Caso a **função assíncrona** gere uma exceção ou algum valor, a [[Promises]] é rejeitada, incorporando o valor lançado.

É importante notar que uma **função assíncrona** ([[Síncrono vs Assíncrono - JavaScript]]) pode incorporar uma expressão **await**. Esta expressão pausa a execução da **função assíncrona**, aguarda a resolução da **Promise** fornecida e, posteriormente, retoma a execução da **função assíncrona**, retornando o valor resolvido.

### Comparação dos códigos "[[Then - Promise.prototype.then()]]" com "async - await":
#### Then:
```js
ferverAgua(chaleiraEstaNoFogao, fogaoEstaLigado)
	.then( () => {
		return passarOCafe()
	})
	.then( () => {
		return tomarCafe()
	})
	.then( () => {
		return lavarXicara()
	})
	.then( () => {
		console.log('Finalizei meu ritual do café, bora trabalhar')
	});
```
#### Async Await:
```js
async function iniciarProcessoDeFazerCafe(){
	const aguaFervida = await ferverAgua(chaleiraEstaNoFogao && fogaoEstaLigado)
	const cafePassado =  await passarOCafe(aguaFervida)
	const cafeTomado = await tomarCafe(cafePassado)
	const xicaraLavada = await lavarXicara(cafeTomado)
	if(xicaraLavada) console.log('Finalizado o ritual de tromar o café, bora trabalhar')
};
```
---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/async_function
Tags: #softwaredevelopment 