>Quando uma [[Function - JavaScript]] terminar de executar "them" (então) a gente vai fazer alguma coisa.

O método **then()** retorna uma [[Promises]]. Possui dois argumentos, ambos são "[[Função Callback]]", sendo uma para o sucesso e outra para o fracasso da promessa.

#### Sintaxe:
```js
p.then(quandoRealizada, quandoRejeitada);
p.then(function(valor) {
   // sucesso
  }, function(motivo) {
  // rejeitada
});
```

### Parâmetros:
#### quandoRealizada:
Uma [[Function - JavaScript]] chamada quando a [[Promises]] é cumprida (**Sucesso**).
>Essa função tem um argumento, o valor do cumprimento.

#### quandoRejeitada:
Uma [[Function - JavaScript]] chamada quando a Promise é **rejeitada**.
>Essa função tem um argumento, o motivo da recusa.

### Functions encadeadas:
Uma [[Function - JavaScript]] é dependente de outra para ser executada. Ao utilizar o método ".then",  facilita a manutenção e leitura do código. Sem a necessidade de criar uma estrutura de pirâmides como era entes do "**then**".

#### Exemplo:
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

---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Promise/then
Tags: #softwaredevelopment 