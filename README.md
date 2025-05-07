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
## 📬 Registro de usuários
Para se registrar, envie uma requisição POST para:
```
http://localhost:8000/register
```
## 📝 Licença
Este projeto está licenciado sob os termos da licença MIT. Veja o arquivo [LICENSE](./LICENSE) para mais informações.

