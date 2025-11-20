# 🐹 GoLang — O que é e por que é tão utilizado?

Go (ou Golang) é uma linguagem criada pelo Google focada em:

- 🚀 Alta performance  
- 🧵 Concorrência nativa (goroutines)  
- ⚙️ Simplicidade  
- 📦 Deploy fácil (binário único)  
- 🛡️ Confiabilidade e estabilidade

---

## ⭐ Por que as empresas usam Go?

- APIs extremamente rápidas  
- Microserviços escaláveis  
- Sistemas de alta concorrência (NOC, SRE, Telecom, Streaming)  
- Ferramentas internas de alto desempenho  
- Monitoramento, logs e workers assíncronos  

Serviços famosos escritos em Go:

- Docker 🐳  
- Kubernetes ☸️  
- Grafana 📊  
- Terraform 🌍  
- Cloudflare 🚀  
- GitHub CLI  

---

## 🧠 Como eu adquiri experiência na prática (resposta para entrevista)

> “Aprendi Go criando automações simples, servidores HTTP e ferramentas de análise. Comecei com scripts pequenos e evoluí para construção de APIs e microserviços. Também estudei conceitos importantes como goroutines, channels e organização de pacotes.”

---

## 🧩 Exemplo simples (API em Go)

```go
package main

import (
    "fmt"
    "net/http"
)

func main() {
    http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
        fmt.Fprintln(w, "API em Go funcionando! 🚀")
    })

    http.ListenAndServe(":8080", nil)
}
