# 01 · Git, GitHub e trabalho colaborativo

Desafio: desenvolver uma API REST simples aplicando Git Flow (`master`, `develop`, `feature`, `hotfix`) e colaborar com outro participante por meio de Pull Requests, com revisão de código e resolução de conflitos.

## Contribuição em outro repositório

- **Projeto:** API de Tarefas (Node.js + Express)
- **Pull Request:** [#1 · Filtro de tarefas por status](https://github.com/alrocha2-stefanini/api-tarefas/pull/1)
- **O que foi feito:** filtro `GET /tarefas?concluida=true|false`, com validação de entrada (retorna 400 para valores inválidos), 4 testes automatizados e atualização do README.
- **Fluxo:** branch `feature/filtro-concluidas` criada a partir da `develop`, 4 commits no padrão Conventional Commits e resolução de conflito no README após atualização da `develop`.

## Minha API

- **Projeto:** _em andamento_
