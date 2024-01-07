A interface **Request** da [[Fetch API]] representa uma requisição de recursos.

Você pode criar um novo objeto **Request** usando o construtor **Request.Request()**, porém é mais provável que você encontre um objeto Request que seja retornado como resultado de outra operação de [[API - Application Programming Interface]].

>Request(): O construtor Request() cria um novo objeto Request.

#### Sintaxe:
```js
var myRequest = new Request(input, init);
```
#### Propriedades:
```js
Request.method: Contém o método da requisição (GET, POST etc.)

Request.url: Contém a URL da requisição.

Request.headers: Contém o objeto Headers associado à requisição.

Request.context: Contém o contexto da requisição (ex., audio, image, iframe etc.)

Request.referrer: Contém a referência da requisição (ex., client).

Request.referrerPolicy: Contém a política de referência da requisição (ex., no-referrer).

Request.mode: Contém o modo da requisição (ex., cors, no-cors, same-origin, navigate.)

Request.credentials: Contém a credencial da requisição
(Ex., omit, same-origin, include).

Request.redirect: Contém o modo de como os redirecionamentos serão tratados, Pode ser: follow, error ou manual.

Request.integrity: Contém o valor da subresource integrity da requisição (ex., sha256-BpfBw7ivV8q2jLiT13fxDYAe2tJllusRSZ273h2nFSE=).

Request.cache: Contém o modo de cache da requisição (ex., default, reload, no-cache).
```

##### Request implementa Body, então também possui as seguintes propriedades disponíveis:
```js
Body.body: Um simples "getter" para ler o conteúdo do corpo através da interface.

Body.bodyUsed: Armazena um Booleano que declara se o corpo da requisição já foi utilizado em uma resposta.
```

#### Métodos:
```js
Request implementa Body, então também possui os seguintes métodos disponíveis:

Request.clone(): Cria uma cópia atual do objeto Request.

Body.arrayBuffer(): Retorna um objeto do tipo promise que resolve um ArrayBuffer com a representação do corpo da requisição.

Body.blob(): Retorna um objeto do tipo promise que resolve um Blob com a representação do corpo da requisição.

Body.formData(): Retorna um objeto do tipo promise que resolve um FormData com a representação do corpo da requisição.

Body.json(): Retorna um objeto do tipo promise que resolve um JSON com a representação do corpo da requisição.

Body.text(): Retorna um objeto do tipo promise que resolve um USVString (en-US) (texto) com a representação do corpo da requisição.
```


---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/API/Request#propriedades
- https://developer.mozilla.org/pt-BR/docs/Web/API/Request/Request
Tags: #softwaredevelopment 