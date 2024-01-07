A interface **Response** da [[Fetch API]] representa a resposta para uma requisição.

Você pode criar um novo objeto Response usando o construtor **Response.Response()**, porém é mais provável você encontrar um objeto Response sendo retornado como o resultado de uma outra operação da [[API - Application Programming Interface]].

### Response() - Cria um novo objeto Response:
#### Sintaxe:
```js
new Response()
new Response(body)
new Response(body, options)
```
#### Parâmetros:

##### body:
>Um objeto que define um corpo para a resposta. Pode ser null(que é o valor padrão) ou um dos seguintes:


```js
Blob
ArrayBuffer
TypedArray
DataView
FormData
ReadableStream
URLSearchParams
String
string literal
```

##### options:
>Um objeto de opções contendo quaisquer configurações personalizadas que você deseja aplicar à resposta ou um objeto vazio (que é o valor padrão). As opções possíveis são:
- **status**: O código de status da resposta. O valor padrão é 200;
- **statusText**: A mensagem de status associada ao código de status, como "OK", O valor padrão é "";
- **headers**: Quaisquer cabeçalhos que você deseja adicionar à sua resposta, contidos em um Headersobjeto ou literal de objeto de Stringpares chave/valor (consulte Cabeçalhos HTTP para obter uma referência; Por padrão, isso está vazio.
### Propriedades
```js
Response.headers: Contém o objeto Headers associado à resposta;

Response.ok: Contém um valor booleano indicando se a resposta foi bem sucedida ("status" no intervalo 200-299) ou não;

Response.redirected: Indica se a resposta é ou não o resultado de um redirecionamento; isto é, sua lista de URL tem mais de uma entrada;

Response.status: Contém o código de "status" da resposta (ex., 200 para um sucesso);

Response.statusText: Contém a mensagem de "status" correspondente ao código de "status" (ex., OK para 200);

Response.type: Contém o tipo da resposta (ex., basic, cors);

Response.url: Contém a URL de resposta;

Response.useFinalURL: Contém um valor boleano indicando se essa é a URL final da resposta;
```
##### Response implementa Body, por isso também tem as seguintes propriedades disponíveis:
```js
Body.body: Um simples "getter" para ler do conteúdo do corpo através da interface ReadableStream.

Body.bodyUsed: Armazena um Boolean que indica se o corpo já foi utilizado em uma resposta.
```
#### Métodos
```js
Response.clone(): Cria uma cópia do objeto Response.

Response.error(): Retorna um novo objeto Response associado a um erro de rede.

Response.redirect(): Cria uma nova resposta com uma URL diferente.

Response implementa Body, por isso também tem as seguintes propriedades disponíveis:

Body.arrayBuffer(): Recebe um "stream" Response e lê até a conclusão. Retorna uma "promise" que resolve com um ArrayBuffer.

Body.blob(): Recebe um "stream" Response e lê até a conclusão. Retorna uma "promise" que resolve com um Blob.

Body.formData(): Recebe um "stream" Response e lê até a conclusão. Retorna uma "promise" que resolve com um objeto FormData.

Body.json(): Recebe um "stream" Response e lê até a conclusão. Retorna uma "promise" que resolve com o resultado do parseamento do texto do corpo como JSON.

Body.text(): Recebe um "stream" Response e lê até a conclusão. Retorna uma "promise" que resolve com um USVString (texto).
```


---
Fontes:
- https://developer.mozilla.org/en-US/docs/Web/API/Response/Response
Tags: #softwaredevelopment 