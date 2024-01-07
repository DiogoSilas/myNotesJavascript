Ao chamar o *map* em um array nós transformamos ele em outro totalmente novo, podendo ter todos os valores mudados.

Parecido com o [[Filter - JavaScript]], mas no *filter* é utilizado para filtrar elementos do array original, possuindo sempre um numero menor de elementos. No *map* podemos criar um array nova mas com o mesmo número de elementos.

	let pessoas = [
		{ nome: 'Roberto', idade: 33},
		{ nome: 'Ricardo', idade: 33},
		{ nome: 'Raphael', idade: 27}
	]
	let nomeDasPessoas = pessoas.map(function(pessoa){
		return pessoa.nome + "têm" + pessoa.idade + " anos de idade"
	})
	console.log(nomeDasPessoas)
	// Simplificando função:
	let nomeDasPessoas = pessoas.map(pessoa => pessoa.nome + "têm" + pessoa.idade + " anos de idade")
	console.log(nomeDasPessoas)

Como o *map* retorna uma nova versão do array, podemos usar esse callback em uma função totalmente nova.

Provavelmente vou usar mais o método *map* do que os métodos [[For e For in - JavaScript]].

---
Fontes: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map
Tags: #softwaredevelopment 