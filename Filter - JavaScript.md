- Usado para filtrar elementos de arrays. Facilitando a leitura e deixando o código mais limpo.
- O filter recebe uma função como parâmetro.
- Em casos de filtragem deixa de ser necessário a utilização do "for" no JavaScript.


Exemplo:
### Utilizando o for

```
let pessoas = [
	{ nome: 'Roberto', idade: 33},
	{ nome: 'Ricardo', idade: 33},
	{ nome: 'Raphael', idade: 27}
];
let pessoasComIdadeDe33Anos = [];

for(let i = 0; i < pessoas.length; i++) {
	if(pessoas[i].idade === 33) {
		pessoasComIdadeDe33Anos.push(pessoas[1])
	}
};
console.log(pessoasComIdadeDe33Anos);
### Utilizando o Filter
	let pessoas = [
		{ nome: 'Roberto', idade: 33},
		{ nome: 'Ricardo', idade: 33},
		{ nome: 'Raphael', idade: 27}
	];

	let pessoasComIdadeDe33Anos = pessoas.filter(function(pessoa){
		return pessoa.idade === 33;
	});
	console.log(pessoasComIdadeDe33Anos)
````

OU
```
let pessoasComIdadeDe33Anos = pessoas.filter(pessoa) => pessoa.idade === 33
console.log(pessoasComIdadeDe33Anos)
```
Fontes: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/filter
Tags: #softwaredevelopment