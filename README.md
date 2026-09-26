<div align="center">

# Hi, I'm Mohan 👋

### I build AI systems — and decide what ships.

**AI Engineer & Technical Product Manager** at [FutureSmart AI](https://futuresmart.ai)

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

**The habit that defines my work: I measure before I choose.** A model swap has to prove itself on accuracy against a fixed benchmark before cost enters the conversation. That instinct is public in [nl2sql-finetune-reliability](https://github.com/MohanVishe/nl2sql-finetune-reliability), [nl2sql-reliability](https://github.com/MohanVishe/nl2sql-reliability) and [pdf-parser-benchmark](https://github.com/MohanVishe/pdf-parser-benchmark), and private in the evaluation harness behind the products below.

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

### 🎛️ [Does Fine-Tuning Buy Reliability?](https://github.com/MohanVishe/nl2sql-finetune-reliability)

**Teams fine-tune to make a model more dependable. I trained one and measured whether that is what you get.**

QLoRA fine-tune of Qwen2.5-Coder-3B on 5,851 examples, then 4,960 scored attempts per model against an **untrained control** put through the identical pipeline — all 434 of its weight tensors verified byte-identical to the published model's before any comparison was allowed.

Capability rose **4.2 points** and reliability **4.4**, so the reliability gap showed no detectable change: `−0.2 [−4.8, +4.4]`. What training did buy has a catch for a production system — **execution errors fell 19.8 points while silently wrong answers rose 14.5**: in net rates, about a quarter of that drop became right answers and the rest became queries that run fine and return the wrong rows. And against a prompted 7B, the fine-tuned 3B can't be separated on pass@10 (`−3.8 [−7.9, +0.4]`) but is **8.1 points behind on a single try and 12.7 behind on right-every-time** — the cheap swap a capability-only comparison would wave through.

Hypotheses and decision rule written down before training, reported as written when the result supported neither. Every one of the 9,920 scored generations published.

`PyTorch` · `PEFT / QLoRA` · `TRL` · `bitsandbytes` · `llama.cpp / GGUF` · `Ollama` · `Qwen2.5-Coder`

📄 [Full write-up](https://mohanvishe.vercel.app/projects/nl2sql-finetune-reliability)

---

### 🧪 [NL2SQL Reliability Study](https://github.com/MohanVishe/nl2sql-reliability)

**Ask an AI the same database question ten times — do you get the same right answer?** 14,880 scored generations say no.

Most leaderboard text-to-SQL scores come from asking each question once. This asks ten times and reports both `pass@10` (right at least once — capability) and `pass^10` (right every time — reliability). The gap is **13.9 points**, and **41% of attempts ran without error and returned rows that didn't match the reference** — silent failures outnumber crashes about 2.5 to 1. An agentic retry loop raised both scores with no detectable change to the gap; a smaller model widened it 1.7×.

Expert-corrected benchmark, no LLM-as-judge, every raw attempt published so any reader can recompute the numbers. 285 tests, 269 in CI. Run locally at zero cost.

`Python` · `Ollama` · `Qwen2.5-Coder` · `SQLite` · `pytest` · `GitHub Actions`

📄 [Full write-up](https://mohanvishe.vercel.app/projects/nl2sql-reliability)

---

### 📐 [Decisions in AI Systems](https://github.com/MohanVishe/product-case-studies)

Two write-ups on one argument: **the price per token is the easiest number to read and the least useful one to decide on.**

*Cheaper per token, more expensive per task* — in an agentic loop you pay per completed task, and in a worked example a model 4× cheaper per token lands 16% more expensive per success; with caching it flips to 27% cheaper. So the piece builds the evaluation that answers it for real: an 8-tool agent, 24 graded multi-turn tasks, 120 conversations per model. At the orchestrator the small model needs to be **4.1× cheaper per token just to break even** (95% CI 2.4–7.5×; 20% of tasks passed against 62.5%), and caching doesn't rescue it. On a separate single-call router, break-even is **1.13×**. Same two models, two kinds of node, opposite answers.

*Price comes last* — the same argument as a product decision, where accuracy gates before cost is considered at all.

`Python` · `Agent evaluation` · `Cost modelling` · `Ollama`

---

<table>
<tr>
<td width="50%" valign="top">

### 🩺 [Medical RAG Chatbot](https://github.com/MohanVishe/medical-rag-chatbot)

Medical Q&A grounded in a PDF corpus, every answer citing the pages it came from.

**The interesting part isn't retrieval — it's refusal.** Probing showed why a similarity threshold alone can't make it say *"my sources don't cover that"*: out-of-corpus medical questions score as close as in-scope ones.

`Llama 2` · `LangChain` · `Pinecone` · `Flask`

</td>
<td width="50%" valign="top">

### 📑 [PDF Parser Benchmark](https://github.com/MohanVishe/pdf-parser-benchmark)

A scored benchmark harness: four hand-verified documents — ten scripts including right-to-left and Indic, three columns, a dense table, a scan — scored on character and word error rate.

No parser wins everywhere: one keeps three columns in reading order and loses every row of a ruled table, another keeps every row and reads straight across the columns.

`Python` · `PyPDF` · `PDFPlumber` · `LlamaParse` · `AWS Textract`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🎯 [HabitLoop](https://github.com/MohanVishe/ai-habit-tracker)

A habit tracker whose AI coach is only given statistics computed from your own log — and whose answers are checked against them before you see them.

Streaks, rates and rankings are pure Python; the model interprets them and never does arithmetic. A held-out eval written before the latest fixes (129 answers, local Qwen2.5-7B) measures **50.4% correct** (95% CI 41.9–58.9%): single figures and streaks are reliable, and comparisons are the measured next step. 153 tests, CI.

`LangChain` · `Llama 3` · `Streamlit` · `SQLite`

</td>
<td width="50%" valign="top">

### 🔍 [Product Similarity API](https://github.com/MohanVishe/product-similarity-api)

Embedding-based product search served over HTTP, with price and rating filters applied inside the vector query — not after it — and a similarity score on every result. A 40-query retrieval eval runs in CI: recall@3 0.958, MRR 0.922.

`FastAPI` · `Chroma` · `Embeddings`

</td>
</tr>
</table>

Plus **[Rossmann Sales Forecasting](https://github.com/MohanVishe/rossmann-sales-forecasting)** — a six-week-ahead forecast for 1,115 stores from inputs known at forecast time only, where LightGBM reaches RMSPE 0.1235 against 0.1449 for the strongest naive baseline. Kept because the fundamentals still matter.

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
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)

| | |
|---|---|
| 🧠 **AI & LLM** | LLMs · Generative AI · RAG · Agentic AI · Multi-agent systems · Tool calling · MCP · Prompt engineering · Structured outputs · Guardrails · Hallucination reduction · Embeddings · Vector databases · NL2SQL · Chatbots |
| 📏 **Evaluation & quality** | LLM evaluation · Model evaluation · Observability · LangSmith tracing · Metrics · Cost & latency optimisation · Experimentation |
| ⚙️ **Backend & cloud** | Python · FastAPI · REST APIs · SQL · PostgreSQL · System design · Scalability · Integrations · Data pipelines · Workflow automation · AWS · Docker · Git · CI/CD · Model deployment |
| 🎛️ **Fine-tuning** | LoRA · QLoRA · PEFT · TRL · PyTorch · bitsandbytes 4-bit NF4 · Adapter merging · Quantization (GGUF / llama.cpp) · Training-data contamination control · Held-out validation |
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
