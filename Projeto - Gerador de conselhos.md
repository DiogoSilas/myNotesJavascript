### Passos:
1. Pegar o elemento de **botão** para ser adicionado o **evento de clique** nele.
2. Pegar o elemento de **id do conselho**.
3. Pegar o elemento de **descrição do conselho**.
4. Após conseguirmos os elementos do html, é necessário a criação da **([[Function - JavaScript]]) responsável por pegar os dados da API** ([[API - Application Programming Interface]], [[Consumir Qualquer API]] e [[Fetch API]]). A melhor forma de se consumir a API é usando **async await** ([[Async e Await - Function]]). Caso não tenha visto a aula, sugiro que assista novamente. Nas referências ficará um link com exemplos.
5. Dentro da função, após pegarmos os dados da API, é necessário atualizar o conteúdo do id e descrição do conselho que colocamos em uma variável usando o **innerHTML**. [[Adição de Elementos com JsvaScript]]
6. Por fim, basta chamar a função criada.
7. Atribuir a função que criamos para ser executada no evento do clique do botão ou se preferir, criar o escopo da função dentro do listener.
#### Meus erros:
>Chamadas de funções assíncronas: Quando você usa funções assíncronas como geradorDeConselhosAleatorios, conselhosAleatorios e mostrarUmConselhoAleatorio, elas retornam Promises, então é necessário usar await para aguardar o resultado delas.

>Uso incorreto de variáveis e acesso aos dados retornados pelas Promises: O retorno das funções assíncronas não pode ser acessado diretamente com [PromiseResult]. É necessário aguardar o resultado dessas funções usando await ([[Async e Await - Function]]) ou [[Then - Promise.prototype.then()]] para acessar os dados corretamente.

>Estruturação inadequada da lógica de obtenção e exibição dos conselhos: Você pode criar uma [[Function - JavaScript]] separada para buscar um conselho aleatório e, quando clicar no botão, chamar essa função para exibir o conselho na página. **Exemplo: [[Projeto mostrar cartões]]**
#### Solução
Aqui está uma versão corrigida do seu código:

```javascript
const btnAdvice = document.getElementById('btn-advice');
const adviceDisplay = document.getElementById('advice-display');

btnAdvice.addEventListener('click', async function() {
    async function obterConselhoAleatorio() {
        const url = 'https://api.adviceslip.com/advice';
        const response = await fetch(url);
        const data = await response.json();
        return data.slip.advice;
    }

    try {
        const conselho = await obterConselhoAleatorio();
        adviceDisplay.textContent = conselho;
    } catch (error) {
        console.error('Ocorreu um erro ao buscar o conselho:', error);
    }
});
```
>Neste código corrigido, ao clicar no botão com ID 'btn-advice', a função obterConselhoAleatorio é acionada. Essa função faz uma requisição à API, aguarda a resposta e, em seguida, exibe o conselho retornado no elemento com ID 'advice-display'.

Certifique-se de ter um elemento HTML com esse ID para exibir o conselho. Além disso, utilizei [[try catch - Tratando Erros no JavaScript]] para capturar possíveis erros que possam ocorrer durante a obtenção do conselho e exibi-los no console para facilitar a depuração.

Lembre-se de substituir 'advice-display' pelo ID do elemento HTML onde você deseja exibir o conselho retornado pela [[API - Application Programming Interface]].

### Mostrar o número do conselho
Para adicionar o número do conselho dentro de uma tag `<span>` no HTML, você pode modificar a função `obterConselhoAleatorio()` para retornar não apenas o conselho, mas também o número associado a ele. Aqui está um exemplo de como você pode fazer isso:

```javascript
const btnAdvice = document.getElementById('btn-advice');
const numeroAdvice = document.getElementById('number-advice');
const adviceDisplay = document.getElementById('advice-display');
btnAdvice.addEventListener('click', async function() {
    async function obterConselhoAleatorio() {
        const url = 'https://api.adviceslip.com/advice';
        const response = await fetch(url);
        const data = await response.json();
        return {
            numero: data.slip.id,
            conselho: data.slip.advice
        };
    }
    try {
        const { numero, conselho } = await obterConselhoAleatorio();
        adviceDisplay.textContent = conselho;
        numeroAdvice.textContent = numero;
    } catch (error) {
        console.error('Ocorreu um erro ao buscar o conselho:', error);
    }
});
```

Neste código, a função **obterConselhoAleatorio()** retorna um objeto com duas propriedades: `numero` e `conselho`. O número do conselho é obtido a partir de **data.slip.id** e o conselho em si é extraído de **data.slip.advice**.

Além de exibir o conselho no elemento com ID **'advice-display'**. Assim, ao clicar no botão, você verá o conselho exibido junto com o número dentro da [[Tag Span]] no HTML. Certifique-se de que o elemento HTML com ID **'advice-display'** exista na sua página para a exibição correta.

---
Fontes:
- Documentação da API: https://api.adviceslip.com/
- https://www.frontendmentor.io/challenges/advice-generator-app-QdUG-13db
Tags: #softwaredevelopment 