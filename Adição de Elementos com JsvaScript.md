Ao clicar no botão de verificação, as imagens são exibidas dinamicamente quando os campos "ano de nascimento" e "sexo" são preenchidos.

A tag de [[Imagens - HTML]] é criada através do JavaScript usando o elemento "[[createElement - Criando elementos (tags) com JavaScript]]" com a seguinte sintaxe:

```js
let elemento = document.createElement(nomeDaTag);
```

Após a criação desse elemento, adicionei uma classe com o nome "foto" utilizando o método "[[setAttribute(name, value) - Adicionado atributos em tags com JavaScript]]" . Exemplo:

```js
img.setAttribute('class', 'foto');
```

Para atribuir o caminho da imagem a essa tag, utilizei o mesmo atributo da variável "img" [[Declaração de variáveis]] , mas com o caminho específico para a foto desejada. Exemplo:

```js
img.setAttribute('src', '../src/images/imagemDesejada.jpg');
```

Dessa forma, criamos a seguinte estrutura:
```js
<img class="foto" src="../src/images/imagemDesejada.jpg">
```

Agora, como adicioná-la a no documento HTML? Selecione uma tag utilizando "getElementById" ou "querySelector" e, em seguida, adicione o método "[[appendChild(filho) - Criando Filhos em tags utilizando Js]]" . Exemplo:

```js
variavelComATagSelecionada.appendChild(img);
```

Lembrando que a criação da tag deve estar dentro da função do método "addEventListener".

---
Fontes:
- https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute
- https://developer.mozilla.org/pt-BR/docs/Web/API/Document/createElement
- https://developer.mozilla.org/pt-BR/docs/Web/API/Node/appendChild
Tags: #softwaredevelopment 