Mini Blog com Markdown

Este é um projeto de um mini blog com autenticação e suporte a Markdown.
O objetivo é praticar consumo de API, organização de frontend e estrutura básica de um sistema fullstack.

Funcionalidades
Cadastro de usuário
Login com autenticação via token (JWT)
Criar posts em Markdown
Listar posts
Visualizar post individual
Editar e excluir posts (apenas do autor)
Tecnologias
Frontend
HTML
Bootstrap
Axios
JavaScript
Backend
Node.js
API REST
JWT
PostgreSQL
Estrutura do Projeto
frontend/
backend/

O frontend é estático e consome a API do backend.

Entidades do Sistema
User

Representa o usuário do sistema.

Atributos:

id
name
email
password_hash
created_at

Regra:

Um usuário pode ter vários posts.
Post

Representa um artigo publicado.

Atributos:

id
title
slug
content (Markdown)
created_at
updated_at
user_id

Regra:

Cada post pertence a um usuário.
Comment (opcional)

Pode ser adicionado futuramente.

Atributos:

id
content
created_at
user_id
post_id
Relações entre as Entidades
User → Post
Um usuário pode ter vários posts.
Relação: 1 para N.
Tipo: associação.
Post → Comment (se implementado)
Um post pode ter vários comentários.
Relação: 1 para N.
Tipo: associação.