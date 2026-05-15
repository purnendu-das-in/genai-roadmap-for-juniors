# Full Stack GenAI Developer Roadmap 2026 Edition

> A visual, interview ready roadmap to become a **full stack GenAI developer** in 2026 — built for freshers, juniors, students, and professionals shifting into GenAI.

This roadmap answers one question: **"I'm new — what do I actually need to learn, build, deploy, and explain in interviews?"** No 100-hour course lists, no theory marathons. Just the essentials, sequenced, with hands-on proof for every concept.

- **Live site:** https://genai-roadmap.purnendudas.in/
- **Hands-on notebook:** [Open in Google Colab](https://colab.research.google.com/drive/1Lpdk15uITxlHoQesHdS-PSQlWSAtTQvf?usp=sharing/) — 9 sections, ~6 hours, beginner-friendly.

---

## The whole journey at a glance

```mermaid
flowchart TD
    S0(["🧭 Stage 0<br/>Setup & Mindset"]) --> S1(["🐍 Stage 1<br/>Python Essentials"])
    S1 --> S2([📐 Stage 2<br/>Just-Enough Math])
    S2 --> S3([🤖 Stage 3<br/>ML Foundations])
    S3 --> S4([🧠 Stage 4<br/>Deep Learning])
    S4 --> S5([🔤 Stage 5<br/>NLP & Transformers])
    S5 --> S6([💬 Stage 6<br/>LLMs])
    S6 --> S7([✍️ Stage 7<br/>Prompt Engineering])
    S7 --> S8([📚 Stage 8<br/>RAG])
    S8 --> S9([🧰 Stage 9<br/>Frameworks])
    S9 --> S10([🕹️ Stage 10<br/>Agents])
    S10 --> S11([🎯 Stage 11<br/>Fine-tuning])
    S11 --> S12([🚀 Stage 12<br/>Deployment])
    S12 --> S13([🛡️ Stage 13<br/>Responsible AI])
    S13 --> JOB{{💼 Portfolio<br/>+ Interviews}}

    classDef foundation fill:#dbeafe,stroke:#2563eb,color:#1e3a8a
    classDef ml fill:#dcfce7,stroke:#16a34a,color:#14532d
    classDef applied fill:#fef3c7,stroke:#d97706,color:#78350f
    classDef advanced fill:#fce7f3,stroke:#be185d,color:#831843
    classDef ship fill:#ede9fe,stroke:#7c3aed,color:#4c1d95

    class S0,S1,S2 foundation
    class S3,S4,S5 ml
    class S6,S7,S8 applied
    class S9,S10,S11 advanced
    class S12,S13,JOB ship
```

> **Rule of thumb:** if you've already worked as a software engineer, you can skim Stages 0–4 and start at **Stage 5**. If you're brand new, start at Stage 0 and don't skip.

---

## How to use this roadmap

1. **Go in order.** Each stage builds on the previous — skipping creates fragile knowledge.
2. **Aim for working understanding, not perfection.** You'll deepen as you build.
3. **Code beats theory.** Build the listed mini-project at the end of each stage.
4. **Time-box.** If a stage takes more than 1.5× the suggested time, simplify and move on. Come back later.
5. **Keep one notebook open.** Open [Python Code Samples.ipynb](Python%20Code%20Samples.ipynb) in Colab and run cells as you progress.

---

## Interview-ready hiring bar

Before applying, make sure your portfolio proves these six abilities:

| Skill | What you should be able to do | Proof |
|---|---|---|
| Software foundation | Python, Git, CLI, virtual envs, HTTP, JSON, env vars, light tests | Project folder with scripts, setup, screenshots, and project notes |
| LLM API fluency | Streaming, retries, rate limits, structured output, token/cost logs | Hosted summarizer or support ticket triage tool |
| RAG quality | Load, chunk, embed, store, retrieve, re-rank, cite, evaluate | Chat-with-PDF with citations + eval sheet |
| Agents/tools | Function calling, typed schemas, tool tests, memory, iteration caps | Research agent with 2–3 tools and traces |
| Production habits | FastAPI, Docker, Pydantic, observability, guardrails, secrets | Public URL with logs, failures, and cost notes |
| Interview clarity | Explain prompt vs RAG vs fine-tune, hallucinations, security, evals | Portfolio case studies with architecture and tradeoffs |

---

## The roadmap

### Stage 0 — Mindset & Setup *(1–2 hours)*
- **What GenAI actually is:** statistical models that generate **tokens** (text), pixels (images), samples (audio), or actions. They predict what comes next given context — they don't "understand" or "look things up" by default.
- **Install:** Python 3.10+, VS Code, Git, and one clean project workspace.
- **Learn:** the command line, virtual environments (`venv` or `conda`), and basic Git (`clone`, `commit`, `push`, `pull`, `branch`).
- **Sign up:** [Google AI Studio](https://aistudio.google.com/), [Hugging Face](https://huggingface.co/), and one hosted-model provider such as [OpenAI](https://platform.openai.com/) or [Anthropic](https://console.anthropic.com/). Use free tiers first; provider limits change, so check current pricing before scaling.
- **Profile setup:** clear LinkedIn headline, simple portfolio page, and one clean project case study.
- **Mini-deliverable:** build a "hello world" Python project with setup steps, one screenshot, and a short note on what GenAI actually means.

### Stage 1 — Python Essentials *(1–2 weeks)*
- Variables, types, control flow, functions, classes.
- Working with **files**, **JSON**, **CSV**, environment variables, and **HTTP APIs** (`requests`).
- API basics: status codes, headers, auth tokens, timeouts, retries, pagination, and rate limits.
- Libraries to know: `numpy` (arrays), `pandas` (tables), `matplotlib` (plots).
- Exception handling, list/dict comprehensions, f-strings, type hints, and light testing with `pytest`.
- Backend preview: build one tiny `FastAPI` endpoint so deployment later does not feel alien.
- **Mini-deliverable:** write a script that reads a CSV, calls a public API with retries, validates the response, and writes clean JSON. ~70 lines.

### Stage 2 — Math (Just Enough) *(2–4 days)*
You don't need a math degree. You need **intuition**.
- **Linear algebra:** vectors, matrices, dot products, what "similarity" means geometrically.
- **Probability:** distributions, expectation, why softmax exists.
- **Calculus:** what a gradient is and why "going downhill" trains a model.
- **Goal:** read a paper's diagram and not feel lost. That's it.

### Stage 3 — Machine Learning Foundations *(1 week)*
- Supervised vs unsupervised vs reinforcement learning.
- Train/validation/test splits, **overfitting**, **bias-variance tradeoff**.
- Evaluation metrics: accuracy, precision, recall, F1, MSE, perplexity.
- Use **scikit-learn** on a small tabular dataset (Iris, Titanic) to feel the workflow.
- Understand **a neuron** → forward pass → loss → backprop → gradient descent. Karpathy's *micrograd* is the gold standard.

### Stage 4 — Deep Learning Basics *(1–2 weeks)*
- Tensors, layers, activations (ReLU, GELU), loss functions, optimizers (SGD, Adam).
- Pick **one** framework — **PyTorch** (recommended; what every modern paper uses) **or** Keras.
- Build end-to-end:
  - A tiny **MLP** for MNIST.
  - A small **CNN** for CIFAR-10.
  - A character-level **RNN/Transformer** for text generation.
- **Mini-deliverable:** train a network that beats random on a real dataset, saved as a notebook with charts.

### Stage 5 — NLP & Transformers *(1 week)*
This is where GenAI starts.

```mermaid
flowchart LR
    T["Hello world"] -->|tokenizer| TOK["IDs: 15496, 995"]
    TOK -->|embedding lookup| EMB[("vectors<br/>e.g. 768-dim each")]
    EMB --> ATT[Self-attention<br/>each token looks at every other]
    ATT --> FFN[Feed-forward<br/>+ residuals + layer norm]
    FFN -.repeat N layers.-> OUT[Logits over vocabulary]
    OUT -->|argmax / sampling| NEXT["next token: '!'"]
    NEXT -.feed back.-> T

    classDef in fill:#fef3c7,stroke:#d97706
    classDef proc fill:#dbeafe,stroke:#2563eb
    classDef out fill:#dcfce7,stroke:#16a34a
    class T,TOK in
    class EMB,ATT,FFN proc
    class OUT,NEXT out
```

- **Tokenization:** how text becomes numbers (BPE, SentencePiece). Words ≠ tokens.
- **Embeddings:** vectors that capture meaning. Similar meaning → similar vectors.
- **Attention:** the mechanism that lets a model "look at" earlier tokens with different weights. Understand the *intuition*, not the matrix algebra.
- **Encoder vs decoder vs encoder-decoder:** BERT (encoder, understanding), GPT/Llama/Claude (decoder, generation), T5/BART (both, translation/summarization).
- **Hands-on:** [Hugging Face Transformers](https://huggingface.co/docs/transformers) — load a model, run `pipeline(...)`, inspect outputs.

### Stage 6 — Large Language Models (LLMs) *(3–5 days)*
- **Pre-training** (predict next token on the internet) → **post-training** (instruction tuning + RLHF/DPO to make it useful and safe).
- **Open-weight vs closed:** Llama, Mistral, Qwen, DeepSeek, Gemma (open) vs GPT, Claude, Gemini (closed APIs).
- **Knobs you'll actually use:**
  - **Context window** — how much text the model can "see" at once (now 128K–2M tokens depending on model).
  - **Tokens** — billing unit and length unit. ~1 token ≈ 4 English characters or ¾ of a word.
  - **Temperature** — 0 = deterministic, 1 = creative, >1 = chaotic. Default 0.2–0.7.
  - **top-p / top-k** — alternative sampling controls. Stick with temperature unless you have a reason.
- **API production basics:** streaming, retries with backoff, timeout handling, rate-limit handling, model fallback, and per-request cost logging.
- **Hands-on:** call a hosted LLM with streaming + retries, log tokens/latency, then run a small open model locally with [Ollama](https://ollama.com/) or `transformers`.

### Stage 7 — Prompt Engineering *(3–5 days)*
- **Zero-shot, few-shot, chain-of-thought.**
- **Roles:** `system` (rules), `user` (input), `assistant` (response). Use them.
- **Structured output:** ask for JSON; better, use the model's *structured-output* mode (`response_format`, `with_structured_output`, etc.). Validate with **Pydantic**.
- **Function / tool calling:** the model returns *which function to call* with *what arguments*; your code runs it and feeds the result back.
- **Prompt evals:** save 20 tricky inputs, run them after every prompt change, and keep the prompt version in logs.
- **Pitfalls:** **hallucinations** (confidently wrong), **prompt injection** (user input overrides system rules), **context drift** in long chats.

```mermaid
flowchart LR
    P[Prompt] --> M{Did it work?}
    M -->|Yes| DONE[✅ Ship it]
    M -->|Mostly. Bad format| P1[Tighten the prompt<br/>+ JSON / Pydantic schema]
    M -->|It doesn't know my data| RAG[Add RAG<br/>Stage 8]
    M -->|Wrong style/skill, even with examples| FT[Fine-tune<br/>Stage 11]
    P1 --> P
    RAG --> DONE
    FT --> DONE

    classDef good fill:#dcfce7,stroke:#16a34a
    classDef warn fill:#fef3c7,stroke:#d97706
    class DONE good
    class P1,RAG,FT warn
```

> **Always try in this order: Prompt → RAG → Fine-tune.** Each step costs 10–100× more effort than the previous. Don't skip ahead.

### Stage 8 — RAG (Retrieval-Augmented Generation) *(1 week)*

```mermaid
flowchart LR
    subgraph INDEX["1️⃣ Build (offline, once)"]
        D[Your docs<br/>PDFs, wiki, tickets] --> CH[Chunk<br/>~300–800 tokens]
        CH --> EMB1[Embedding model<br/>e.g. all-MiniLM-L6-v2]
        EMB1 --> VDB[(Vector DB<br/>FAISS / Chroma / Qdrant / Pinecone)]
    end

    subgraph QUERY["2️⃣ Answer (every request)"]
        Q[User question] --> EMB2[Same embedding model]
        EMB2 --> SEARCH[Top-k similarity search]
        VDB --> SEARCH
        SEARCH --> CTX[Top chunks = context]
        CTX --> PROMPT[Prompt = system + context + question]
        PROMPT --> LLM[LLM]
        LLM --> A[Grounded answer<br/>with citations]
    end

    classDef offline fill:#dbeafe,stroke:#2563eb
    classDef online fill:#dcfce7,stroke:#16a34a
    class D,CH,EMB1,VDB offline
    class Q,EMB2,SEARCH,CTX,PROMPT,LLM,A online
```

- **Why RAG:** LLMs don't know your data and have a knowledge cutoff. RAG injects relevant snippets into the prompt at query time.
- **Embeddings & vector DBs:** FAISS (local, free), Chroma (local + simple), Qdrant (production OSS), Pinecone (managed).
- **Chunking:** start with `RecursiveCharacterTextSplitter`, ~500 tokens, ~50 overlap. Tune later.
- **Re-ranking:** add a cross-encoder (e.g. `bge-reranker`) on top-20 → top-3 for big quality wins.
- **Hybrid search:** combine keyword/BM25 with vector search when exact terms, IDs, or error codes matter.
- **RAG evals:** measure context recall, faithfulness, answer relevance, citation accuracy, and "I don't know" behavior.
- **Mini-deliverable:** **"Chat with your PDF"** with source citations, retrieved chunk preview, and a 25-question eval sheet. (Section 6 of the notebook.)

### Stage 9 — Frameworks & Tooling *(1 week)*
- **Orchestration:** **LangChain** (broadest) or **LlamaIndex** (RAG-first). Pick one. Both are fine.
- **Validation:** **Pydantic** v2 — your defense against malformed LLM output.
- **UIs in <50 lines:** **Gradio** (great for ML demos) or **Streamlit** (great for dashboards).
- **Observability:** **LangSmith**, **Langfuse**, or **Phoenix** — see every prompt, response, and tool call.
- **Model gateway:** use LiteLLM or a thin adapter layer so switching providers does not rewrite your app.
- **Integration pattern:** learn MCP basics if you want agents/tools to connect cleanly to external systems.
- **Experiment tracking (optional):** Weights & Biases, MLflow.

### Stage 10 — Agents & Multi-step Workflows *(1–2 weeks)*

```mermaid
flowchart LR
    U[User goal] --> AG{LLM<br/>plans next step}
    AG -->|"Thought:<br/>I need to search the docs"| TOOL[Pick a tool<br/>+ arguments]
    TOOL --> EXEC[Run tool<br/>search / API / code]
    EXEC -->|"Observation"| AG
    AG -->|"I have enough info"| ANS[Final answer]

    classDef think fill:#fef3c7,stroke:#d97706
    classDef act fill:#dbeafe,stroke:#2563eb
    classDef done fill:#dcfce7,stroke:#16a34a
    class AG think
    class TOOL,EXEC act
    class ANS done
```

- **Agent = LLM + tools + memory + a loop.** The **ReAct** pattern (Reason → Act → Observe → repeat) is the foundation.
- **Tool use / function calling:** the LLM emits a JSON call; your runtime executes it and returns the result.
- **Frameworks:** **LangGraph** (graphs, controllable, recommended), **CrewAI** (role-based), **AutoGen** (multi-agent chat), **OpenAI Agents SDK**.
- **Tool quality:** typed schemas, input validation, deterministic tool tests, clear errors, and a max-iteration budget.
- **Memory:** separate short-term conversation state from long-term user/profile memory; never store sensitive data by accident.
- **Watch out for:** infinite loops (always cap iterations), runaway costs (log every call), bad tools (a flaky tool poisons the whole agent).
- **Mini-deliverable:** a research agent that takes a question, calls 2-3 tools, shows its trace, writes a 1-page sourced report, and stops on budget.

### Stage 11 — Fine-tuning & Customization *(Optional but powerful)*
**Use this when prompting + RAG genuinely cannot get you there** — usually for *style*, *tone*, *domain language*, or *strict format adherence*, not for adding facts.
- **LoRA / QLoRA** — train a small "adapter" instead of the full model. Runs on a single consumer GPU.
- **Datasets:** quality > quantity. 500 hand-curated examples beat 50,000 noisy ones.
- **Evaluation:** build an eval set *before* you fine-tune. If you can't measure it, you can't improve it.
- **Tools:** Hugging Face `peft` + `trl`, Unsloth, Axolotl.

### Stage 12 — Deployment & Productionization *(1 week)*

```mermaid
flowchart LR
    DEV[Notebook<br/>that works] --> APP[FastAPI / Flask app<br/>+ Pydantic schemas]
    APP --> DOCK[Dockerfile<br/>requirements.txt]
    DOCK --> HOST{{Where?}}
    HOST --> HF[🤗 HF Spaces<br/>free, easy]
    HOST --> RND[Render<br/>free tier]
    HOST --> RAIL[Railway<br/>$5/mo Hobby]
    HOST --> CLOUD[AWS / GCP / Azure<br/>full control]

    APP --> OBS[Observability<br/>LangSmith / Langfuse]
    APP --> GUARD[Guardrails<br/>input/output filters]
    APP --> COST[Cost tracking<br/>tokens × price]

    classDef green fill:#dcfce7,stroke:#16a34a
    classDef blue fill:#dbeafe,stroke:#2563eb
    classDef yellow fill:#fef3c7,stroke:#d97706
    class HF,RND green
    class RAIL,CLOUD blue
    class OBS,GUARD,COST yellow
```

- Wrap your model in **FastAPI**. Validate input/output with **Pydantic**.
- Containerize with **Docker** so it runs the same everywhere.
- Free / cheap hosting: **Hugging Face Spaces** (free GPU on a queue), **Render** (free web service tier), **Railway** ($5/mo Hobby).
- Production basics: secrets management, request queues, caching, background jobs, health checks, CI/CD, and rollback notes.
- Reliability basics: retry only safe operations, cap output tokens, add timeouts, and surface useful errors to users.
- **Don't ship without:** logging, error handling, rate limiting, a kill-switch, a per-request token-cost log, and a small eval set you can run before releases.

### Stage 13 — Responsible AI *(ongoing)*
Not a stage you "finish" — it's a lens for everything above.
- **Hallucinations:** assume they happen. Cite sources, validate, add a confidence step.
- **Prompt injection / jailbreaks:** treat user input as *untrusted*. Never let it override system instructions for sensitive actions.
- **Data leakage:** don't send PII, secrets, or proprietary data to third-party APIs without consent. Use a self-hosted model when in doubt.
- **Bias & fairness:** test across demographics; don't assume "default" outputs are neutral.
- **Security baseline:** know the [OWASP Top 10 for LLM Apps](https://owasp.org/www-project-top-10-for-large-language-model-applications/) and design around prompt injection, data exfiltration, excessive agency, and insecure plugins/tools.
- **Evals & guardrails:** Ragas for RAG, DeepEval, Guardrails AI, NeMo Guardrails.

---

## Minimal toolkit (one row = one decision)

| Area | Pick this | Why |
|---|---|---|
| Language | Python 3.10+ | Every GenAI library lives here |
| DL framework | PyTorch | What modern papers and HF use |
| LLM API | Gemini, OpenAI, Anthropic | Learn one deeply, compare two others for tradeoffs |
| Backend API | FastAPI | Simple, typed, production-shaped Python web services |
| LLM library (open) | Hugging Face Transformers | Standard for any open model |
| Local model runner | Ollama | One command to run Llama / Qwen / Gemma |
| Model gateway | LiteLLM or thin adapter | Switch providers without rewriting app logic |
| Orchestration | LangChain *or* LlamaIndex | Pick one and commit |
| Vector DB (start) | FAISS *or* Chroma | Local, free, zero ops |
| UI prototype | Gradio *or* Streamlit | Demo in < 50 lines |
| Validation | Pydantic v2 | Stops malformed JSON from breaking prod |
| Agent framework | LangGraph | Most controllable; pairs with LangChain |
| Tool integration | Function calling + MCP basics | Clean schemas and reusable tool connections |
| RAG evals | Ragas or DeepEval | Measure faithfulness instead of trusting vibes |
| Observability | LangSmith *or* Langfuse | See every prompt + response |
| Deployment | Docker + HF Spaces | Free, fast, public URL |

---

## What does this actually cost? *(real numbers)*

For a learner doing the roadmap end-to-end, keep the first pass cheap: free tiers, local models, tiny datasets, and small eval sets before any paid scale-up.

| Provider | Tier | What you can do |
|---|---|---|
| **Google AI Studio (Gemini)** | Free / low-cost | Good for learner experiments; check current limits before large runs. |
| **OpenAI** | Optional paid credit | Useful for practice calls, extraction, routing, and structured output demos. |
| **Anthropic Claude** | Optional paid credit | Useful comparison provider for writing, analysis, and safety-focused workflows. |
| **Hugging Face** | Free | Datasets, model downloads, Spaces hosting (CPU). |
| **Ollama (local)** | Free | Runs on your laptop. 8GB RAM = 7B-parameter model territory. |

> **Beginner play:** start with free-tier hosted models + Ollama for local experiments. Spend money only when you need reliability, higher limits, or a production demo.

---

## Project ideas (build these, in order)

1. **Smart Summarizer** — paste an article → get a 5-bullet summary. *(Stage 7)*
2. **AI Support Ticket Triage** — paste a customer issue → category, priority, confidence, and suggested first reply (JSON via Pydantic). *(Stage 7)*
3. **Code Explainer Bot** — paste a function → get a beginner explanation. *(Stage 7)*
4. **Chat with your PDF** — RAG over a textbook or company handbook. *(Stage 8)*
5. **Mini Research Agent** — a goal in → a sourced report out. *(Stage 10)*
6. **Capstone:** something you'd actually use. A meal planner from your fridge photo. A journal that reflects with you. A study buddy that quizzes you from your own notes. **Personal > impressive.**

Portfolio quality bar:

| Must include | Why interviewers care |
|---|---|
| Live demo + screenshots | Proves you shipped beyond a notebook |
| Architecture diagram | Shows system thinking |
| Prompt examples + model choices | Shows tradeoff reasoning |
| Eval results + failure cases | Shows you can debug, not just demo |
| Cost/latency notes | Shows production awareness |
| Limitations + next steps | Shows judgment and honesty |

---

## Suggested 12-week plan

Practical timelines:

| Track | Time | Best for | Outcome |
|---|---:|---|---|
| Fast track | 6 weeks, 25-35 hrs/week | People who already know Python | 3-4 shipped projects + interview prep |
| Recommended | 12 weeks, 8-12 hrs/week | Freshers, students, working professionals | 6 portfolio projects + mock interviews |
| College track | 24 weeks, 4-6 hrs/week | Busy students | Slow, durable learning + polished capstone |

| Weeks | Focus | Deliverable | Interview checkpoint |
|---|---|---|---|
| 1-2 | Python + API basics | Project folder with scripts, tests, screenshots, and setup notes | Explain HTTP, JSON, env vars, errors, and version-control flow |
| 3-4 | ML + Deep Learning | Tiny image/text classifier with metrics | Explain overfitting, splits, metrics, and baselines |
| 5-6 | Transformers + LLM APIs | Hosted LLM tool with streaming + logs | Explain tokens, temperature, context, latency, and cost |
| 7-8 | Prompt engineering + RAG | Chat-with-PDF deployed publicly | Explain chunking, embeddings, retrieval, citations, and RAG evals |
| 9-10 | Agents + frameworks | Agent with 2-3 tools and visible trace | Explain tool schemas, loops, memory, budgets, and failures |
| 11 | Capstone build | One project you'd genuinely use | Prepare architecture story and tradeoff decisions |
| 12 | Deployment + polish | Project brief, demo video, eval report, blog post | Run mock system design and portfolio deep-dive rounds |

---

## Common beginner mistakes (avoid these)

1. **Tutorial loop.** You finish 12 courses and have no working project to show. Build first; learn while building.
2. **Jumping to fine-tuning.** 95% of "fine-tuning" tasks are actually RAG or prompt problems.
3. **Skipping evaluation.** "It looked good in 3 examples" isn't a result. Build a 20–50 example eval set early.
4. **Ignoring tokens.** Tokens are time, money, and quality. Always log them.
5. **Trusting LLM output blindly.** Validate JSON. Verify facts. Treat it like a junior engineer who's confident but new.
6. **Over-frameworking.** LangChain/LangGraph are great when you need them. For a 30-line script, plain `requests` + the SDK is fine.
7. **Building in secret.** Share your progress, publish small demos, and write up what you broke. The portfolio *is* the credential.

---

## Interview prep

| Question | Short answer |
|---|---|
| RAG vs fine-tuning? | RAG retrieves facts at query time; fine-tuning changes behavior/style/format. Try prompt → RAG → fine-tune. |
| How do you reduce hallucinations? | Ground with RAG, require citations, validate structured output, lower temperature for factual tasks, and run evals. |
| What is prompt injection? | User-supplied text tries to override system rules. Treat user input as data, validate tool calls, and confirm sensitive actions. |
| How do you evaluate an LLM app? | Build a saved eval set, define task-specific metrics, log results per prompt/model version, and rerun on every change. |
| How do you design a RAG chatbot? | Ingest docs, chunk, embed, store, retrieve, re-rank, assemble prompt, answer with citations, monitor and evaluate. |
| What makes an agent different? | An agent can choose tools, observe results, update state, and continue toward a goal. Cap loops and log tool traces. |
| How do you reduce latency/cost? | Use smaller models, trim context, cache, stream output, cap tokens, batch offline work, and measure every request. |
| What should a portfolio case study show? | Problem, demo, architecture, setup, prompt examples, evals, cost/latency notes, failures, limitations, and next steps. |

---

## Free resources (curated, ranked)

- **[Andrej Karpathy — Neural Networks: Zero to Hero](https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ)** — best deep-learning video series ever made.
- **[Hugging Face NLP Course](https://huggingface.co/learn/nlp-course)** + **[LLM Course](https://huggingface.co/learn/llm-course)** — practical, free, modern.
- **[DeepLearning.AI short courses](https://www.deeplearning.ai/short-courses/)** — 1-hour dives on Prompting, RAG, LangChain, Agents.
- **[fast.ai — Practical Deep Learning for Coders](https://course.fast.ai/)** — top-down, very fast progress.
- **[Full Stack Deep Learning](https://fullstackdeeplearning.com/)** — production-grade systems.
- **Anthropic docs + OpenAI docs** — official patterns for building real API workflows.

---

## Glossary (for absolute beginners)

| Term | One-line meaning |
|---|---|
| **Token** | The chunk of text the model actually sees. ~4 characters or ¾ of a word. |
| **Context window** | How many tokens the model can read at once (input + output combined). |
| **Embedding** | A vector that represents meaning. Two similar sentences → two close vectors. |
| **Vector DB** | A database that stores embeddings and finds nearest neighbors fast. |
| **Temperature** | Randomness knob. 0 = same answer every time, 1 = creative. |
| **System prompt** | Persistent instructions the model follows for the whole conversation. |
| **Hallucination** | Confident-sounding but wrong output. Mitigate with RAG + citations. |
| **RAG** | "Look it up in my docs, then answer using what you found." |
| **Hybrid search** | Combining keyword search and vector search so exact terms and semantic meaning both work. |
| **Re-ranking** | A second model reorders retrieved chunks so the best evidence reaches the LLM first. |
| **Fine-tuning** | Updating the model's weights on your data — usually a small LoRA adapter. |
| **Agent** | An LLM that can choose to call tools in a loop until a goal is met. |
| **Tool / function calling** | The LLM emits a JSON call; your code runs it; the result goes back. |
| **MCP** | Model Context Protocol: a standard way for AI apps to connect to external tools and data sources. |
| **Prompt injection** | A user smuggling instructions into your prompt to override system rules. |
| **Eval set** | A saved set of inputs and expected behavior you rerun after prompt, model, or code changes. |
| **Latency** | How long the user waits. LLM latency comes from retrieval, model time, output length, and network. |
| **Rate limit** | A provider cap on requests or tokens per minute. Handle it with backoff and queues. |
| **Inference** | Running the model to get a result (vs. training, which builds the model). |

---

## Stay Updated

Found something missing, wrong, or out-of-date? Send a LinkedIn message with the source and a short explanation.

If you used this and built something cool, share it on LinkedIn and tag Purnendu Das so more freshers can learn from it.

---
