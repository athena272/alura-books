# AluraBooks 📚

O **AluraBooks** é uma loja virtual de livros da Casa do Código, criada como um MVP com potencial para futuras funcionalidades. Este repositório contém o front-end e o back-end da aplicação.

## 🧭 Estrutura do Projeto

```plaintext
alura-books-main/
├── front/   # Aplicação React (interface do usuário)
├── back/    # API mockada com json-server + JWT
└── README.md (este arquivo)
```
## 🖥️ Front-end
A aplicação foi desenvolvida em React, com a página inicial já disponível. Você pode usá-la como base ou criar sua própria versão.
### 🔨 Funcionalidades
- Página inicial estilizada
- Interface responsiva
- Integração com API REST mockada
### ▶️ Como rodar
```
cd front
npm install
npm start
```
## 🔧 Back-end
API REST mockada usando json-server com autenticação JWT.
###🚀 Como rodar
```
cd back
npm install
npm run start-auth
```

## 🔒 Configuração SSL para Desenvolvimento

### Gerando certificados SSL auto-assinados

Para desenvolvimento local com HTTPS, dentro da basta **back**, execute o seguinte comando:

```bash
openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout server.key -out server.crt
```

### Arquivos gerados

- `server.key` - Chave privada (NÃO commitar no git)
- `server.crt` - Certificado público (NÃO commitar no git)

### Configuração do servidor

Para usar HTTPS, modifique o `server.js` para incluir:

```javascript
const https = require('https');
const fs = require('fs');

const options = {
  key: fs.readFileSync('./server.key'),
  cert: fs.readFileSync('./server.crt')
};

https.createServer(options, server).listen(8000, () => {
  console.log("API HTTPS disponível em https://localhost:8000");
});
```

### Notas importantes

- Estes certificados são apenas para desenvolvimento
- Para produção, use certificados válidos de uma CA
- Os arquivos `.key` e `.crt` estão no `.gitignore` por segurança

## 📬 Registro de usuários
Para se registrar, envie uma requisição POST para:
```
http://localhost:8000/register
```
## 📝 Licença
Este projeto está licenciado sob os termos da licença MIT. Veja o arquivo [LICENSE](./LICENSE) para mais informações.

