# 🧪 API Automation Tests — Cypress + JavaScript

> Desafio de Projeto DIO | Automação de Testes de API  
> Autora: **Idna Reis** | [LinkedIn](https://linkedin.com/in/idna-reis) · [GitHub](https://github.com/IdnaReis)

---

## 📌 Sobre o Projeto

Este projeto é uma versão melhorada do desafio de automação de testes de API da [Digital Innovation One (DIO)](https://dio.me), originalmente desenvolvido com **Java + REST Assured** pela Expert Carolina.

Nesta versão, utilizei **Cypress + JavaScript**, trazendo uma abordagem moderna, mais simples de configurar e amplamente adotada no mercado de QA.

A API testada é a [JSONPlaceholder](https://jsonplaceholder.typicode.com) — uma API REST pública gratuita usada para prototipação e testes.

---

## 🚀 Tecnologias Utilizadas

| Tecnologia | Versão | Finalidade |
|---|---|---|
| [Cypress](https://cypress.io) | 13.x | Framework de testes |
| JavaScript | ES6+ | Linguagem principal |
| Node.js | 18+ | Ambiente de execução |
| JSONPlaceholder | — | API de testes |

---

## 📁 Estrutura do Projeto

```
idna-api-tests-cypress/
├── cypress/
│   ├── e2e/
│   │   ├── posts.cy.js       # Testes do endpoint /posts
│   │   ├── users.cy.js       # Testes do endpoint /users
│   │   └── comments.cy.js    # Testes do endpoint /comments
│   └── support/
│       └── e2e.js            # Comandos customizados globais
├── cypress.config.js         # Configuração do Cypress
├── package.json
└── README.md
```

---

## ✅ Cobertura de Testes

### 📋 Posts (`/posts`)
- [x] GET — Listar todos os posts (200, array com 100 itens)
- [x] GET — Buscar post por ID (200, estrutura correta)
- [x] GET — Buscar post inexistente (404)
- [x] GET — Filtrar posts por userId
- [x] POST — Criar novo post (201, dados retornados)
- [x] PUT — Atualizar post completo (200)
- [x] PATCH — Atualizar post parcialmente (200)
- [x] DELETE — Excluir post (200, body vazio)

### 👤 Users (`/users`)
- [x] GET — Listar todos os usuários (200, array com 10 itens)
- [x] GET — Buscar usuário por ID (200, dados corretos)
- [x] GET — Buscar usuário inexistente (404)
- [x] GET — Validar email de todos os usuários
- [x] GET — Posts de um usuário (`/users/:id/posts`)
- [x] GET — Todos de um usuário (`/users/:id/todos`)
- [x] POST — Criar novo usuário (201)

### 💬 Comments (`/comments`)
- [x] GET — Listar todos os comentários (200, array com 500 itens)
- [x] GET — Buscar comentário por ID (200)
- [x] GET — Buscar comentário inexistente (404)
- [x] GET — Filtrar por postId (`/comments?postId=1`)
- [x] GET — Rota aninhada (`/posts/:id/comments`)
- [x] GET — Validar equivalência entre rotas de filtro
- [x] POST — Criar novo comentário (201)
- [x] DELETE — Excluir comentário (200, body vazio)

---

## 🔧 Como Executar

### Pré-requisitos
- Node.js 18+
- npm

### Instalação

```bash
# Clone o repositório
git clone https://github.com/IdnaReis/idna-api-tests-cypress.git

# Acesse a pasta
cd idna-api-tests-cypress

# Instale as dependências
npm install
```

### Executar os testes

```bash
# Modo headless (terminal) — todos os testes
npm test

# Modo interativo (interface visual do Cypress)
npm run test:open
```

---

## 📊 Diferencial desta versão

| Recurso | REST Assured (original) | Cypress (esta versão) |
|---|---|---|
| Linguagem | Java | JavaScript |
| Setup | Maven + pom.xml | npm (simples) |
| Comandos customizados | — | ✅ validatePostStructure, validateUserStructure, validateCommentStructure |
| Cobertura | Básica | Extendida (todos, filtros, rotas aninhadas) |
| Legibilidade | Intermediária | Alta |

---

## 🧠 Aprendizados

- Estrutura de testes de API com Cypress
- Validação de status codes, headers e body
- Criação de comandos customizados (`Cypress.Commands.add`)
- Testes de rotas aninhadas e parâmetros de query
- Cobertura de cenários positivos e negativos (happy path + error path)

---

## 🔗 Referências

- [Repositório original — DIO + REST Assured](https://github.com/digitalinnovationone/api-automation-tests-challenge-rest-assured)
- [JSONPlaceholder — API de testes](https://jsonplaceholder.typicode.com)
- [Documentação Cypress](https://docs.cypress.io)

---

> *"QA não é apenas encontrar bugs. É construir produtos melhores desde o início."*  
> — Idna Reis
