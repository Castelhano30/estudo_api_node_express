# CRUD de Usuários com Node.js, Express e Prisma

Este projeto consiste na criação de um CRUD (Create, Read, Update e Delete) de usuários utilizando Node.js, Express e Prisma. Cada usuário possui os seguintes atributos:

* **Name**: Nome completo do usuário.
* **Age**: Idade do usuário.
* **Email**: E-mail único do usuário.

## Tecnologias Utilizadas

* **Node.js**
* **Express**
* **Prisma**


## Modelo Prisma

```prisma
model User {
  id    String  @id @default(uuid())
  name  String
  age   Int
  email String  @unique
}
```

## Endpoints

| Método   | Rota         | Descrição                |
| -------- | ------------ | ------------------------ |
| `GET`    | `/users`     | Listar todos os usuários |
| `POST`   | `/users`     | Criar um novo usuário    |
| `GET`    | `/users/:id` | Buscar usuário por ID    |
| `PUT`    | `/users/:id` | Atualizar usuário por ID |
| `DELETE` | `/users/:id` | Excluir usuário por ID   |

## Como Executar

### 1. Instale as dependências:

```bash
npm install
```

### 2. Configure o banco com Prisma:

```bash
npx prisma migrate dev
```

### 3. Execute o servidor:

```bash
npm run dev
```

Agora seu servidor estará disponível em `http://localhost:3000`.

---

**Desenvolvido por Felipe Castelhano**
