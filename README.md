# DIO - Trilha .NET - API e Entity Framework

www.dio.me

_Versão por:_ **Thiago de Oliveira Miranda**

## Desafio de projeto

Para este desafio, foi utilizado os conhecimentos adquiridos no módulo de API e Entity Framework, da trilha .NET da DIO.

## Contexto

Construir um sistema gerenciador de tarefas, onde você poderá ser cadastrado uma lista de tarefas que permitir organizar melhor a rotina.

Essa lista de tarefas precisa ter um **CRUD**, ou seja, deverá permitir a você obter os registros, criar, salvar e deletar esses registros.

A sua aplicação implementada foi uma Web API.

Classe principal de tarefa:

![Diagrama da classe Tarefa](diagrama.png)

## Métodos implementados

**Swagger**

![Métodos Swagger](swagger.png)

**Endpoints**

| Verbo  | Endpoint               | Parâmetro | Body          |
| ------ | ---------------------- | --------- | ------------- |
| GET    | /Tarefa/{id}           | id        | N/A           |
| PUT    | /Tarefa/{id}           | id        | Schema Tarefa |
| DELETE | /Tarefa/{id}           | id        | N/A           |
| GET    | /Tarefa/ObterTodos     | N/A       | N/A           |
| GET    | /Tarefa/ObterPorTitulo | titulo    | N/A           |
| GET    | /Tarefa/ObterPorData   | data      | N/A           |
| GET    | /Tarefa/ObterPorStatus | status    | N/A           |
| POST   | /Tarefa                | N/A       | Schema Tarefa |

Esse é o schema (model) de Tarefa, utilizado para passar para os métodos que exigirem.

```json
{
  "id": 0,
  "titulo": "string",
  "descricao": "string",
  "data": "2022-06-08T01:31:07.056Z",
  "status": "Pendente"
}
```
