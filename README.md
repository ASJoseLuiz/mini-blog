# Mini Blog com Markdown

Projeto de um mini blog com autenticação e suporte a Markdown. O objetivo é praticar consumo de API, organização de frontend e estrutura básica de um sistema fullstack.

## Funcionalidades

- Cadastro de usuário
- Login com autenticação via token (JWT)
- Criar posts em Markdown
- Listar posts
- Visualizar post individual
- Editar e excluir posts (apenas do autor)

## Tecnologias

**Frontend:** HTML, Bootstrap, Axios, JavaScript

**Backend:** Node.js, API REST, JWT, PostgreSQL

## Estrutura do Projeto

```
/
├── frontend/
└── backend/
```

O frontend é estático e consome a API do backend.

## Entidades do Sistema

### User

Representa o usuário do sistema.

- `id`
- `name`
- `email`
- `password_hash`
- `created_at`

> Um usuário pode ter vários posts.

### Post

Representa um artigo publicado.

- `id`
- `title`
- `slug`
- `content` (Markdown)
- `created_at`
- `updated_at`
- `user_id`

> Cada post pertence a um usuário.

### Comment *(opcional)*

Pode ser adicionado futuramente.

- `id`
- `content`
- `created_at`
- `user_id`
- `post_id`

## Relações entre Entidades

- **User → Post:** um usuário pode ter vários posts (1 para N)
- **Post → Comment:** um post pode ter vários comentários (1 para N)