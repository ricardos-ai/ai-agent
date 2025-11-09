
# 🤖 AI Data Assistant Agent — LangChain × Streamlit × Docker

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/ricardos-ai/ai-agent?quickstart=1)

This repository provides **production-grade reference implementations** of LangChain-based AI agents deployed as Streamlit applications. Each example demonstrates a core AI engineering pattern—including memory management, retrieval-augmented reasoning, API integration, and containerized deployment.

---

## 🧩 Key Implementations

- **`basic_streaming.py`**: Demonstrates token-level streaming from `langchain.chat_models.ChatOpenAI` for responsive UIs.
- **`basic_memory.py`**: Showcases conversation persistence using `StreamlitChatMessageHistory` to maintain LLM state across user sessions.
- **`mrkl_demo.py`**: Reproduces the [MRKL Agent](https://python.langchain.com/docs/modules/agents/how_to/mrkl) with dynamic tool selection and decision chaining.
- **`minimal_agent.py`**: A minimal search-augmented agent leveraging environment variables for secure key management (`OPENAI_API_KEY`).
- **`search_and_chat.py`**: A retrieval-enabled chatbot with persistent memory for contextual multi-turn reasoning.
- **`simple_feedback.py`**: Implements human-in-the-loop evaluation via [streamlit-feedback](https://github.com/trubrics/streamlit-feedback) and integrates [LangSmith](https://docs.smith.langchain.com/) for traceability.
- **`chat_with_documents.py`**: A document-grounded assistant performing contextual retrieval (RAG) using vector stores such as FAISS or Chroma.
- **`chat_with_sql_db.py`**: Enables natural language interaction with SQL databases, executing verified queries through an LLM agent.
- **`chat_pandas_df.py`**: Interactive analysis of Pandas DataFrames with controlled Python AST execution (⚠️ review security implications).

Each app illustrates LangChain’s modular architecture for **callback tracing**, **tool orchestration**, and **session-based memory persistence** within Streamlit.

---

## ⚙️ Setup & Environment

This project uses **Poetry** for dependency management and reproducible builds.

```bash
poetry install
poetry shell
pre-commit install
```

---

## 🚀 Running Locally

Run any Streamlit app directly:
```bash
streamlit run streamlit_agent/mrkl_demo.py
```

---

## 🐳 Running with Docker

The included **Dockerfile** supports multi-stage builds optimized for image size and caching.

```bash
DOCKER_BUILDKIT=1 docker build --target=runtime . -t ai-data-agent:latest
```

Run the container:
```bash
docker run -d --name ai-data-agent -p 8051:8051 ai-data-agent:latest
```

Or with Compose (recommended):
```bash
docker-compose up
```

---

## 💡 Contribution & Extensions

Future iterations will extend to multi-agent coordination, vector-based reasoning, and advanced observability pipelines. Contributions enhancing **RAG quality**, **data connectivity**, or **deployment automation** are welcome.

> This repository exemplifies applied **AI Engineering** — integrating LLM reasoning, retrieval systems, and containerized infrastructure into reproducible, interactive data assistants.
=======
# ai-agent
A production ready AI agent integrating LangChain, Streamlit, and Docker to enable real time LLM reasoning, data retrieval (RAG, SQL, Pandas), conversational memory, and feedback tracking, demonstrating advanced AI engineering, model orchestration, and containerized deployment skills.
