A [[Fetch API]] fornece uma interface JavaScript para acessar e manipular partes do pipeline HTTP, tais como os pedidos e respostas. Ela também fornece o [[Método fetch()]] que fornece uma maneira fácil e lógica para buscar recursos de forma assíncrona ([[Síncrono vs Assíncrono - JavaScript]]) através da rede.

Este tipo de funcionalidade era obtida anteriormente utilizando "XMLHttpRequest". Fetch fornece uma alternativa melhor que pode ser facilmente utilizada por outras tecnologias como **Service Workers**. Fetch também provê um lugar lógico único para definir outros conceitos relacionados ao protocolo HTTP como CORS e extensões ao HTTP.

Note que a especificação [[Método fetch()]] difere de **jQuery.ajax()**, principalmente, de três formas:
- A Promise retornada do fetch() não rejeitará o status do erro HTTP, mesmo que a resposta seja um HTTP 404 ou 500. Em vez disso, ela irá resolver normalmente (com o status ok definido como falso), e só irá rejeitar se houver falha na rede ou se algo impedir a requisição de ser completada.
- fetch() não receberá cookies cross-site; você não pode estabelecer uma conexão cross-site usando fetch. Cabeçalhos Set-Cookie de outros sites são ignorados silenciosamente.
- fetch() não enviará cookies, a não ser que seja definida a opção credentials do parâmetro init.

**Fetch API support** pode ser detectada na existência do escopo Headers, [[Request]], [[Response]] ou [[Método fetch()]] no **Window** ou **Worker** . Por exemplo, faça o seguinte teste no seu código:
```js
if (self.fetch) {
  // execute minha solicitação do fetch aqui
} else {
  // faça alguma coisa com XMLHttpRequest?
}
```

---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/API/Fetch_API/Using_Fetch
Tags: #softwaredevelopment 