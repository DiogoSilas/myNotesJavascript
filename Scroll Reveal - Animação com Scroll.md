### Sintaxe:
```js
window.scrollReveal = ScrollReveal({ reset: true });
scrollReveal.reveal('.nomeDaClass', {
	atributo: valor,
	atributo: valor,
	atributo: valor
});
//Ou com Objetos
scrollReveal.reveal('.nomeDaClass', objetoComOsValores)
//Ou
scrollReveal.reveal('.nomeDaClass', {atributo: valor, atributo: 'valor', atributo: valor});
```

#### Como utilizar:
1. Adicione o link para a API do Scroll Reveal dentro da tag head e um script reservado para as animações;
```html
<!DOCTYPE html>

<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Diogo Silas - Desenvolvedor Front-end</title>
  <!-- Styles: -->
  <link rel="stylesheet" href="./src/css/reveal.css">
  <!--Scripts:-->
  <script src="https://unpkg.com/scrollreveal"></script>
  <script src="./src/javascript/scrollReveal.js" defer></script>
</head>
```
2. Crie um arquivo CSS e adicione a propriedade **visibility: hidden;** através de classes ([[Class e Id]]) nos elementos que serão animado
#### Sintaxe:
```css
.class1,
.class2,
.class3{
    visibility: hidden;
}
```
3. No topo do script de JavaScript adicione o código a seguir:
```js
window.scrollReveal = ScrollReveal({ reset: true });
```
### Maneiras diferentes de adicionar animações:
Pode ser criado [[Objetos - JavaScript]] com propriedades de animação.
Sempre **adicionar virgulas** entre um atributo e outro.
#### Sintaxe:
```js
window.scrollReveal = ScrollReveal({ reset: true });
const textHome = {
    duration: 2500,
    distance: '30%',
    origin: 'left'
}
const imgHome = {
    duration: 2500,
    distance: '30%',
    origin: 'right'
}
const subTitulos = {
    duration: 2500,
    distance: '0px'
}
```

### Adicionando as animações:
As propriedade e seu valores estão todas disponíveis dento da biblioteca do **Scroll Reveal**.
#### Exemplos:
```js
window.scrollReveal = ScrollReveal({ reset: true });
const qualquerNome1 = {
    duration: 2500,
    distance: '30%',
    origin: 'left'
}
const qualquerNome2 = {
    duration: 2500,
    distance: '30%',
    origin: 'right'
}
const qualquerNome3 = {
    duration: 1000,
    distance: '0px'
}
scrollReveal.reveal('.class1', qualquerNome1);
scrollReveal.reveal('.class2', qualquerNome2);
scrollReveal.reveal('.class3', qualquerNome3);
```

---
Fontes:
- https://scrollrevealjs.org/
Tags: #softwaredevelopment 