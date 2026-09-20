<div align="center">

# Hi, I'm Mohan 👋

### I build AI systems — and decide what ships.

**Technical Product Manager & AI Engineer** at [FutureSmart AI](https://futuresmart.ai)

Production RAG · AI agents · NL2SQL · Document intelligence

[![Portfolio](https://img.shields.io/badge/Portfolio-mohanvishe.vercel.app-111111?style=for-the-badge&logo=vercel&logoColor=white)](https://mohanvishe.vercel.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mohanvishe)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mohanvishe.plus@gmail.com)
[![Agent Platform](https://img.shields.io/badge/Live-agent.futuresmart.ai-6E56CF?style=for-the-badge)](https://agent.futuresmart.ai/)

</div>

---

## 🧭 What I actually do

Most people in AI are either the engineer or the one deciding what to build. I'm both — which is why my title reads Technical Product Manager while the work is AI engineering.

```
Discovery  →  what's worth building, and what isn't
Design     →  RAG or agent? which model at which step? cost / latency / accuracy?
Build      →  Python · FastAPI · LangChain · LangGraph · vector DBs · MCP
Evaluate   →  benchmark before choosing; gate releases on measured quality, not vibes
Ship       →  AWS, Docker, microservices — then watch whether anyone actually adopts it
```

**The habit that defines my work: I measure before I choose.** A model swap has to prove itself on accuracy against a fixed benchmark before cost enters the conversation. That instinct is public in [nl2sql-reliability](https://github.com/MohanVishe/nl2sql-reliability) and [pdf-parser-benchmark](https://github.com/MohanVishe/pdf-parser-benchmark), and private in the evaluation harness behind the products below.

---

## 🚀 Shipped at work

> Built with a team at FutureSmart AI. These are live products, not repos — the code belongs to the company, so what I can show you is the product and the thinking behind it.

| Product | What it does | My part |
|---|---|---|
| 🤖 **[Agent Platform](https://agent.futuresmart.ai/)** | Platform for building and running AI agents | Engineering across a 14-microservice system; observability and agent health |
| 🗄️ **Database Agent (NL2SQL)** | Ask in English, get the answer from your database | Product owner **and** builder — prototype to public launch |
| 📄 **Document Intelligence** | Pull structured data out of messy documents, then chat with it | Product owner — positioning, scope, release |
| 📊 **[AI Demos](https://aidemos.com/)** | Public AI evaluation and demo platform | Model benchmarking and comparison |
| 📝 **Meeting Notes System** | Transcription → structured notes → ten downstream workflows, one over MCP | Owner and code contributor |

---

## 🔬 Public projects

### 🧪 [NL2SQL Reliability Study](https://github.com/MohanVishe/nl2sql-reliability)

**Ask an AI the same database question ten times — do you get the same right answer?** 14,940 scored generations say no.

Every published text-to-SQL score comes from asking each question once. This asks ten times and reports both `pass@10` (right at least once — capability) and `pass^10` (right every time — reliability). The gap is **13.7 points**, and **41% of attempts ran without error and returned the wrong rows** — silent failures outnumber crashes more than 2 to 1. An agentic retry loop raised both scores and left the gap unchanged; a smaller model nearly doubled it.

Expert-corrected benchmark, no LLM-as-judge, every raw attempt published so any reader can recompute the numbers. 251 tests in CI. Run locally at zero cost.

`Python` · `Ollama` · `Qwen2.5-Coder` · `SQLite` · `pytest` · `GitHub Actions`

📄 [Full write-up](https://mohanvishe.vercel.app/projects/nl2sql-reliability)

---

<table>
<tr>
<td width="50%" valign="top">

### 🩺 [Medical RAG Chatbot](https://github.com/MohanVishe/medical-rag-chatbot)

Medical Q&A grounded in a PDF corpus.

**The interesting part isn't retrieval — it's refusal.** Getting it to say *"my sources don't cover that"* instead of confidently improvising is the half most RAG demos skip.

`Llama 3` · `LangChain` · `Pinecone` · `Flask`

</td>
<td width="50%" valign="top">

### 📑 [PDF Parser Benchmark](https://github.com/MohanVishe/pdf-parser-benchmark)

Local parsers vs cloud services, on documents that actually break them.

PyPDF, PDFPlumber and PDFMiner against LlamaParse and AWS Textract — one harness, same input, side-by-side output.

`NLP` · `LlamaParse` · `AWS Textract` · `Python`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🎯 [HabitLoop](https://github.com/MohanVishe/ai-habit-tracker)

A habit tracker whose AI coach can only tell you what your own log actually says.

Statistics are computed in Python and **tested**; the model interprets them and never does arithmetic. Runs on open weights.

`LangChain` · `Llama 3` · `Streamlit` · `SQLite`

</td>
<td width="50%" valign="top">

### 🔍 [Product Similarity API](https://github.com/MohanVishe/product-similarity-api)

Embedding-based similarity search served over HTTP — find the closest products to any query, then filter by price and rating.

`FastAPI` · `Chroma` · `Embeddings`

</td>
</tr>
</table>

Plus **[Rossmann Sales Forecasting](https://github.com/MohanVishe/rossmann-sales-forecasting)** — daily sales across 1,115 stores, where tree models took test R² from 0.836 to 0.965. Kept because the fundamentals still matter.

---

## 🛠️ Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![Anthropic](https://img.shields.io/badge/Anthropic-D97757?style=flat-square&logo=anthropic&logoColor=white)
![Llama 3](https://img.shields.io/badge/Llama_3-0467DF?style=flat-square&logo=meta&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=flat-square)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)

| | |
|---|---|
| 🧠 **AI & LLM** | LLMs · Generative AI · RAG · Agentic AI · Multi-agent systems · Tool calling · MCP · Prompt engineering · Structured outputs · Guardrails · Hallucination reduction · Embeddings · Vector databases · NL2SQL · Chatbots |
| 📏 **Evaluation & quality** | LLM evaluation · Model evaluation · Observability · LangSmith tracing · Metrics · Cost & latency optimisation · Experimentation |
| ⚙️ **Backend & cloud** | Python · FastAPI · REST APIs · SQL · PostgreSQL · System design · Scalability · Integrations · Data pipelines · Workflow automation · AWS · Docker · Git · CI/CD · Model deployment |
| 📊 **ML & data** | Machine learning · Data science · Regression · SQL analytics · Analytics |
| 🧭 **Product** | Product management · Roadmaps · PRDs · Acceptance criteria · Prototyping · Wireframing · Agile · Cross-functional delivery · Stakeholder management |

---

## 💬 Currently

🔭 Building production GenAI at FutureSmart AI

🌱 Going deeper on agent evaluation — measuring agent quality, not just model quality

👀 Open to **AI Engineer** and **Technical Product Manager** roles

📫 **mohanvishe.plus@gmail.com** · [LinkedIn](https://www.linkedin.com/in/mohanvishe) · [mohanvishe.vercel.app](https://mohanvishe.vercel.app/)

<div align="center">
<br>

*I'd rather ship one system people use than prototype five that nobody does.*

</div>
