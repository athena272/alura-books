# Configuração SSL para Desenvolvimento

## Gerando certificados SSL auto-assinados

Para desenvolvimento local com HTTPS, execute o seguinte comando:

```bash
openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout server.key -out server.crt
```

## Arquivos gerados

- `server.key` - Chave privada (NÃO commitar no git)
- `server.crt` - Certificado público (NÃO commitar no git)

## Configuração do servidor

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

## Notas importantes

- Estes certificados são apenas para desenvolvimento
- Para produção, use certificados válidos de uma CA
- Os arquivos `.key` e `.crt` estão no `.gitignore` por segurança 