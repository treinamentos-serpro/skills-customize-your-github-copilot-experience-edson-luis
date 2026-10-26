# 📘 Assignment: Persistência com SQLite e FastAPI

## 🎯 Objective

Adicione persistência a uma API de tarefas criada com FastAPI usando o SQLite da biblioteca padrão do Python. Ao concluir, os dados continuarão disponíveis depois que a aplicação for reiniciada.

## 📝 Tasks

### 🛠️ Criar o banco de dados e a tabela

#### Descrição
Crie a estrutura SQLite que armazenará as tarefas da API. A tabela deve ser criada automaticamente quando a aplicação iniciar e não deve apagar os dados existentes.

#### Requisitos
O programa concluído deve:

- Usar o módulo `sqlite3`, que já faz parte da biblioteca padrão do Python
- Criar um arquivo de banco de dados chamado `tasks.db`
- Criar a tabela `tasks` com as colunas `id`, `title`, `description` e `completed`
- Definir `id` como chave primária inteira e `title` como obrigatório
- Usar `CREATE TABLE IF NOT EXISTS` para preservar a tabela e os dados ao reiniciar a aplicação

### 🛠️ Consultar e criar tarefas persistentes

#### Descrição
Conecte as rotas de consulta e criação ao banco de dados, substituindo o armazenamento em memória usado na assignment anterior.

#### Requisitos
O programa concluído deve:

- Implementar `GET /tasks` para consultar as tarefas salvas
- Implementar `GET /tasks/{task_id}` para consultar uma tarefa pelo identificador
- Implementar `POST /tasks` para salvar uma tarefa e retornar o status HTTP `201`
- Gerar um identificador único para cada tarefa criada
- Usar consultas SQL parametrizadas para inserir e consultar dados
- Retornar o status HTTP `404` quando uma tarefa solicitada não existir

### 🛠️ Atualizar, excluir e verificar a persistência

#### Descrição
Finalize o CRUD usando o SQLite e teste os endpoints pela documentação interativa do FastAPI. Confirme que a API mantém as tarefas mesmo depois de ser reiniciada.

#### Requisitos
O programa concluído deve:

- Implementar `PUT /tasks/{task_id}` para atualizar uma tarefa existente
- Implementar `DELETE /tasks/{task_id}` para excluir uma tarefa existente
- Retornar o status HTTP `404` quando a tarefa a atualizar ou excluir não existir
- Retornar o status HTTP `204` ao excluir uma tarefa existente
- Usar consultas SQL parametrizadas e confirmar as alterações no banco de dados
- Testar as operações em `http://127.0.0.1:8000/docs`
- Criar uma tarefa, reiniciar a aplicação e confirmar que ela continua disponível em `GET /tasks`
