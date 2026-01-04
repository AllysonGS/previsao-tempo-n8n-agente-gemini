# 🌤️ Previsão do Tempo - Chatbot com N8N + Agente Gemini (Memória + Busca Contextual)

Este repositório contém dois workflows do **n8n** que trabalham juntos para criar um chatbot inteligente capaz de responder sobre a previsão do tempo, mantendo uma memória simples de interações anteriores e consultando fontes externas (como Wikipedia) quando falta contexto.

O projeto demonstra como combinar **automação + IA + integração de dados** em uma arquitetura modular.

---

## 📌 Componentes do Projeto

### 🟢 1. Workflow - Previsão do Tempo
Responsável por:
- Receber o nome de uma cidade
- Consultar uma API de clima
- Processar e estruturar a resposta
- Retornar temperatura, condições e detalhes relevantes

Pode ser acionado:
- Manualmente no n8n
- Via HTTP / API
- Pelo agente conversacional

---

### 🤖 2. Agente - Chatbot Gemini (com Memória Simples)

Funciona como um **agente inteligente com comportamento contextual**:

1. Tenta responder usando a memória recente do usuário
2. Se faltar informação → consulta fontes externas (ex: Wikipedia)
3. Se a pergunta for sobre clima → aciona o workflow de previsão do tempo
4. Gera uma resposta final, natural e explicada

---

## 🧠 Fluxo de Raciocínio do Agente

```
Usuário pergunta → Agente Gemini
→ Verifica memória recente
→ Precisa de contexto? → Busca na Wikipedia
→ É sobre clima? → Chama Workflow de Previsão do Tempo
→ n8n processa resultado
→ Resposta final contextualizada
```

---

## ⚙️ Como Importar os Workflows no n8n

1. Abra o painel do **n8n**
2. Clique em **Import**
3. Selecione um dos arquivos `.json`
4. Repita para o segundo workflow
5. Configure:
   - API do modelo Gemini / LLM
   - API de clima (OpenWeather)
6. Salve e execute

---

## 🛠️ Tecnologias Utilizadas

- n8n - Orquestração de automações
- Gemini / LLM - Inteligência conversacional
- API de clima
- Wikipedia como fallback informacional
- JSON workflows exportáveis

---

## 🤝 Contribuindo

Sugestões e PRs são bem-vindos.  
Sinta-se à vontade para abrir uma issue e colaborar no projeto.

---

### ✨ Autor

Projeto desenvolvido por **Allyson Garcia**


