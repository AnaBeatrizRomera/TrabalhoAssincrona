# 📌 Trabalho Assíncrona – Sistema de Avaliação de Filmes

Este projeto foi desenvolvido em **Node.js**, utilizando **Express**, **Sequelize** e **Handlebars**.
Ele implementa um **CRUD de usuários e endereços**.

---

## 🚀 Tecnologias Utilizadas

* [Node.js](https://nodejs.org/)
* [Express](https://expressjs.com/)
* [Sequelize](https://sequelize.org/)
* [MySQL2](https://www.npmjs.com/package/mysql2)
* [Handlebars](https://handlebarsjs.com/)

---

## ⚙️ Pré-requisitos

Antes de rodar o projeto, você precisa ter instalado:

* [Node.js](https://nodejs.org/) (versão 18 ou superior recomendada)
* [MySQL](https://www.mysql.com/)

---

## 📂 Estrutura de Pastas

```
TrabalhoAssincrona/
│── db/              # Configuração de conexão com banco
│── models/          # Modelos Sequelize (User, Address)
│── views/           # Templates Handlebars
│── public/          # Arquivos estáticos (CSS, JS)
│── index.js         # Arquivo principal da aplicação
│── package.json     # Dependências do projeto
│── .env             # Variáveis de ambiente
│── .gitignore       # Arquivos ignorados pelo git
```

---

## ▶️ Como rodar o projeto

### 1. Clonar o repositório

```bash
git clone <url-do-repo>
cd TrabalhoAssincrona
```

### 2. Instalar dependências

```bash
npm install
```

### 3. Configurar variáveis de ambiente

Crie um arquivo **`.env`** na raiz do projeto com:

```env
DB_HOST=localhost
DB_USER=seu_usuario
DB_PASSWORD=sua_senha
DB_NAME=trabalho_assincrona
```

### 4. Criar o banco de dados

No MySQL, crie o banco:

```sql
CREATE DATABASE trabalho_assincrona;
```

O Sequelize irá sincronizar as tabelas automaticamente.

### 5. Rodar o servidor

```bash
npm run dev
```

O servidor estará disponível em:
👉 [http://localhost:3000](http://localhost:3000)

---

## 🔑 Funcionalidades

### Usuários

* **Cadastrar novo usuário** (com nome, ocupação e newsletter)
* **Listar usuários** (na página inicial `/`)
* **Editar usuário** (rota `/users/edit/:id`)
* **Excluir usuário** (rota `/users/delete/:id`)
* **Visualizar detalhes do usuário** (inclui endereços)

### Endereços

* Associados a usuários (1:N)
* Criar e excluir endereços pelo formulário na página de edição de usuário

---

## 💡 Exemplos de Uso

* **Página inicial (`/`)** → lista todos os usuários cadastrados.
* **Cadastro (`/users/create`)** → formulário com nome, ocupação e newsletter.
* **Edição (`/users/edit/:id`)** → altera dados do usuário e gerencia endereços.
* **Detalhes (`/users/:id`)** → exibe informações de um usuário específico.

---
