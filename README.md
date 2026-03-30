# ci-demo

## Descrição do projeto
Um pipeline simples de **Continuous Integration (CI)** utilizando **GitHub Actions**, configurado para executar automaticamente a cada `push` no repositório e exibir mensagens no log da execução.

## Objetivo da atividade
O objetivo do pipeline criado é demonstrar o funcionamento básico de uma esteira de CI no GitHub Actions, validando que o workflow:
- é disparado corretamente a cada `push`;
- executa um job em um runner Linux (`ubuntu-latest`);
- roda etapas (steps) que exibem mensagens no console (logs), simulando o início e o fim de um processo de integração.

## Estrutura do projeto
Arquivos e pastas presentes no repositório:

- `.github/workflows/ci.yml`
- `README.md`

## Explicação do workflow (`.github/workflows/ci.yml`)
Abaixo está a explicação das partes do arquivo:

- **`name: CI Test`**
  - Define o nome do workflow que aparecerá na aba **Actions** do GitHub.

- **`on: [push]`**
  - Define o evento que dispara o workflow.
  - Neste caso, o pipeline executa **sempre que houver um push** para o repositório.

- **`jobs:`**
  - Seção que agrupa os jobs (tarefas) do workflow.

- **`test:`**
  - Nome do job (identificador). Aqui ele foi chamado de `test`.

- **`runs-on: ubuntu-latest`**
  - Define o ambiente (runner) onde o job será executado.
  - `ubuntu-latest` significa que ele rodará em uma máquina virtual Linux fornecida pelo GitHub.

- **`steps:`**
  - Lista de etapas executadas em sequência dentro do job.

- **Step 1**
  - **`- name: Mensagem 1`**: nome descritivo da etapa.
  - **`run: echo "Iniciando pipeline"`**: comando executado no shell, imprimindo a mensagem nos logs.

- **Step 2**
  - **`- name: Mensagem 2`**: nome descritivo da etapa.
  - **`run: echo "Pipeline finalizado"`**: imprime a mensagem final nos logs.

## Fluxo do pipeline
Fluxo de execução do pipeline:

Push no GitHub  
↓  
Disparo do GitHub Actions (workflow `CI Test`)  
↓  
Execução do job `test` no runner `ubuntu-latest`  
↓  
Execução das etapas (steps) com comandos `echo`  
↓  
Exibição das mensagens no log da execução  

## Resultado da execução
Quando o pipeline é executado (após um `push`):
- o GitHub Actions inicia uma execução do workflow **CI Test**;
- o job `test` roda em um runner Linux;
- no log da execução aparecem as mensagens:
  - `Iniciando pipeline`
  - `Pipeline finalizado`

