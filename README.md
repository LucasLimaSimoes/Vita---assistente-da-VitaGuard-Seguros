\# ❤️ Chatbot Inteligente para Seguros de Vida com RAG, LLM e Memória Conversacional



\[!\[Python](https://img.shields.io/badge/Python-3.x-blue.svg)]()

\[!\[LLM](https://img.shields.io/badge/LLM-FLAN--T5-green.svg)]()

\[!\[RAG](https://img.shields.io/badge/RAG-FAISS-orange.svg)]()

\[!\[NLP](https://img.shields.io/badge/NLP-Embeddings-purple.svg)]()

\[!\[Chatbot](https://img.shields.io/badge/AI-Virtual%20Assistant-red.svg)]()



Este projeto apresenta o desenvolvimento de um \*\*chatbot inteligente para atendimento em seguros de vida\*\*, utilizando uma arquitetura moderna baseada em:



\- \*\*RAG (Retrieval-Augmented Generation)\*\*

\- \*\*LLM (Large Language Model)\*\*

\- \*\*Embeddings semânticos\*\*

\- \*\*Memória conversacional\*\*

\- \*\*Busca vetorial com FAISS\*\*



O sistema simula uma assistente virtual chamada \*\*Vita\*\*, representante da seguradora fictícia \*\*VitaGuard Seguros\*\*, capaz de responder dúvidas de clientes de forma \*\*natural, contextual e personalizada\*\*.



\---



\# 👥 Autores



\- Lucas Lima Simões

\- Raphael Hilário Alcova Coelho

\- Patricia Tavares Simões

\- Thayná dos Santos Patricio Furtado

\- Willian Mello Antunes



\---



\# 📌 Sumário



\- \[Contexto e Motivação](#-contexto-e-motivação)

\- \[Objetivo](#-objetivo)

\- \[Arquitetura da Solução](#-arquitetura-da-solução)

\- \[Base de Dados](#-base-de-dados)

\- \[Metodologia](#-metodologia)

\- \[Tecnologias Utilizadas](#-tecnologias-utilizadas)

\- \[Funcionalidades Implementadas](#-funcionalidades-implementadas)

\- \[Resultados](#-resultados)

\- \[Diferenciais do Projeto](#-diferenciais-do-projeto)

\- \[Trabalhos Futuros](#-trabalhos-futuros)



\---



\# 🌍 Contexto e Motivação



O setor de seguros depende fortemente de \*\*atendimento ao cliente\*\*, especialmente para dúvidas recorrentes sobre:



\- boletos

\- sinistros

\- cancelamentos

\- documentação

\- coberturas

\- alterações cadastrais



Grande parte dessas demandas é repetitiva e pode ser automatizada.



Neste contexto, chatbots inteligentes surgem como uma alternativa para:



\- reduzir custos operacionais

\- melhorar a experiência do usuário

\- oferecer atendimento 24/7

\- aumentar escalabilidade



\---



\# 🎯 Objetivo



Desenvolver um chatbot capaz de:



\- responder dúvidas sobre seguros de vida

\- utilizar \*\*busca contextual baseada em documentos\*\*

\- manter \*\*memória de conversa\*\*

\- identificar \*\*intenções do usuário\*\*

\- produzir respostas naturais e consistentes



\---



\# 🏗 Arquitetura da Solução



O sistema utiliza uma arquitetura híbrida:



```text

Usuário

&#x20;  ↓

Detecção de intenção (LLM)

&#x20;  ↓

Busca semântica (RAG + FAISS)

&#x20;  ↓

Validação da resposta

&#x20;  ↓

Humanização da resposta

&#x20;  ↓

Memória conversacional

&#x20;  ↓

Resposta final

```



\---



\# 🗂 Base de Dados



Foram utilizados dois tipos principais de dados:



\## 1. FAQ sintético



Dataset gerado artificialmente contendo mais de \*\*2.000 exemplos\*\*, incluindo:



\- pagamento

\- sinistro

\- cancelamento

\- cobertura

\- carência

\- beneficiário

\- documentação

\- atendimento

\- vencimento

\- reajuste

\- plano

\- portabilidade

\- renovação

\- dados cadastrais

\- fraude

\- apólice

\- carteirinha



Cada exemplo possui:



\- pergunta

\- resposta

\- categoria



\---



\## 2. Documentos simulados



Também foram gerados documentos fictícios da seguradora para enriquecer o contexto:



\- contratos de seguro

\- termos e condições

\- regulamentos

\- manuais do cliente

\- procedimentos de sinistro

\- políticas internas

\- FAQ institucional



Todos em formato \*\*PDF\*\*, posteriormente convertidos em texto e fragmentados (\*chunking\*).



\---



\# 🧪 Metodologia



O desenvolvimento foi dividido em etapas.



\## 🔹 Geração dos dados



Criação de base sintética com múltiplas variações linguísticas.



Exemplo:



\- "Como emitir segunda via do boleto?"

\- "Onde encontro meu boleto?"

\- "Como faço para pagar meu seguro?"



\---



\## 🔹 Processamento de documentos



Leitura automática de PDFs usando a biblioteca \*\*PyPDF\*\*.



Depois aplicamos \*\*chunking textual\*\* para dividir documentos longos em partes menores.



\---



\## 🔹 Embeddings



Utilizamos o modelo \*\*all-MiniLM-L6-v2\*\* para transformar textos em vetores semânticos.



\---



\## 🔹 Indexação vetorial



Os embeddings foram indexados usando \*\*FAISS (Facebook AI Similarity Search)\*\*, permitindo busca rápida e eficiente.



\---



\## 🔹 RAG



Quando o usuário faz uma pergunta:



1\. gera-se o embedding da pergunta

2\. busca-se os textos mais semelhantes

3\. seleciona-se o melhor contexto

4\. retorna-se a resposta



\---



\## 🔹 Uso de LLM



Utilizamos o modelo \*\*google/flan-t5-small\*\* para:



\- detecção de intenção

\- interpretação da pergunta

\- apoio à inteligência do chatbot



Importante:



✅ o modelo \*\*não inventa respostas\*\*  

✅ a resposta final vem do \*\*RAG\*\*



\---



\## 🔹 Memória conversacional



O chatbot armazena:



\- pergunta

\- resposta

\- tópicos

\- embedding



Permitindo detectar perguntas como:



> "Já perguntei do boleto?"



e responder corretamente.



\---



\# 🛠 Tecnologias Utilizadas



\- Python

\- Pandas

\- NumPy

\- Sentence Transformers

\- FAISS

\- Transformers (Hugging Face)

\- FLAN-T5

\- PyPDF

\- Google Colab



\---



\# 🤖 Funcionalidades Implementadas



✅ Busca semântica com RAG  

✅ Integração com documentos PDF  

✅ Memória de conversa  

✅ Detecção de intenção  

✅ Respostas humanizadas  

✅ Tratamento de perguntas repetidas  

✅ Multi-tópicos  

✅ Fallback para "não sei responder"  

✅ Interface conversacional via terminal



\---



\# 📈 Resultados



Exemplo de interação:



```text

Você: Como emitir segunda via do boleto?

Vita: Acesse o portal do cliente e clique em '2ª via de boleto'.



Você: O que faço em caso de sinistro?

Vita: Entre em contato pelo telefone 0800 ou utilize o aplicativo.



Você: Já perguntei do boleto?

Vita: Sim 😊 você já perguntou isso. Mas respondendo novamente...

```



Resultados observados:



\- alta consistência nas respostas

\- baixa alucinação

\- boa recuperação documental

\- memória funcionando corretamente



\---



\# 🧠 Diferenciais do Projeto



\### Memória contextual

Não lembra apenas a pergunta — lembra \*\*tópicos\*\*.



\### Arquitetura híbrida

Combina:



\- regras

\- embeddings

\- LLM



\### RAG com documentos reais

Além do FAQ, responde com base em documentos institucionais.



\### Humanização controlada

Respostas naturais sem depender totalmente da LLM.



\---



\# 🚀 Trabalhos Futuros



Possíveis melhorias:



\- interface web com Gradio ou Streamlit

\- autenticação/login

\- histórico persistente em banco de dados

\- feedback do usuário

\- dashboard administrativo

\- integração com APIs reais



\---



\# 💡 Conclusão



O projeto demonstra como técnicas modernas de IA podem ser aplicadas para construir um \*\*assistente virtual robusto e realista\*\*, combinando:



\- NLP

\- RAG

\- LLM

\- memória conversacional



A solução proposta é facilmente adaptável para cenários reais do mercado segurador.

