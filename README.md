# 🤖 Agente de IA para Docentes federais (Caso de uso da UFRA) via WhatsApp (n8n + Supabase + RAG)

Este projeto implementa um **Agente de IA** que responde a professores via **WhatsApp**, utilizando **RAG (Retrieval-Augmented Generation)** sobre documentos institucionais (resoluções, regimentos, anexos).  
A solução foi desenvolvida com **n8n** para orquestração de fluxos, **Supabase + pgvector** como banco vetorial e **OpenAI** para embeddings e geração de respostas.  

---

## ✨ Funcionalidades
- 📚 **RAG**: busca em resoluções e regimentos armazenados em banco vetorial (Supabase).  
- 📲 **WhatsApp**: interação direta com professores via integração Evolution API.  
- 🔎 **Busca semântica**: consultas são respondidas com base em similaridade vetorial.  
- ⚙️ **n8n**: responsável por coordenar a ingestão de dados, embeddings e fluxo de conversas.  
- 🗂 **Suporte a anexos e tabelas**: conteúdo é transformado em chunks para melhor contexto.  

---

## 🛠️ Tecnologias Utilizadas
- [n8n](https://n8n.io/) – automação e orquestração do agente  
- [Supabase](https://supabase.com/) – banco de dados + pgvector  
- [pgvector](https://github.com/pgvector/pgvector) – busca vetorial  
- [OpenAI Embeddings](https://platform.openai.com/docs/guides/embeddings) – geração de embeddings semânticos  
- [WAHA](https://waha.dev/)  – integração com WhatsApp  

---

## 📂 Estrutura do Repositório
 - instrucoes.md # Setup do Supabase e configuração de tabelas
 -  workflow.png # Print do fluxo no n8n
- workflows: agente-n8n.json # Export do workflow do n8n
- README.md

---

##  Como Reproduzir
1. **Clone este repositório**
   ```bash
   git clone https://github.com/seu-usuario/agente-ia-rag-n8n.git
   cd agente-ia-rag-n8n
Configure o Supabase

Crie a tabela vetorial resolucoes_vec e a função match_resolucoes (scripts em /docs/instrucoes.md).

Habilite a extensão pgvector.

Importe o Workflow no n8n

No painel do n8n, importe o arquivo agente-n8n.json.

Configure as credenciais do Supabase, OpenAI e WhatsApp API.

Execute o Agente

Envie perguntas via WhatsApp e receba respostas contextualizadas usando RAG.

 Próximos Passos

Melhorar o parsing de anexos em tabelas (estrutura colunar em JSON).

Adicionar interface web para consulta além do WhatsApp.

Publicar artigo detalhando a arquitetura e uso em contexto educacional.

📜 Licença

Este projeto é disponibilizado sob a licença MIT.
Sinta-se livre para usar, modificar e compartilhar.

👨‍🏫 Autor

Desenvolvido por Carlos Jean Quadros – Professor Universitário e Pesquisador em Computação Aplicada.


---
