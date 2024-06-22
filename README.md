
# 🚀 Projeto Node.js com Prisma e Docker 🌟


## Índice 📚
- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Executando a Aplicação](#executando-a-aplicação)
- [Utilizando Docker](#utilizando-docker)



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



