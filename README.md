# OpenMessage
Um serviço de mensagens OpenSource!

# Tutorial de Uso
[Clique aqui](./tutorial-de-uso.md) para acessar o Tutorial de Uso!

# Documentação Técnica - OpenMessage

## Tópicos
- Tópicos
- Endpoints
  - Login
  - Registro
  - Enviar Mensagens
  - Criar Servidor
  - Criar Canais
  - Listar Servidores
  - Listar Canais de um Servidor
  - Listar Mensagens de um Servidor
  - Buscar nick do usuário por ID
  - Socket
- Fluxos
- Sobre o Socket
- Finalização
- Licença
- Créditos

## Endpoints
Nesse tópico, daremos exemplos de cada um dos endpoints.

## Endpoints - Login (/login)

### Tipo de Requisição: 
- POST
### Como enviar: 
- BODY da requisição
### Informações que devem ser enviadas: 
- `user` e `tokenaes`. User é o nome do usuário que foi criado no Registro, e o TokenAES é o que foi gerado ao se registrar.

### Exemplo de resposta:
```
{ message: "Login bem-sucedido" }
```


## Endpoints - Registro (/register)

### Tipo de Requisição:
- POST
### Como enviar:
- BODY da requisição
### Informações que devem ser enviadas:
- O único valor que deve ser enviado é o `user`. Que é o nome de usuário.
### Exemplo de resposta:
```
{ message: "Registro bem-sucedido", "token aes do usuário"}
```


## Endpoints - Enviar Mensagem (/send-message)

### Tipo de Requisição:
- POST
### Como enviar:
- BODY da requisição
### Informações que devem ser enviadas:
- Os dados que devem ser enviados são: `channelId`, `serverId` e `message`.
### Exemplo de resposta:
```
{ message: "Mensagem enviada" }
```


## Endpoints - Criar Servidor (/create-server)

### Tipo de Requisição:
- POST
### Como enviar:
- BODY da requisição
### Informações que devem ser enviadas:
- Os dados que devem ser enviados são: `name`, e `description`.
### Exemplo de resposta:
```
{ message: "Servidor criado", serverId: "ID DO SERVIDOR" }
```


## Endpoints - Criar Canal (/create-channel)

### Tipo de Requisição:
- POST
### Como enviar:
- BODY da requisição
### Informações que devem ser enviadas:
- Os dados que devem ser enviados são: `serverId`, `name` e `description`.
### Exemplo de resposta:
```
{ message: "Canal criado", channelId: "ID DO CANAL" }
```


## Endpoints - Listar Servidores (/servers)

### Tipo de Requisição:
- GET
### Como enviar:
- NULL (Ele não pede nenhuma informação)
### Informações que devem ser enviadas:
- NULL (Ele não pede nenhuma informação)
### Exemplo de resposta:
```
[{"id":1,"name":"OpenMessage","description":"Servidor Oficial do OpenMessage"}]
```


## Endpoints - Listar canais de um servidor (/channels/ID-DO-SERVIDOR-AQUI/messages)

