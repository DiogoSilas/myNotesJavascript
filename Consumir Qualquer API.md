Adicionar o [[Método fetch()]] vai fazer uma requisição para chamar o link que eu preciso. ([[Fetch]] & [[Fetch API]])
#### EXEMPLO:
```js
fetch("https://")
```
Após este comando, vai ser adicionado o "[[Then - Promise.prototype.then()]]" e nele criar uma [[Function - JavaScript]].
#### EXEMPLO:
```js
fetch("https://").then(function(resposta) {
	console.log(resposta)
	return resposta.json
})
```
Neste casso vai enviar todos os objetos.
Como fazer para escolher o objeto?
Após o ".then", crie outro com o nome da function "corpo":
```js
fetch("https://").then(function(resposta) {
	return resposta.json
}).then(function(corpo) {
	console.log(corpo)
})
```
**O que aconteceu?**
Quando mandei a requisição através do método ([[Then - Promise.prototype.then()]]), o servidor enviou a resposta. Para ver adicione o console.log ([[console.log() e Comentários no código JavaScript]]).
O primeiro .then está dizendo "pegue o que está dentro desta resposta e me retorne em .json ([[JSON - JavaScript Object Notation - Notação de Objetos JavaScript]])",
No segundo ".then": Agora eu quero que me retorne no console.log().

>Mas eu poderia retornar ela em uma tag do HTML ([[Tags HTML]]).
---
Fonte:
- https://youtu.be/IDG6EOXYAq8?si=V4VXZ65U9sOGQFqs
Tag: #softwaredevelopment 