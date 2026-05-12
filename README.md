Mini Blog com Markdown

Este é um projeto de um mini blog com autenticação e suporte a Markdown.
O objetivo é praticar consumo de API, organização de frontend e estrutura básica de um sistema fullstack.

Funcionalidades
Cadastro de usuário
Login com autenticação via token
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

Entidades
User
id
name
email
password_hash
created_at

Um usuário pode ter vários posts.

Post
id
title
slug
content
created_at
updated_at
user_id

Cada post pertence a um usuário.