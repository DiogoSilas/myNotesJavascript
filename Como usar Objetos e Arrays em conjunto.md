
>Como usar [[Objetos - JavaScript]] e [[Array - JavaScript]] em conjunto?

Cria um [[Objetos - JavaScript]], crie uma **chave** e dentro dela passe como parâmetro um [[Array - JavaScript]].
#### Exemplo:
```js
let videoGame = {
	nome: 'Xbox',
	valor: 3000,
	jogos: [
		{nome:'Final Fantasy'}, 
		{nome:'Fallout'},
		{nome: 'FiFA'}
	]
}console.log(videoGame)

//----
let jogo1 = {
	nome:'Final Fantasy'
}

let jogo2 = {
	nome:'Fallout'
}

let videoGame = {
	nome: 'Xbox',
	valor: 3000,
	jogos: [jogo1, jogo2]
}

let jogo3 = {
	nome: 'Fifa'
}

videoGame.jogos.push(jogo3)
console.log(videoGame)
```