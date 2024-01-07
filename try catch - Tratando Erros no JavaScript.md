>Com o try{}catch() o código não para de ser executado quando ocorre um erro dentro dele. 

As declarações **try...catch** marcam um bloco de declarações para testar (**try**), e especifica uma resposta, caso uma exceção seja lançada.

A declaração **try** consiste em um bloco try, que contém uma ou mais declarações, e ao menos uma **cláusula catch** ou uma cláusula finally, ou ambas. Ou seja, há 3 formas de declarações **try** :

- try{}catch()
- try{}finally{}
- try{}catch()finally{}

#### Cláusula catch:
Uma cláusula catch contém declarações que especificam o que fazer caso uma exceção seja lançada no bloco try. Ou seja, se você quer que o bloco try tenha êxito, e caso não tenha, você quer que o controle passe para o bloco catch. Caso qualquer declaração dentro do bloco try (ou em uma função chamada no interior do bloco try) lançar uma exceção o controle imediatamente muda para a cláusula catch. Se nenhuma exceção for lançada no bloco try a cláusula catch é ignorada.
##### Sintaxe:
```js
async function iniciarProcessoDeFazerCafe(){
	try{
		const aguaFervida = await ferverAgua(chaleiraEstaNoFogao && fogaoEstaLigado)
		const cafePassado =  await passarOCafe(aguaFervida)
		const cafeTomado = await tomarCafe(cafePassado)
		const xicaraLavada = await lavarXicara(cafeTomado)
	}catch(err){
		console.log(err)
	}
};
```
#### Cláusula finally:
A cláusula finally é executada após a execução do bloco try e da(s) cláusula(s) catch porém antes das declarações seguintes ao try. Ela sempre é executada, independente se uma exceção for lançada ou capturada.
> Indicado para fechar conexão de banco de dados ou arquivos abertos para leitura.
##### Sintaxe:
```js
async function iniciarProcessoDeFazerCafe(){
	try{
		const aguaFervida = await ferverAgua(chaleiraEstaNoFogao && fogaoEstaLigado)
		const cafePassado =  await passarOCafe(aguaFervida)
		const cafeTomado = await tomarCafe(cafePassado)
		const xicaraLavada = await lavarXicara(cafeTomado)
	}catch(err){
		console.log(err)
	}finally{
		console.log('Finalizado o ritual de tromar o café, bora trabalhar')
	}
};
```
#### Cláusula throw:
```js
async function iniciarProcessoDeFazerCafe(){
	try{
		const aguaFervida = await ferverAgua(chaleiraEstaNoFogao && fogaoEstaLigado)
		const cafePassado =  await passarOCafe(aguaFervida)
		const cafeTomado = await tomarCafe(cafePassado)

	   throw "Mensagem de erro"
	}catch(err){
		console.log(err)
	}finally{
		console.log('Finalizado o ritual de tromar o café, bora trabalhar')
	}
};
```
---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Error
- https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/try...catch
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/throw
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling
Links:
- [[Consumir Qualquer API]]
- [[Function - JavaScript]]
- [[Async e Await - Function]]
- [[Função Callback]]
Tags: #softwaredevelopment 