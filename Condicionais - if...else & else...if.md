Em qualquer linguagem de programação, o código precisa tomar decisões e realizar ações de acordo, dependendo de diferentes entradas.

## if...else
>O tipo mais comum de declaração condicional que você usará em JavaScript

### Sintaxe básica:
```js
if (condicao) {
  codigo para executar caso a condição seja verdadeira
} else {
  senão, executar este código
}
```

A palavra reservada if seguida de um par de parênteses:
- Um teste condicional, localizado dentro dos parênteses (normalmente "este valor é maior que esse", ou "este valor existe"). Esta condição pode fazer uso dos operadores de comparação que discutimos no último módulo, e podem retornar true ou false.
- Um par de chaves, e dentro dele temos código — pode ser qualquer código que queiramos, e só vai ser executado se o teste condicional retornar true.

A palavra reservada **else**:
- Outro par de chaves, dentro dele temos mais um pouco de código — pode ser qualquer código que queiramos, e **só vai executar se o teste condicional retornar um valor diferente de true,** neste caso not true, ou false.
## Else...if
Maneira de encadear escolhas/resultados extras ao seu if...else.
```js
var select = document.querySelector("select");
var para = document.querySelector("p");

select.addEventListener("change", setWeather);

function setWeather() {
  var choice = select.value;

  if (choice === "sunny") {
    para.textContent =
      "It is nice and sunny outside today. Wear shorts! Go to the beach, or the park, and get an ice cream.";
  } else if (choice === "rainy") {
    para.textContent =
      "Rain is falling outside; take a rain coat and a brolly, and don't stay out for too long.";
  } else if (choice === "snowing") {
    para.textContent =
      "The snow is coming down — it is freezing! Best to stay in with a cup of hot chocolate, or go build a snowman.";
  } else if (choice === "overcast") {
    para.textContent =
      "It isn't raining, but the sky is grey and gloomy; it could turn any minute, so take a rain coat just in case.";
  } else {
    para.textContent = "";
  }
}
```

```html
<label for="weather">Select the weather type today: </label>
<select id="weather">
  <option value="">--Make a choice--</option>
  <option value="sunny">Sunny</option>
  <option value="rainy">Rainy</option>
  <option value="snowing">Snowing</option>
  <option value="overcast">Overcast</option>
</select>

<p></p>
```
Links:
- [[Operadores Lógicos - JavaScript]]
- [[Operadores Matemáticos]]


---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript/Building_blocks/conditionals

Tags: #softwaredevelopment 