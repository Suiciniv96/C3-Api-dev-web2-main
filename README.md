Guia de Configuração e Execução
Passos Iniciais
Clone o repositório do projeto.
Execute npm install para instalar todas as dependências necessárias.
Configure o banco de dados executando npm run prisma.
Compile e inicie a aplicação com npm run build.
A aplicação estará pronta para uso.
Utilizando Docker
Verifique se o Docker está instalado e configurado corretamente em sua máquina.
Na raiz do projeto, construa a imagem Docker com o comando:
docker build -t api-dev-web .
Após a conclusão da build, inicie o container com o comando:
docker run -p 3000:3000 api-dev-web
A API estará disponível em http://localhost:3000.
Autenticação de Usuários
Registro de Usuário
Para registrar um novo usuário, envie uma requisição POST para:

http://localhost:3000/api/auth/signup
Corpo da requisição (JSON):

{
    "name": "nomeDeUsuario",
    "email": "seuemail@gmail.com",
    "password": "suasenha123"
}
Login de Usuário
Para fazer login, envie uma requisição POST para:

http://localhost:3000/api/auth/signin
Corpo da requisição (JSON):

{
    "email": "seuemail@gmail.com",
    "password": "suasenha123"
}
O token retornado deve ser incluído no cabeçalho das próximas requisições:

Authorization: Bearer codigo_token
Exemplos de Uso da API
Listar Usuários
Para obter a lista de usuários, envie uma requisição GET para:

http://localhost:3000/api/users
Criar um Post
Para criar um novo post, envie uma requisição POST para:

http://localhost:3000/api/post
Corpo da requisição (JSON):

{
    "title": "Título do post",
    "content": "Conteúdo do post",
    "authorId": 1,
    "published": true
}
authorId é o ID do usuário que está criando o post.

Listar Posts
Para obter a lista de posts, envie uma requisição GET para:

http://localhost:3000/api/posts
Criar um Comentário
Para adicionar um comentário a um post, envie uma requisição POST para:

http://localhost:3000/api/comment
Corpo da requisição (JSON):

{
    "content": "Conteúdo do comentário",
    "postId": 3
}
postId é o ID do post onde o comentário será adicionado.

Listar Comentários de um Post
Para obter os comentários de um post específico, envie uma requisição GET para:

http://localhost:3000/api/posts/3/comments
Substitua 3 pelo ID do post cujos comentários você deseja listar.
