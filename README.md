# 🚀 Guia Rápido — Integração Contínua com GitHub Actions

Este projeto demonstra um **pipeline simples de CI (Integração Contínua)** utilizando **GitHub Actions**, que é executado automaticamente sempre que ocorre um **push no repositório**.

O objetivo é mostrar de forma prática **como automatizar tarefas básicas dentro de um workflow**.

---

# 🎯 Objetivo do Exemplo

Este pipeline demonstra:

- ✔ Criar um **workflow de CI**
- ✔ Executar automações após **push no repositório**
- ✔ Rodar **comandos dentro de um job**

---

# 📁 Estrutura do Projeto

O workflow fica localizado no seguinte caminho dentro do repositório:


.github/workflows/ci.yml


---

# ⚙️ Workflow Completo

```yaml
name: CI Example

on: [push]

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - name: Mensagem 1
        run: echo "Iniciando pipeline"

      - name: Mensagem 2
        run: echo "Pipeline finalizado"
🔍 Explicação do Workflow
1️⃣ Nome do Workflow
name: CI Example

Define o nome do pipeline, que aparecerá na aba Actions do repositório.

2️⃣ Evento que dispara o pipeline
on: [push]

Significa que o workflow será executado sempre que ocorrer um push no repositório.

3️⃣ Job do Pipeline
jobs:
  test:

Um job representa um conjunto de tarefas executadas em uma máquina virtual.

Neste exemplo existe apenas um job chamado:

test
4️⃣ Ambiente de Execução
runs-on: ubuntu-latest

Define que o job será executado em uma máquina virtual Ubuntu hospedada pelo GitHub.

5️⃣ Steps (Etapas)

Os steps são os comandos executados dentro do job.

Step 1
- name: Mensagem 1
  run: echo "Iniciando pipeline"

Saída no log:

Iniciando pipeline
Step 2
- name: Mensagem 2
  run: echo "Pipeline finalizado"

Saída no log:

Pipeline finalizado
▶️ Fluxo de Execução

Sempre que um push for realizado:

Push no repositório
        ↓
GitHub detecta o evento
        ↓
Workflow é iniciado
        ↓
Job "test" é executado
        ↓
Step 1 executa
        ↓
Step 2 executa
        ↓
Mensagens aparecem no log
📊 Exemplo de saída no log
Iniciando pipeline
Pipeline finalizado
🛠 Tecnologias utilizadas

GitHub

GitHub Actions

YAML

Ubuntu Runner
