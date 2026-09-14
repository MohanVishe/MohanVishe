<div align="center">

# Hi, I'm Mohan 👋

### I build AI systems — and decide what ships.

**Technical Product Manager & AI Engineer** at [FutureSmart AI](https://futuresmart.ai)

Production RAG · AI agents · NL2SQL · Document intelligence

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

**The habit that defines my work: I measure before I choose.** A model swap has to prove itself on accuracy against a fixed benchmark before cost enters the conversation. That instinct is public in [pdf-parser-benchmark](https://github.com/MohanVishe/pdf-parser-benchmark), and private in the evaluation harness behind the products below.

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
![Meta Llama](https://img.shields.io/badge/Llama_3-0467DF?style=flat-square&logo=meta&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=flat-square)
![Chroma](https://img.shields.io/badge/Chroma-FF6B6B?style=flat-square)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

<table>
<tr><td width="50%" valign="top">

**🧠 AI & LLM engineering**

RAG · Agentic AI · Agent orchestration · Multi-agent workflows · Tool calling · MCP · Prompt engineering · Context engineering · Chunking strategies · Structured outputs & validation · Grounding controls · Safety guardrails · Hallucination reduction · Multi-step reasoning · NL2SQL / Text2SQL · Document intelligence · Semantic search · NLP & embeddings · Vector databases · Multi-provider LLM integration · Speech-to-text & TTS

</td><td width="50%" valign="top">

**📏 Evaluation**

LLM evaluation · Model benchmarking & selection · RAG evaluation · Golden-set & edge-case test data · Labelled benchmarks · Graders · Reference-based scoring · Faithfulness & factual consistency · Regression gating before release · Regression monitoring · Handling non-deterministic outputs · Provenance-tracked runs · Human-in-the-loop review · LangSmith tracing

</td></tr>
<tr><td width="50%" valign="top">

**⚙️ Backend & infrastructure**

Python · FastAPI · REST APIs · Microservices · Webhooks · System design · Task-based processing · PostgreSQL · MySQL · SQL · Redis · pandas · Data pipelines · AWS · Docker · Production deployment · Cloud-native basics · Observability · Cost optimisation · Workflow automation

</td><td width="50%" valign="top">

**🧭 Product**

Technical product management · Roadmap & prioritisation · Product discovery · Competitor benchmarking · PRDs, specs & user stories · Wireframing & rapid prototyping · Scope & success criteria · Adoption tracking · Success metrics & ROI · Experiment-driven iteration · RAG-vs-agent architecture decisions · Model & vendor selection · Stakeholder management · Cross-functional delivery · Agile delivery · Enterprise integration

</td></tr>
</table>

> **Where I don't go:** model training and fine-tuning. I've solved those problems with retrieval, orchestration and evaluation instead — happy to talk about when I'd reach for fine-tuning and why I haven't needed to yet.

---

## 📈 Activity

<div align="center">

![Mohan's GitHub stats](https://github-readme-stats.vercel.app/api?username=MohanVishe&show_icons=true&theme=tokyonight&hide_border=true&count_private=true)

![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=MohanVishe&layout=compact&theme=tokyonight&hide_border=true&langs_count=8)

</div>

---

## 💬 Currently

🔭 Building production GenAI at FutureSmart AI

🌱 Going deeper on agent evaluation — measuring agent quality, not just model quality

👀 Open to **AI Engineer** and **Technical Product Manager** roles

📫 **mohanvishe.plus@gmail.com** · [LinkedIn](https://www.linkedin.com/in/mohanvishe)

<div align="center">
<br>

*I'd rather ship one system people use than prototype five that nobody does.*

</div>
