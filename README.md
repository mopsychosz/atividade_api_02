# Filmes API REST

API RESTful para gerenciamento de um catálogo de filmes, desenvolvida em Node.js e Express com foco em arquitetura limpa (MVC).

## Tecnologias Utilizadas
- Node.js
- Express.js
- Nodemon (Desenvolvimento)

## Arquitetura
O projeto utiliza o padrão MVC (Model-View-Controller) modificado para APIs:
- **Models:** Gerenciamento dos dados (array em memória para este projeto).
- **Controllers:** Regras de negócio e orquestração das requisições/respostas.
- **Routes:** Definição limpa dos endpoints.
- **Middlewares:** Interceptadores para validação de dados e tratamento global de erros.

## Instalação e Execução

1. Clone o repositório.
2. Instale as dependências: `npm install`
3. Inicie o servidor: `npm run dev` (A API rodará em `http://localhost:3000`)

## Endpoints

| Método | Rota                | Descrição                      | Status Sucesso | Status Erro     |
|--------|---------------------|--------------------------------|----------------|-----------------|
| GET    | `/api/filmes`       | Lista todos os filmes          | 200            | -               |
| GET    | `/api/filmes/:id`   | Busca um filme pelo ID         | 200            | 404             |
| POST   | `/api/filmes`       | Cria um novo filme             | 201            | 400             |
| PUT    | `/api/filmes/:id`   | Atualiza um filme existente    | 200            | 400, 404        |
| DELETE | `/api/filmes/:id`   | Remove um filme                | 204            | 404             |

## Documentação e Testes (Postman)
O arquivo `postman_collection.json` na raiz do projeto contém todas as rotas pré-configuradas e testes automatizados (`pm.test`) para validação de status codes e tipos de retorno.