### Tipo de Requisição:
- GET
### Como enviar:
- NULL (Ele não pede nenhuma informação além da passada na URL)
### Informações que devem ser enviadas:
- NULL (Ele não pede nenhuma informação além da passada na URL)
### Exemplo de resposta:
```
[{"id":1,"userId":1,"channelId":1,"serverId":1,"message":"O server foi resetado meu povo","timestamp":"2025-02-23 01:03:07"},{"id":2,"userId":1,"channelId":1,"serverId":1,"message":"skasksak","timestamp":"2025-02-23 01:03:09"},{"id":3,"userId":1,"channelId":1,"serverId":1,"message":"Beta é assim, some e volta","timestamp":"2025-02-23 01:03:18"},{"id":4,"userId":1,"channelId":1,"serverId":1,"message":"Em fim","timestamp":"2025-02-23 18:08:26"},{"id":5,"userId":1,"channelId":1,"serverId":1,"message":"vou spammar um pouco pra testar uma parada","timestamp":"2025-02-23 18:08:36"},{"id":6,"userId":1,"channelId":1,"serverId":1,"message":"então ignorem","timestamp":"2025-02-23 18:08:38"},{"id":7,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:40"},{"id":8,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:40"},{"id":9,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:40"},{"id":10,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:41"},{"id":11,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:41"},{"id":12,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:42"},{"id":13,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:42"},{"id":14,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:42"},{"id":15,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:43"},{"id":16,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:43"},{"id":17,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:43"},{"id":18,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:43"},{"id":19,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:44"},{"id":20,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:44"},{"id":21,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:44"},{"id":22,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:44"},{"id":23,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:45"},{"id":24,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:45"},{"id":25,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:45"},{"id":26,"userId":1,"channelId":1,"serverId":1,"message":".","timestamp":"2025-02-23 18:08:45"},{"id":27,"userId":1,"channelId":1,"serverId":1,"message":"6565654","timestamp":"2025-02-23 18:08:47"},{"id":28,"userId":1,"channelId":1,"serverId":1,"message":"654","timestamp":"2025-02-23 18:08:47"},{"id":29,"userId":1,"channelId":1,"serverId":1,"message":"654","timestamp":"2025-02-23 18:08:47"},{"id":30,"userId":1,"channelId":1,"serverId":1,"message":"654","timestamp":"2025-02-23 18:08:48"},{"id":31,"userId":1,"channelId":1,"serverId":1,"message":"654","timestamp":"2025-02-23 18:08:48"},{"id":32,"userId":1,"channelId":1,"serverId":1,"message":"654","timestamp":"2025-02-23 18:08:48"},{"id":33,"userId":1,"channelId":1,"serverId":1,"message":"654","timestamp":"2025-02-23 18:08:48"},{"id":34,"userId":1,"channelId":1,"serverId":1,"message":"65","timestamp":"2025-02-23 18:08:49"},{"id":35,"userId":1,"channelId":1,"serverId":1,"message":"56","timestamp":"2025-02-23 18:08:49"},{"id":36,"userId":1,"channelId":1,"serverId":1,"message":"6","timestamp":"2025-02-23 18:08:49"},{"id":37,"userId":1,"channelId":1,"serverId":1,"message":"6","timestamp":"2025-02-23 18:08:50"},{"id":38,"userId":1,"channelId":1,"serverId":1,"message":"6","timestamp":"2025-02-23 18:08:50"},{"id":39,"userId":1,"channelId":1,"serverId":1,"message":"6","timestamp":"2025-02-23 18:08:50"},{"id":40,"userId":1,"channelId":1,"serverId":1,"message":"6","timestamp":"2025-02-23 18:08:50"},{"id":41,"userId":1,"channelId":1,"serverId":1,"message":"6","timestamp":"2025-02-23 18:08:50"},{"id":42,"userId":1,"channelId":1,"serverId":1,"message":"5","timestamp":"2025-02-23 18:08:51"},{"id":43,"userId":1,"channelId":1,"serverId":1,"message":"56","timestamp":"2025-02-23 18:08:51"},{"id":44,"userId":1,"channelId":1,"serverId":1,"message":"6","timestamp":"2025-02-23 18:08:51"},{"id":45,"userId":1,"channelId":1,"serverId":1,"message":"6","timestamp":"2025-02-23 18:08:52"},{"id":46,"userId":1,"channelId":1,"serverId":1,"message":"6","timestamp":"2025-02-23 18:08:52"},{"id":47,"userId":1,"channelId":1,"serverId":1,"message":"3","timestamp":"2025-02-23 18:08:53"},{"id":48,"userId":1,"channelId":1,"serverId":1,"message":"2","timestamp":"2025-02-23 18:08:53"},{"id":49,"userId":1,"channelId":1,"serverId":1,"message":"58","timestamp":"2025-02-23 18:08:53"},{"id":50,"userId":1,"channelId":1,"serverId":1,"message":"4","timestamp":"2025-02-23 18:08:54"},{"id":51,"userId":1,"channelId":1,"serverId":1,"message":"8","timestamp":"2025-02-23 18:08:54"},{"id":52,"userId":1,"channelId":1,"serverId":1,"message":"76","timestamp":"2025-02-23 18:08:54"},{"id":53,"userId":1,"channelId":1,"serverId":1,"message":"8~34","timestamp":"2025-02-23 18:08:55"},{"id":54,"userId":1,"channelId":1,"serverId":1,"message":"789","timestamp":"2025-02-23 18:08:56"},{"id":55,"userId":1,"channelId":1,"serverId":1,"message":"45","timestamp":"2025-02-23 18:08:56"},{"id":56,"userId":1,"channelId":1,"serverId":1,"message":"234","timestamp":"2025-02-23 18:08:56"},{"id":57,"userId":1,"channelId":1,"serverId":1,"message":"534","timestamp":"2025-02-23 18:08:56"},{"id":58,"userId":1,"channelId":1,"serverId":1,"message":"675","timestamp":"2025-02-23 18:08:57"},{"id":59,"userId":1,"channelId":1,"serverId":1,"message":"89","timestamp":"2025-02-23 18:08:57"},{"id":60,"userId":1,"channelId":1,"serverId":1,"message":"790","timestamp":"2025-02-23 18:08:57"},{"id":61,"userId":1,"channelId":1,"serverId":1,"message":"678","timestamp":"2025-02-23 18:08:57"},{"id":62,"userId":1,"channelId":1,"serverId":1,"message":"65","timestamp":"2025-02-23 18:08:58"},{"id":63,"userId":1,"channelId":1,"serverId":1,"message":"234","timestamp":"2025-02-23 18:08:58"},{"id":64,"userId":1,"channelId":1,"serverId":1,"message":"234","timestamp":"2025-02-23 18:08:58"},{"id":65,"userId":1,"channelId":1,"serverId":1,"message":"65","timestamp":"2025-02-23 18:08:58"},{"id":66,"userId":1,"channelId":1,"serverId":1,"message":"689","timestamp":"2025-02-23 18:08:59"},{"id":67,"userId":1,"channelId":1,"serverId":1,"message":"78","timestamp":"2025-02-23 18:08:59"},{"id":68,"userId":1,"channelId":1,"serverId":1,"message":"5234","timestamp":"2025-02-23 18:08:59"},{"id":69,"userId":1,"channelId":1,"serverId":1,"message":"67","timestamp":"2025-02-23 18:09:00"},{"id":70,"userId":1,"channelId":1,"serverId":1,"message":"789","timestamp":"2025-02-23 18:09:00"},{"id":71,"userId":1,"channelId":1,"serverId":1,"message":"678","timestamp":"2025-02-23 18:09:00"},{"id":72,"userId":1,"channelId":1,"serverId":1,"message":"534","timestamp":"2025-02-23 18:09:01"},{"id":73,"userId":1,"channelId":1,"serverId":1,"message":"53454","timestamp":"2025-02-23 18:09:01"},{"id":74,"userId":1,"channelId":1,"serverId":1,"message":"6534","timestamp":"2025-02-23 18:09:01"},{"id":75,"userId":1,"channelId":1,"serverId":1,"message":"789","timestamp":"2025-02-23 18:09:02"},{"id":76,"userId":1,"channelId":1,"serverId":1,"message":"65","timestamp":"2025-02-23 18:09:02"},{"id":77,"userId":1,"channelId":1,"serverId":1,"message":"654","timestamp":"2025-02-23 18:09:03"},{"id":78,"userId":1,"channelId":1,"serverId":1,"message":"6785","timestamp":"2025-02-23 18:09:03"},{"id":79,"userId":1,"channelId":1,"serverId":1,"message":"689","timestamp":"2025-02-23 18:09:03"},{"id":80,"userId":1,"channelId":1,"serverId":1,"message":"534","timestamp":"2025-02-23 18:09:04"},{"id":81,"userId":1,"channelId":1,"serverId":1,"message":"234","timestamp":"2025-02-23 18:09:04"},{"id":82,"userId":1,"channelId":1,"serverId":1,"message":"785","timestamp":"2025-02-23 18:09:04"},{"id":83,"userId":1,"channelId":1,"serverId":1,"message":"789","timestamp":"2025-02-23 18:09:05"},{"id":84,"userId":1,"channelId":1,"serverId":1,"message":"87","timestamp":"2025-02-23 18:09:05"},{"id":85,"userId":1,"channelId":1,"serverId":1,"message":"5234","timestamp":"2025-02-23 18:09:05"},{"id":86,"userId":1,"channelId":1,"serverId":1,"message":"78","timestamp":"2025-02-23 18:09:06"},{"id":87,"userId":1,"channelId":1,"serverId":1,"message":"8","timestamp":"2025-02-23 18:09:06"},{"id":88,"userId":1,"channelId":1,"serverId":1,"message":"8","timestamp":"2025-02-23 18:09:06"},{"id":89,"userId":1,"channelId":1,"serverId":1,"message":"8","timestamp":"2025-02-23 18:09:06"},{"id":90,"userId":1,"channelId":1,"serverId":1,"message":"8","timestamp":"2025-02-23 18:09:07"},{"id":91,"userId":1,"channelId":1,"serverId":1,"message":"78","timestamp":"2025-02-23 18:09:07"},{"id":92,"userId":1,"channelId":1,"serverId":1,"message":"Teste","timestamp":"2025-02-23 18:09:08"},{"id":93,"userId":1,"channelId":1,"serverId":1,"message":"123","timestamp":"2025-02-23 18:09:09"},{"id":94,"userId":1,"channelId":1,"serverId":1,"message":"tESTE","timestamp":"2025-02-23 18:09:10"},{"id":95,"userId":1,"channelId":1,"serverId":1,"message":"123","timestamp":"2025-02-23 18:09:12"},{"id":96,"userId":1,"channelId":1,"serverId":1,"message":"lazy loading","timestamp":"2025-02-23 18:09:17"},{"id":97,"userId":1,"channelId":1,"serverId":1,"message":"sla","timestamp":"2025-02-23 18:09:17"},{"id":98,"userId":1,"channelId":1,"serverId":1,"message":"pronto","timestamp":"2025-02-23 18:09:20"},{"id":99,"userId":1,"channelId":1,"serverId":1,"message":"spam finalizado","timestamp":"2025-02-23 18:09:22"},{"id":100,"userId":1,"channelId":1,"serverId":1,"message":"teste2","timestamp":"2025-02-23 18:26:20"}]
```


