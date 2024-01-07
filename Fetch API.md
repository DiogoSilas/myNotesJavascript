O Fetch fornece uma definição genérica de objetos de [[Request]] e [[Response]] (e outras coisas envolvidas com solicitações de rede). Isso permitirá que eles sejam usados onde quer que sejam necessários no futuro, seja para service workers, Cache API e outras coisas similares que manipulam ou modifiquem pedidos e respostas ou qualquer tipo de caso de uso que possa exigir que você gere suas próprias responses programaticamente.

Ele também fornece uma definição para conceitos relacionados como CORS e a semântica de cabeçalho de origem HTTP, suplantando suas definições separadas em outro lugar.

O [[Método fetch()]] tem um argumento obrigatório, **o caminho para o recurso que deseja obter**. Ele retorna uma promessa que resolve a [[Response]] para esta requisição, **seja ele bem-sucedido ou não**. Você também pode, opcionalmente, passar um objeto de opções de inicialização como o segundo argumento.

>Uma vez que uma Response é recuperada, há uma série de métodos disponíveis para definir o conteúdo do corpo e como ele deve ser tratado.

---
Fontes:
- https://developer.mozilla.org/pt-BR/docs/Web/API/Fetch_API
Tags: #softwaredevelopment 