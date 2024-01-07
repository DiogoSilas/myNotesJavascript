
-  == : igual
	1. O valor tem que ser o mesmo, independente se é do tipo string ou number
-  ===
	1. Idêntico, o valor e o tipo de dado têm que ser idêntico.
-  !=
	1. Comprovar se os valores são diferentes
- < menor; <= menor ou igual à; > maior que; >= maior ou igual à


---
and: *&&* ← resultado1 *AND* resultado2
- console.log(primeiro resultado *&&* segundo resultado)
    - true *&&* true = true
    - true *&&* false = false
    - false *&&* true = false
    - false *&&* false = false

or (**ou** uma coisa **ou** outra):**||**
- console.log(primeiro resultado **||** segundo resultado)
    - true **||** true = true
    - true **||** false = true
    - false **||** true = true
    - false **||** false = false

not: O que for verdadeiro vai ser falso e o que for falso vai ser verdadeiro.
- const x = 2
- const y = 2
- console.log(*!*(primeiro resultado === segundo resultado))
    - *X* e *Y* são idênticos, é verdadeiro (*true*), mas por causa do *not (!)* o resultado será trocado para *false*.

Estes operadores podem ser adicionados dentro dos colchetes de:
- [[console.log() e Comentários no código JavaScript]]
- [[Function - JavaScript]]

---
Fontes:
1. https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Expressions_and_Operators
2. https://www.todamateria.com.br/tabela-verdade/
3. https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript/Building_blocks/conditionals

Tags: #softwaredevelopment 