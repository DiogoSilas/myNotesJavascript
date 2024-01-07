>Nunca versionar a pasta "node_modules"


O NPM é uma ferramenta essencial para o desenvolvimento de projetos JavaScript, permitindo que você instale, atualize e gerencie facilmente as dependências do seu projeto. Uma biblioteca com códigos prontos para usar.

Geralmente vamos utilizar linhas de comando:
```bash
$ npm install nome-do-pacote
```

Ou utilizar o package.json - [[JSON - JavaScript Object Notation - Notação de Objetos JavaScript]].

### Instalar o NPM
Quando baixamos no Node.Js o NPM é instalado junto, caso tenha o node instalado, entre no terminal Git Bash e digite
```
npm --version
```
Caso não apareça nada ou de algum erro, instale outra vez o Node.Js

### Iniciar o NPM
Abrir o terminal powershell na raiz do projeto que desejo usar o NPM
- npm init
- No package: usando_npm
- descrition: texto desejado sobre o arquivo
- entry point: (indec.js)
- keywords: javascript, npm
- author: Diogo Silas
- Licença, deixar padrão
- Is this OK? (yes) yes
Vai ser criado om arquivo [[JSON - JavaScript Object Notation - Notação de Objetos JavaScript]] com as informações colocadas.

### Instalando Pacotes
- **npm install** nome-do-pacote **--save**
- O save é para instalar na lista de dependência do pacote .json

>Nunca versionar a pasta "node_modules"

- npm install vai instalar todos os pacotes dependentes e instalar no meu computador.

---
Fontes:
- https://www.npmjs.com/
Tag: #softwaredevelopment 