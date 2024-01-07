Variáveis no JavaScript ([[Declaração de variáveis]]) são contêineres para valores de dados. Objetos também são variáveis. Mas os objetos podem conter muitos valores.

#### Object Definition:
```js
let tenis = {
	//chave: valor
	cor: 'branco',
	tamanho:'42',
	emEstoque: true
}
// ao abrir e fechar chaver torna
// em um objeto.

tenis.valor = 200
//aciciona uma propriedade após ser criado.

console.log(tenis)
// mostrará todos valores

console.log(tenis.tamanho)
//mostratá o valor da chave "tamanho"
```

```js
const person = {  
  firstName: "John",  
  lastName: "Doe",  
  age: 50,  
  eyeColor: "blue"  
};
```

#### Object Properties:
Os pares name:values em objetos JavaScript são chamados de propriedades

#### Acessando Propriedades do Objeto:
Posso acessar objetos de duas maneira:
```js
objectName.propertyName
// Ou
objectName["propertyName"]
```

**Exemplo:**
```js
const person = {  
  firstName: "John",  
  lastName: "Doe",  
  age: 50,  
  eyeColor: "blue"  
};

person.lastName;
//Ou
person["lastName"];
```

---
Fontes:
Tags: #softwaredevelopment 