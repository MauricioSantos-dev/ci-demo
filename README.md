# ci-demo

Repositório de demonstração de **CI (Integração Contínua)** usando **GitHub Actions**.

## O que este projeto faz?

Este projeto contém um workflow simples que roda automaticamente a cada **push** no repositório, executando passos de exemplo no runner do GitHub.

## Workflow de CI

- Arquivo: `.github/workflows/ci.yml`
- Nome do workflow: `CI Test`
- Gatilho: `on: [push]` (executa em todo push)
- Ambiente: `ubuntu-latest`
- Passos atuais:
  - Exibe a mensagem: `Iniciando pipeline`
  - Exibe a mensagem: `Pipeline finalizado`

## Como usar / testar

1. Faça qualquer alteração no repositório (ex.: edite este README).
2. Faça commit e dê push para o GitHub.
3. Vá na aba **Actions** do repositório para acompanhar a execução do workflow.

## Estrutura do repositório

- `.github/workflows/ci.yml` — pipeline de CI (exemplo)
- `README.md` — documentação do projeto

## Objetivo

Servir como base para evoluir o pipeline, por exemplo:
- adicionar lint/testes reais
- rodar build
- validar formatação
- criar jobs separados (test/build/deploy)

---