## Endpoints - Buscar nome de usuário pelo ID (/user/ID-DO-USUÁRIO-AQUI)

### Tipo de Requisição:
- GET
### Como enviar:
- NULL (Ele não pede nenhuma informação além da passada na URL)
### Informações que devem ser enviadas:
- NULL (Ele não pede nenhuma informação além da passada na URL)
### Exemplo de resposta:
```
{"username":"op3n"}
```



# Fluxos
Esse projeto não tem fluxos, pois, nenhum endpoint depende diretamente do outro para funcionar. Resumo... pula pro próximo 👍

# Sobre o Socket
O Socket está sendo utilizado nesse projeto, como uma forma de enviar e receber mensagens em tempo real. Ele tem seu papel no projeto, e fizemos essa parte da documentação, apenas para te informar que sim, esse projeto utiliza WebSocket.

# Finalização
Agradecemos pela sua escolha, e estamos abertos para melhorias... Achou um bug? Só abrir um PR. Em fim, agradecemos de coração pela sua escolha.

# Licença
Esse projeto está sob as condições da licença [unlicense](./LICENSE).

# Créditos
Esse projeto foi criado e idealizado pelo [op3n/op3ny](https://github.com/op3ny).
Design refeito pela [AuryChar/aury_dev](https://github.com/AuryChar)

# Hsyst
A Hsyst Project... Bye!
