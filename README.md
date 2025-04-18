# 📋 Task API - Gerenciador de Tarefas com Prioridade

Uma API RESTful para gerenciamento de tarefas com título, descrição, prioridade e status. Desenvolvida com **Java + Spring Boot**, usando **PostgreSQL** como banco de dados e documentada com **Swagger UI**.

---

## 🚀 Funcionalidades

- ✅ Criar tarefas
- 📄 Listar todas as tarefas
- 🔍 Buscar tarefa por ID
- ✏️ Atualizar tarefa
- ❌ Deletar tarefa
- 📚 Documentação interativa com Swagger

---

## 🧰 Tecnologias Utilizadas

- Java 17+
- Spring Boot
- Spring Data JPA
- PostgreSQL
- Swagger (springdoc-openapi)
- Maven

---

## 🗃️ Modelagem da Tarefa (`Task`)

```java
public class Task {
    Long id;
    String title;
    String description;
    Priority priority; // LOW, MEDIUM, HIGH
    Status status;     // PENDING, IN_PROGRESS, DONE
}
```

---

## 💾 Configuração do Banco (PostgreSQL)

1. Acesse o **pgAdmin 4** ou outro client PostgreSQL.
2. Crie um banco com nome: `taskdb`
3. Atualize seu `application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/taskdb
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

## ▶️ Como Rodar o Projeto

### Pré-requisitos:

- Java 17+
- Maven
- PostgreSQL rodando localmente

### Passos:

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/task-api.git
cd task-api

# Rode a aplicação
./mvnw spring-boot:run
```

---

## 🌐 Swagger UI

Após iniciar a aplicação, acesse:

```
http://localhost:8080/swagger-ui.html
```

Você verá uma interface para testar todos os endpoints da API.

---

## 📬 Endpoints Principais

| Método | Rota          | Ação                        |
|--------|---------------|-----------------------------|
| GET    | /tasks        | Listar todas as tarefas     |
| GET    | /tasks/{id}   | Buscar uma tarefa por ID    |
| POST   | /tasks        | Criar uma nova tarefa       |
| PUT    | /tasks/{id}   | Atualizar uma tarefa        |
| DELETE | /tasks/{id}   | Deletar uma tarefa por ID   |

---

## 🧪 Exemplo de JSON para criação de tarefa (POST)

```json
{
  "title": "Estudar Spring",
  "description": "Focar em JPA e Swagger",
  "priority": "HIGH",
  "status": "PENDING"
}
```

---

## 📦 Futuras melhorias

- Integração com autenticação (JWT)
- Integração com front-end React
- Ordenação por prioridade ou status

---

## 🤝 Contribuição

Contribuições são bem-vindas! Abra uma issue ou envie um PR.

---

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.
