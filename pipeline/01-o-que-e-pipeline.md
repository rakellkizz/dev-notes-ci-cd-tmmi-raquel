# 🛠 O que é um Pipeline?

Um **pipeline** é uma sequência de etapas automatizadas que executam um processo de ponta a ponta.

Ele funciona como uma **linha de produção**:

> Saída de uma etapa → vira entrada da próxima.

---

## 🔹 Definição simples

> “Pipeline é o fluxo automatizado de tarefas que vão desde o código até o resultado final (build, relatório, deploy, etc.).”

Cada etapa do pipeline executa uma parte do trabalho:

1. Baixar o código
2. Configurar ambiente
3. Instalar dependências
4. Rodar testes ou scripts
5. Gerar artefatos ou fazer deploy

---

## 🔹 Exemplo de pipeline típico em CI/CD

Um pipeline comum pode ter:

1. **Checkout** – baixa o código do repositório
2. **Setup** – configura linguagem (Python, Node, etc.)
3. **Install** – instala dependências
4. **Test** – roda testes automatizados
5. **Build** – gera o build ou artefatos
6. **Deploy** – envia para servidor ou nuvem

---

## 🔹 Exemplo com GitHub Actions (na prática)

No projeto `python-log-cleaner-ci`, o pipeline é:

1. `actions/checkout@v4`  
   → baixa o código

2. `actions/setup-python@v5`  
   → configura Python 3.10

3. `pip install -r requirements.txt`  
   → instala `loguru`, `pandas`, `colorama`, etc.

4. `python src/cleaner.py`  
   → executa o script que processa os logs

5. `actions/upload-artifact@v4`  
   → faz upload do `relatorio_final.txt` como artefato

---

## 🎯 Como explicar pipeline em entrevista

> “Pipeline é a automação do fluxo de trabalho. Em vez de alguém rodar comandos manualmente, o pipeline orquestra checkout, instalação, execução de testes, build e deploy, sempre da mesma forma, a cada push ou evento configurado.”
