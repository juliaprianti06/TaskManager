# Task Manager API

API REST simples para gerenciamento de tarefas, desenvolvida com **C# e ASP.NET Core**. O projeto permite realizar operações CRUD e utiliza **Entity Framework Core** para persistência dos dados em um banco SQLite.

O projeto foi desenvolvido com o objetivo de praticar os principais conceitos do ecossistema .NET e o desenvolvimento de APIs REST.

## 🚀 Tecnologias

- C#
- .NET
- ASP.NET Core
- Entity Framework Core
- SQLite

## 📌 Funcionalidades

- Criar uma nova tarefa
- Listar todas as tarefas
- Buscar uma tarefa por ID
- Atualizar uma tarefa
- Excluir uma tarefa
- Persistir os dados utilizando SQLite

## 📂 Estrutura

```text
TaskManager/
├── Data/
│   └── AppDbContext.cs
├── Migrations/
├── Models/
│   └── TaskItem.cs
├── Program.cs
└── TaskManager.csproj
```

## 🔗 Endpoints

| Método | Endpoint | Descrição |
|---|---|---|
| `POST` | `/tasks` | Cria uma nova tarefa |
| `GET` | `/tasks` | Lista todas as tarefas |
| `GET` | `/tasks/{id}` | Busca uma tarefa pelo ID |
| `PUT` | `/tasks/{id}` | Atualiza uma tarefa |
| `DELETE` | `/tasks/{id}` | Exclui uma tarefa |

## 📋 Modelo de tarefa

```json
{
  "title": "Estudar C#",
  "description": "Praticar desenvolvimento de APIs com .NET",
  "completed": false
}
```

Uma tarefa armazenada possui a seguinte estrutura:

```json
{
  "id": 1,
  "title": "Estudar C#",
  "description": "Praticar desenvolvimento de APIs com .NET",
  "completed": false,
  "createdAt": "2026-10-01T12:00:00Z"
}
```

## ▶️ Como executar

### Pré-requisitos

É necessário ter instalado:

- .NET SDK

Clone o repositório:

```bash
git clone <URL-DO-REPOSITORIO>
```

Acesse a pasta do projeto:

```bash
cd TaskManager
```

Restaure as dependências:

```bash
dotnet restore
```

Aplique as migrations:

```bash
dotnet ef database update
```

Execute a aplicação:

```bash
dotnet run
```

A API estará disponível no endereço informado no terminal.

## 💾 Banco de dados

O projeto utiliza **SQLite** para armazenamento dos dados e **Entity Framework Core** como ORM.

As alterações na estrutura do banco são controladas por migrations do Entity Framework Core.

## 🎯 Objetivo

Este projeto foi desenvolvido como prática introdutória de desenvolvimento backend com **C# e .NET**, abordando conceitos como:

- APIs REST
- CRUD
- Programação assíncrona com `async/await`
- Entity Framework Core
- Migrations
- Persistência de dados
- SQLite
