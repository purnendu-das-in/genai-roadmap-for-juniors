# 🚀 GenAI Roadmap for Juniors & Career Switchers

> A minimal, beginner-friendly roadmap to break into **Generative AI** — built for students, juniors, and professionals shifting their career toward GenAI.

This repository is a **practical, no-fluff guide** that lists only the things you *really* need to learn to become productive with Generative AI. No 100-hour courses, no overwhelming book lists — just the essentials, in the right order.

📖 **Live site:** _GitHub Pages will be enabled for this repo._
📓 **Hands-on notebook:** _A Jupyter notebook will be added soon._

---

## 🧭 How to use this roadmap

1. Go through the stages **in order** — each one builds on the previous.
2. For every topic, aim for a **working understanding**, not perfection.
3. Build a tiny project at the end of each stage. Code beats theory.
4. Revisit fundamentals whenever you feel stuck.

---

## 🪜 The Roadmap

### Stage 0 — Mindset & Setup
- Understand what GenAI is (and isn't): models that generate text, images, audio, code.
- Install: **Python 3.10+**, **VS Code**, **Git**, **GitHub account**.
- Learn the basics of the **command line** and **virtual environments** (`venv` / `conda`).
- Create a free account on **Hugging Face** and **OpenAI / Anthropic / Google AI Studio** (any one).

### Stage 1 — Python Essentials
- Variables, data types, control flow, functions, classes.
- Working with files, JSON, and APIs (`requests`).
- Libraries to know: `numpy`, `pandas`, `matplotlib`.
- Practice on small scripts — no need to master everything.

### Stage 2 — Math (Just Enough)
- **Linear algebra basics:** vectors, matrices, dot products.
- **Probability basics:** distributions, expectations.
- **Calculus intuition:** gradients & derivatives (conceptually).
- Goal: understand *why* models work, not derive them from scratch.

### Stage 3 — Machine Learning Foundations
- Supervised vs unsupervised learning.
- Train/test split, overfitting, evaluation metrics.
- Try **scikit-learn** with a small dataset.
- Understand what a **neural network** is and how it learns (forward + backprop intuition).

### Stage 4 — Deep Learning Basics
- Tensors, layers, activation functions, loss functions, optimizers.
- Pick **one** framework: **PyTorch** (recommended) or **TensorFlow/Keras**.
- Build a tiny image classifier or text classifier end-to-end.

### Stage 5 — NLP & Transformers
- Tokenization, embeddings, attention mechanism.
- The **Transformer architecture** (high-level intuition is enough at first).
- Encoder vs decoder vs encoder-decoder models.
- Hands-on with 🤗 **Hugging Face Transformers**.

### Stage 6 — Large Language Models (LLMs)
- What an LLM is, how it's pre-trained and fine-tuned.
- Open vs closed models (Llama, Mistral, GPT, Claude, Gemini).
- Context windows, tokens, temperature, top-p.
- Try calling an LLM API and a local model with `transformers` or `ollama`.

### Stage 7 — Prompt Engineering
- Zero-shot, few-shot, chain-of-thought prompting.
- System vs user vs assistant roles.
- Structured output (JSON), function/tool calling.
- Common pitfalls: hallucinations, prompt injection.

### Stage 8 — RAG (Retrieval-Augmented Generation)
- Why RAG: grounding LLMs with your own data.
- Embeddings & **vector databases** (FAISS, Chroma, Pinecone, Qdrant).
- Chunking strategies, similarity search, re-ranking.
- Build a mini **"chat with your PDF"** project.

### Stage 9 — Frameworks & Tooling
- **LangChain** or **LlamaIndex** — pick one and stick with it.
- **Pydantic** for structured outputs.
- **Streamlit** or **Gradio** for quick UIs.
- Experiment tracking: **Weights & Biases** or **MLflow** (optional).

### Stage 10 — Agents & Multi-step Workflows
- What an AI agent is: LLM + tools + memory + planning.
- ReAct pattern, tool use, function calling.
- Frameworks: **LangGraph**, **CrewAI**, **AutoGen**.
- Build a small agent that can browse, search, or call APIs.

### Stage 11 — Fine-tuning & Customization (Optional but Powerful)
- Prompting → RAG → Fine-tuning (use them in this order).
- **LoRA / QLoRA** for cheap fine-tuning.
- Datasets, instruction tuning, evaluation.
- Try fine-tuning a small open model on a custom dataset.

### Stage 12 — Deployment & Productionization
- Serve models with **FastAPI** or **Flask**.
- Containerize with **Docker**.
- Deploy on **Hugging Face Spaces**, **Render**, **Railway**, or **AWS/GCP/Azure**.
- Logging, monitoring, cost tracking, and basic safety guardrails.

### Stage 13 — Responsible AI
- Bias, fairness, hallucinations, privacy.
- Prompt injection, jailbreaks, data leakage.
- Evaluating model outputs and adding guardrails.

---

## 🛠️ Minimal Toolkit

| Area | Pick One |
|---|---|
| Language | Python |
| DL Framework | PyTorch |
| LLM Library | Hugging Face Transformers |
| Orchestration | LangChain *or* LlamaIndex |
| Vector DB | Chroma *or* FAISS |
| UI | Streamlit *or* Gradio |
| Deployment | Docker + Hugging Face Spaces |

---

## 🎯 Project Ideas (Build These!)

1. **Smart Summarizer** — paste an article, get a summary.
2. **Chat with your PDF** — RAG over your own documents.
3. **AI Resume Reviewer** — feedback on resumes via LLM.
4. **Code Explainer Bot** — paste code, get an explanation.
5. **Mini Research Agent** — agent that searches the web and writes a report.

---

## 📚 Recommended Free Resources

- **Andrej Karpathy** — *Neural Networks: Zero to Hero* (YouTube)
- **Hugging Face** — *NLP Course* and *LLM Course*
- **DeepLearning.AI** — short courses on Prompting, RAG, LangChain, Agents
- **fast.ai** — Practical Deep Learning for Coders
- **Full Stack Deep Learning** — production-grade ML/AI

---

## 🗓️ Suggested 12-Week Plan

| Weeks | Focus |
|---|---|
| 1–2 | Python + Math basics |
| 3–4 | ML + Deep Learning fundamentals |
| 5–6 | Transformers + LLM APIs |
| 7–8 | Prompt engineering + RAG |
| 9–10 | Agents + frameworks |
| 11 | Mini capstone project |
| 12 | Deployment + portfolio polish |

---

## 🤝 Contributing

Found something missing or outdated? PRs and issues are very welcome. This roadmap is meant to evolve with the field.

---

## 📓 Coming Soon

- A hands-on **Jupyter notebook** with runnable examples for each stage.
- More project walkthroughs.

---

⭐ If this helped you, consider starring the repo so others can find it too.
