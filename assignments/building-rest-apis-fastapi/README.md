# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Construa uma API REST para gerenciar tarefas usando FastAPI. Você praticará a criação de rotas, validação de dados e respostas HTTP para operações CRUD.

## 📝 Tasks

### 🛠️ Criar a aplicação e consultar tarefas

#### Descrição
Crie uma aplicação FastAPI para gerenciar tarefas. Cada tarefa deve ter um identificador inteiro, um título, uma descrição e um indicador de conclusão. Mantenha os dados em memória; não é necessário usar um banco de dados.

#### Requisitos
O programa concluído deve:

- Instalar FastAPI e Uvicorn e iniciar a aplicação com `uvicorn main:app --reload`
- Definir um modelo Pydantic para os dados de uma tarefa
- Implementar `GET /tasks` para retornar a lista de tarefas
- Implementar `GET /tasks/{task_id}` para retornar uma tarefa pelo identificador
- Retornar o status HTTP `404` quando o identificador solicitado não existir


### 🛠️ Criar e atualizar tarefas

#### Descrição
Adicione as operações necessárias para criar tarefas e substituir os dados de uma tarefa existente. Use os modelos Pydantic para validar os dados recebidos.

#### Requisitos
O programa concluído deve:

- Implementar `POST /tasks` para criar uma tarefa e retornar o status HTTP `201`
- Gerar um identificador único para cada tarefa criada
- Implementar `PUT /tasks/{task_id}` para substituir os dados de uma tarefa existente
- Retornar o status HTTP `404` ao tentar atualizar uma tarefa inexistente
- Rejeitar dados inválidos, como uma solicitação sem o título obrigatório


### 🛠️ Excluir e testar tarefas pela API

#### Descrição
Finalize as operações CRUD e use a documentação interativa da aplicação para testar os endpoints.

#### Requisitos
O programa concluído deve:

- Implementar `DELETE /tasks/{task_id}` para excluir uma tarefa existente
- Retornar o status HTTP `204` ao excluir uma tarefa e `404` se ela não existir
- Abrir `http://127.0.0.1:8000/docs` e testar a criação, consulta, atualização e exclusão de uma tarefa
- Demonstrar que uma tarefa excluída não aparece mais em `GET /tasks`
