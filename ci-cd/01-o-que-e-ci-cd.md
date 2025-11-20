# 🧪 O que é CI/CD?

CI/CD significa:

- **CI → Continuous Integration (Integração Contínua)**
- **CD → Continuous Delivery / Continuous Deployment (Entrega Contínua / Deploy Contínuo)**

---

## 🔹 CI – Continuous Integration (Integração Contínua)

É o processo de **integrar código frequentemente** (várias vezes ao dia) em um repositório compartilhado (GitHub, GitLab, etc.) com:

- testes automatizados
- validações de build
- verificação de qualidade

A ideia é:

> “Cada vez que alguém faz um commit/push, o código é automaticamente testado para garantir que não quebrou nada.”

### Exemplos do que a CI faz:
- Roda testes automatizados
- Checa se o projeto builda
- Roda lint (análise estática de código)
- Gera artefatos (relatórios, binários, etc.)

---

## 🔹 CD – Continuous Delivery / Deployment

Depois da integração contínua, vem a **entrega contínua**:

- **Continuous Delivery**: o sistema está sempre pronto para ser implantado (deploy), mas alguém ainda decide *quando* fazer o deploy.
- **Continuous Deployment**: o deploy acontece automaticamente em produção sempre que a pipeline termina com sucesso.

### Exemplos:
- Subir uma nova versão de um site automaticamente
- Atualizar uma API depois de cada merge na branch `main`
- Publicar pacotes ou imagens Docker sem intervenção manual

---

## 🎯 Resumo simples para entrevista

> **“CI/CD é um conjunto de práticas e automações que garantem que cada mudança de código seja integrada, testada e entregue de forma rápida, segura e padronizada.”**

---

## 🧪 No meu projeto `python-log-cleaner-ci`

- Usei **GitHub Actions** como ferramenta de CI/CD.
- A pipeline:
  - instala dependências
  - executa um script Python para processar logs
  - gera um relatório automático
  - salva o relatório como artefato

Isso mostra na prática:

- Integração Contínua (código é validado a cada push)
- Entrega Contínua (relatório é gerado automaticamente)
