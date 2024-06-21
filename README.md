
# 🚀 Projeto Node.js com Prisma e Docker 🌟


## Índice 📚
- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Executando a Aplicação](#executando-a-aplicação)
- [Utilizando Docker](#utilizando-docker)
- [Autenticação](#autenticação)
  - [Registrar](#registrar)
  - [Logar](#logar)
- [Exemplos de Uso da API](#exemplos-de-uso-da-api)
  - [Listar Usuários](#listar-usuários)
  - [Criar Post](#criar-post)
  - [Listar Posts](#listar-posts)
  - [Criar Comentário](#criar-comentário)
  - [Listar Comentários por Post](#listar-comentários-por-post)
- [Contribuição](#contribuição)
- [Licença](#licença)

## Pré-requisitos

- Node.js v18+
- Docker (opcional, mas recomendado)

## Instalação

1. Clone este repositório:
   ```sh
   git clone https://github.com/seuusuario/seuprojeto.git
   cd seuprojeto
   ```

2. Instale as dependências:
   ```sh
   npm install
   ```

3. Gere o banco de dados:
   ```sh
   npm run prisma
   ```

## Executando a Aplicação

1. Compile o projeto:
   ```sh
   npm run build
   ```

2. Inicie o servidor:
   ```sh
   npm start
   ```

3. A API estará disponível em `http://localhost:3000`.

## Utilizando Docker

1. Construa a imagem Docker:
   ```sh
   docker build -t api-dev-web .
   ```

2. Execute o container Docker:
   ```sh
   docker run -p 3000:3000 api-dev-web
   ```

3. Acesse a API em `http://localhost:3000`.

## Autenticação

### Registrar

Para registrar um novo usuário, envie uma requisição POST para:
```
http://localhost:3000/api/auth/signup
```
Corpo da requisição (JSON):
```json
{
    "name": "nomeDeUsuario",
    "email": "seuemail@gmail.com",
    "password": "suasenha123"
}
```

### Logar

Para autenticar um usuário, envie uma requisição POST para:
```
http://localhost:3000/api/auth/signin
```
Corpo da requisição (JSON):
```json
{
    "email": "seuemail@gmail.com",
    "password": "suasenha123"
}
```
Inclua o token retornado no cabeçalho das próximas requisições:
```
Authorization: Bearer seu_token_aqui
```

## Exemplos de Uso da API

### Listar Usuários

Para obter a lista de usuários, faça uma requisição GET para:
```
http://localhost:3000/api/users
```

### Criar Post

Para criar um novo post, envie uma requisição POST para:
```
http://localhost:3000/api/post
```
Corpo da requisição (JSON):
```json
{
    "title": "Título do post",
    "content": "Conteúdo do post",
    "authorId": 1,
    "published": true
}
```

### Listar Posts

Para obter a lista de posts, faça uma requisição GET para:
```
http://localhost:3000/api/posts
```

### Criar Comentário

Para adicionar um comentário a um post, envie uma requisição POST para:
```
http://localhost:3000/api/comment
```
Corpo da requisição (JSON):
```json
{
    "content": "Conteúdo do comentário",
    "postId": 3
}
```

### Listar Comentários por Post

Para obter os comentários de um post específico, faça uma requisição GET para:
```
http://localhost:3000/api/posts/3/comments
```
Substitua `3` pelo ID do post cujos comentários deseja listar.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

1. Fork este repositório.
2. Crie um branch para sua feature (`git checkout -b feature/nova-feature`).
3. Commit suas mudanças (`git commit -am 'Adiciona nova feature'`).
4. Push para o branch (`git push origin feature/nova-feature`).
5. Crie um novo Pull Request.

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Divirta-se explorando e melhorando este projeto! 🚀😊
