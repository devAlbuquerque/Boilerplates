# Node com Typescript

### **Instalação**

1. Crie uma pasta [server] e execute os codigos abaixo para instalacao. 
1. Use `npm init -y` para iniciar um projeto com configuracoes padroes. O package.json contem as informacoes principais do projeto.
1. Use `npm install typescript -D` para realizar a instalacao do typescript.
1. Use `npx tsc --init` para criar o arquivo de configuracoes do typescript.
1. Use `npm install ts-node -D`, como o node so "entende" JS, instalamos esta dependencia para ser possivel sua execucao. Com o "-D" porque so sera utilizado enquanto estiver desenvolvendo a aplicacao.
1. Use `npm install express -D` Para ser possivel trabalhar com aplicacoes web.

Apos os passos acima realizados, crie uma pasta **src** e um arquivo **server.ts**, com o seguinte conteudo:

```
server.ts

import express from 'express';

const app = express();

app.get('/users', (request, response) => {
    console.log('Iniciou')
    //response.send('Hello World');
    response.json(['Nome1','Nome2','Nome3','Nome4'])
});

app.listen(3333);
```

### **Observacoes/Utilitarios**

- O *node_modules* armazena as dependencias.
- **-D** dependencia de desenvolvimento
- **npx** - executa um pacote instalado
- `npx ts-node src/server.ts` E o comando utilizado para executar a aplicacao.
- `npm install ts-node-dev -D` Utilizado para nao ter que ficar reiniciando o servidor a todo momento com o CTRL + C, ele ficara observando a todo momento as mudancas na app.

Como forma melhorada para evitar sempre ficar escrevendo um comando muito grande, segue exemplo de script a ser adicionado no package.json.

`dev" : "ts-node-dev src/server.ts;`

Agora basta executar `npm run dev` no terminal.