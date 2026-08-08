# Python Library Guide and Topic Map

> This companion connects every handbook chapter to runnable Python examples. It distinguishes the **standard-library scenario implementation** already included with each chapter from the **library-based companion implementation** that demonstrates common production ecosystems.

## How to use this guide

1. Find a chapter in the chapter-to-code map.
2. Run its dependency-free scenario first to understand the control logic.
3. Install only the relevant requirements pack.
4. run the mapped library companion with `--help` and preferably `--dry-run` when it touches a remote model or service.
5. Replace synthetic connectors and policies with your organization-specific adapters only after the local behavior is understood.

## Installation packs

| Pack | File | Main topics |
|---|---|---|
| Foundations | [`requirements-foundations.txt`](../examples/library-companions/requirements-foundations.txt) | ML, deep learning, transformers, tabular analysis |
| RAG | [`requirements-rag.txt`](../examples/library-companions/requirements-rag.txt) | embeddings, FAISS, Chroma, LlamaIndex |
| Agents | [`requirements-agents.txt`](../examples/library-companions/requirements-agents.txt) | Agents SDK, LangGraph, CrewAI, AutoGen, LangChain, DSPy, ADK, Semantic Kernel |
| Interoperability and evaluation | [`requirements-interoperability-eval.txt`](../examples/library-companions/requirements-interoperability-eval.txt) | MCP, A2A, Ragas, DeepEval, OpenTelemetry |
| Service | [`requirements-service.txt`](../examples/library-companions/requirements-service.txt) | FastAPI, Uvicorn, HTTPX |

Use an isolated virtual environment. These packs are deliberately separated because installing every framework into one environment increases dependency conflicts and makes upgrades harder to diagnose.

## Library catalog

| Library | What it contributes | Handbook topics |
|---|---|---|
| `pydantic` | Typed contracts, validation, JSON Schema | prompts, tools, state, context, APIs, evaluation |
| `numpy` | Array operations and metrics | ML, embeddings, evaluation, performance |
| `pandas` | Tabular analysis and product experiments | product management, evaluation, observability |
| `scikit-learn` | Classical ML, TF-IDF, metrics, splitting | ML, retrieval baselines, evaluation |
| `torch` | Neural networks and tensor computation | deep learning, transformers |
| `transformers` | Pretrained transformer models and generation | LLMs, tokenization, generation |
| `openai` | Responses API and structured generation | LLMs, prompting, tools |
| `openai-agents` | Managed agent loop, tools, handoffs, sessions, guardrails, tracing | agents, orchestration, harnesses |
| `sentence-transformers` | Embedding models | RAG, semantic search |
| `faiss-cpu` | Efficient vector similarity search | RAG, vector indexes |
| `chromadb` | Persistent vector collections | RAG, memory |
| `llama-index` | Context augmentation, indexes, agents, workflows | RAG, agents |
| `langgraph` | Stateful graph workflows and loops | agents, orchestration, loop engineering |
| `langchain` | Agent construction, tools, middleware, structured output | dynamic tool routing |
| `crewai` | Role-based crews and flows | multi-agent systems |
| `autogen-agentchat` | Conversational agents and teams | multi-agent systems |
| `google-adk` | Agents, tools, sessions, workflows, evaluation | modern agent SDKs |
| `semantic-kernel` | Enterprise agents, plugins, orchestration | modern agent SDKs |
| `dspy` | Typed LM programs and prompt optimization | prompting, ReAct, evaluation |
| `mcp` | Standard tools, resources, and prompts | interoperability, context |
| `a2a-sdk` | Agent cards, messages, tasks, and agent collaboration | interoperability, multi-agent |
| `ragas` | RAG and agent evaluation metrics | evaluation |
| `deepeval` | LLM application tests and metrics | evaluation |
| `opentelemetry-sdk` | Portable traces and metrics | observability, operations |
| `fastapi` | Typed production APIs | application layer, deployment |
| `httpx` | Async HTTP clients and API testing | tools, A2A, FastAPI testing |
| `networkx` | Graph analysis and cycle detection | multi-agent, loop engineering |
| `scipy` | Statistical tests and optimization | experimentation, evaluation |

## Library example index

Every script uses `argparse`, writes JSON when `--output` is supplied, and avoids embedding secrets in source code. Remote examples support `--dry-run` where practical.

| Example | Libraries | Scenario | Important arguments | Execution note |
|---|---|---|---|---|
| [`01_sklearn_ticket_classifier.py`](../examples/library-companions/01_sklearn_ticket_classifier.py) | scikit-learn + pandas | Classical ML support-ticket classification | `--data PATH --text TEXT [--test-size FLOAT] [--seed INT] [--output PATH]` | Local; downloads nothing |
| [`02_torch_mlp_classifier.py`](../examples/library-companions/02_torch_mlp_classifier.py) | PyTorch | Neural-network training loop | `[--epochs INT] [--hidden INT] [--learning-rate FLOAT] [--seed INT] [--output PATH]` | Local synthetic data |
| [`03_transformers_generation.py`](../examples/library-companions/03_transformers_generation.py) | Hugging Face Transformers + PyTorch | Local text generation | `[--model MODEL] --prompt TEXT [--max-new-tokens INT] [--temperature FLOAT] [--output PATH]` | May download model weights |
| [`04_openai_structured_output.py`](../examples/library-companions/04_openai_structured_output.py) | OpenAI Python SDK + Pydantic | Schema-constrained classification | `--ticket TEXT [--model MODEL] [--dry-run] [--output PATH]` | Remote unless dry-run |
| [`05_sentence_transformers_faiss_rag.py`](../examples/library-companions/05_sentence_transformers_faiss_rag.py) | SentenceTransformers + FAISS + NumPy | Dense retrieval baseline | `--documents PATH --query TEXT [--model MODEL] [--top-k INT] [--output PATH]` | May download embedding model |
| [`06_llamaindex_rag.py`](../examples/library-companions/06_llamaindex_rag.py) | LlamaIndex | Document ingestion and RAG | `--directory PATH --query TEXT [--similarity-top-k INT] [--dry-run] [--output PATH]` | Remote/default model unless dry-run |
| [`07_openai_agents_sdk_support.py`](../examples/library-companions/07_openai_agents_sdk_support.py) | OpenAI Agents SDK | Managed agent loop and function tools | `--ticket TEXT [--model MODEL] [--dry-run] [--output PATH]` | Remote unless dry-run |
| [`08_langgraph_stateful_workflow.py`](../examples/library-companions/08_langgraph_stateful_workflow.py) | LangGraph | Stateful graph workflow | `--request TEXT [--max-revisions INT] [--dry-run] [--output PATH]` | Remote unless dry-run |
| [`09_crewai_research_crew.py`](../examples/library-companions/09_crewai_research_crew.py) | CrewAI | Role-based research crew | `--topic TEXT [--model MODEL] [--dry-run] [--output PATH]` | Remote unless dry-run |
| [`10_autogen_review_team.py`](../examples/library-companions/10_autogen_review_team.py) | AutoGen AgentChat | Conversational multi-agent review | `--task TEXT [--model MODEL] [--max-turns INT] [--dry-run] [--output PATH]` | Remote unless dry-run |
| [`11_langchain_dynamic_tools.py`](../examples/library-companions/11_langchain_dynamic_tools.py) | LangChain | Dynamic tool routing | `--request TEXT [--model MODEL] [--dry-run] [--output PATH]` | Remote unless dry-run |
| [`12_dspy_classifier.py`](../examples/library-companions/12_dspy_classifier.py) | DSPy | Declarative prompting and optimization surface | `--ticket TEXT [--model MODEL] [--dry-run] [--output PATH]` | Remote unless dry-run |
| [`13_mcp_server.py`](../examples/library-companions/13_mcp_server.py) | MCP Python SDK | Tool/resource server | `[--transport stdio|streamable-http] [--host HOST] [--port INT]` | Starts a local server |
| [`14_a2a_client.py`](../examples/library-companions/14_a2a_client.py) | A2A SDK + HTTPX | Remote agent discovery and delegation | `--agent-url URL --message TEXT [--timeout FLOAT] [--dry-run] [--output PATH]` | Remote unless dry-run |
| [`15_ragas_deepeval_eval.py`](../examples/library-companions/15_ragas_deepeval_eval.py) | Ragas + DeepEval | RAG and answer-quality evaluation | `--question TEXT --answer TEXT --context TEXT [--expected TEXT] [--framework ragas|deepeval|dry-run] [--output PATH]` | May call judge models unless dry-run |
| [`16_phoenix_opentelemetry_trace.py`](../examples/library-companions/16_phoenix_opentelemetry_trace.py) | OpenTelemetry / Phoenix-compatible tracing | Agent trace export | `[--endpoint URL] [--service NAME] [--dry-run] [--output PATH]` | Exports to configured endpoint unless dry-run |
| [`17_fastapi_agent_service.py`](../examples/library-companions/17_fastapi_agent_service.py) | FastAPI + Uvicorn + Pydantic | Typed agent-facing HTTP service | `[--host HOST] [--port INT] [--reload]` | Starts a local web server |
| [`18_pandas_product_experiment.py`](../examples/library-companions/18_pandas_product_experiment.py) | pandas + SciPy | AI product experiment analysis | `--data PATH --baseline NAME --candidate NAME [--max-latency-increase-pct FLOAT] [--output PATH]` | Local |
| [`19_google_adk_agent.py`](../examples/library-companions/19_google_adk_agent.py) | Google ADK | Function-tool agent | `--request TEXT [--model MODEL] [--dry-run] [--output PATH]` | Remote unless dry-run |
| [`20_semantic_kernel_agent.py`](../examples/library-companions/20_semantic_kernel_agent.py) | Semantic Kernel | Plugin-based agent | `--request TEXT [--deployment MODEL] [--dry-run] [--output PATH]` | Remote unless dry-run |
| [`21_chromadb_rag.py`](../examples/library-companions/21_chromadb_rag.py) | ChromaDB | Persistent vector retrieval | `--documents PATH --query TEXT [--persist-dir PATH] [--collection NAME] [--top-k INT] [--output PATH]` | Local; embedding function may download model |
| [`22_pydantic_context_contracts.py`](../examples/library-companions/22_pydantic_context_contracts.py) | Pydantic | Context-contract validation | `--input PATH [--schema PATH] [--output PATH]` | Local |

## What each library is teaching

### `01_sklearn_ticket_classifier.py` — Classical ML support-ticket classification

**Libraries:** scikit-learn + pandas

Trains TF-IDF + logistic regression and reports a holdout classification report.

**Arguments:** `--data PATH --text TEXT [--test-size FLOAT] [--seed INT] [--output PATH]`

**Execution:** Local; downloads nothing.

Run `python examples/library-companions/01_sklearn_ticket_classifier.py --help` for the generated CLI reference.

### `02_torch_mlp_classifier.py` — Neural-network training loop

**Libraries:** PyTorch

Trains a small MLP and reports loss, accuracy, and parameter count.

**Arguments:** `[--epochs INT] [--hidden INT] [--learning-rate FLOAT] [--seed INT] [--output PATH]`

**Execution:** Local synthetic data.

Run `python examples/library-companions/02_torch_mlp_classifier.py --help` for the generated CLI reference.

### `03_transformers_generation.py` — Local text generation

**Libraries:** Hugging Face Transformers + PyTorch

Creates a text-generation pipeline and exposes generation controls.

**Arguments:** `[--model MODEL] --prompt TEXT [--max-new-tokens INT] [--temperature FLOAT] [--output PATH]`

**Execution:** May download model weights.

Run `python examples/library-companions/03_transformers_generation.py --help` for the generated CLI reference.

### `04_openai_structured_output.py` — Schema-constrained classification

**Libraries:** OpenAI Python SDK + Pydantic

Uses a Pydantic response model; dry-run emits the request contract without an API call.

**Arguments:** `--ticket TEXT [--model MODEL] [--dry-run] [--output PATH]`

**Execution:** Remote unless dry-run.

Run `python examples/library-companions/04_openai_structured_output.py --help` for the generated CLI reference.

### `05_sentence_transformers_faiss_rag.py` — Dense retrieval baseline

**Libraries:** SentenceTransformers + FAISS + NumPy

Embeds documents, builds an inner-product FAISS index, and returns ranked evidence.

**Arguments:** `--documents PATH --query TEXT [--model MODEL] [--top-k INT] [--output PATH]`

**Execution:** May download embedding model.

Run `python examples/library-companions/05_sentence_transformers_faiss_rag.py --help` for the generated CLI reference.

### `06_llamaindex_rag.py` — Document ingestion and RAG

**Libraries:** LlamaIndex

Builds a VectorStoreIndex from a directory and queries it with source-node output.

**Arguments:** `--directory PATH --query TEXT [--similarity-top-k INT] [--dry-run] [--output PATH]`

**Execution:** Remote/default model unless dry-run.

Run `python examples/library-companions/06_llamaindex_rag.py --help` for the generated CLI reference.

### `07_openai_agents_sdk_support.py` — Managed agent loop and function tools

**Libraries:** OpenAI Agents SDK

Defines a support agent, registers a typed order tool, and executes it with Runner.

**Arguments:** `--ticket TEXT [--model MODEL] [--dry-run] [--output PATH]`

**Execution:** Remote unless dry-run.

Run `python examples/library-companions/07_openai_agents_sdk_support.py --help` for the generated CLI reference.

### `08_langgraph_stateful_workflow.py` — Stateful graph workflow

**Libraries:** LangGraph

Demonstrates typed graph state, conditional edges, checkpointing, and thread identity.

**Arguments:** `--request TEXT [--max-revisions INT] [--dry-run] [--output PATH]`

**Execution:** Remote unless dry-run.

Run `python examples/library-companions/08_langgraph_stateful_workflow.py --help` for the generated CLI reference.

### `09_crewai_research_crew.py` — Role-based research crew

**Libraries:** CrewAI

Defines researcher, writer, and reviewer roles with explicit task handoffs.

**Arguments:** `--topic TEXT [--model MODEL] [--dry-run] [--output PATH]`

**Execution:** Remote unless dry-run.

Run `python examples/library-companions/09_crewai_research_crew.py --help` for the generated CLI reference.

### `10_autogen_review_team.py` — Conversational multi-agent review

**Libraries:** AutoGen AgentChat

Builds a bounded team with specialist messages and a termination condition.

**Arguments:** `--task TEXT [--model MODEL] [--max-turns INT] [--dry-run] [--output PATH]`

**Execution:** Remote unless dry-run.

Run `python examples/library-companions/10_autogen_review_team.py --help` for the generated CLI reference.

### `11_langchain_dynamic_tools.py` — Dynamic tool routing

**Libraries:** LangChain

Creates tools and an agent that selects capabilities at runtime.

**Arguments:** `--request TEXT [--model MODEL] [--dry-run] [--output PATH]`

**Execution:** Remote unless dry-run.

Run `python examples/library-companions/11_langchain_dynamic_tools.py --help` for the generated CLI reference.

### `12_dspy_classifier.py` — Declarative prompting and optimization surface

**Libraries:** DSPy

Defines a typed signature/module rather than assembling a prompt string manually.

**Arguments:** `--ticket TEXT [--model MODEL] [--dry-run] [--output PATH]`

**Execution:** Remote unless dry-run.

Run `python examples/library-companions/12_dspy_classifier.py --help` for the generated CLI reference.

### `13_mcp_server.py` — Tool/resource server

**Libraries:** MCP Python SDK

Exposes a bounded capability through an MCP server contract.

**Arguments:** `[--transport stdio|streamable-http] [--host HOST] [--port INT]`

**Execution:** Starts a local server.

Run `python examples/library-companions/13_mcp_server.py --help` for the generated CLI reference.

### `14_a2a_client.py` — Remote agent discovery and delegation

**Libraries:** A2A SDK + HTTPX

Discovers an Agent Card and sends a task/message to a remote agent endpoint.

**Arguments:** `--agent-url URL --message TEXT [--timeout FLOAT] [--dry-run] [--output PATH]`

**Execution:** Remote unless dry-run.

Run `python examples/library-companions/14_a2a_client.py --help` for the generated CLI reference.

### `15_ragas_deepeval_eval.py` — RAG and answer-quality evaluation

**Libraries:** Ragas + DeepEval

Adapts a common dataset into representative evaluation-library calls.

**Arguments:** `--question TEXT --answer TEXT --context TEXT [--expected TEXT] [--framework ragas|deepeval|dry-run] [--output PATH]`

**Execution:** May call judge models unless dry-run.

Run `python examples/library-companions/15_ragas_deepeval_eval.py --help` for the generated CLI reference.

### `16_phoenix_opentelemetry_trace.py` — Agent trace export

**Libraries:** OpenTelemetry / Phoenix-compatible tracing

Creates nested workflow, retrieval, and tool spans with semantic attributes.

**Arguments:** `[--endpoint URL] [--service NAME] [--dry-run] [--output PATH]`

**Execution:** Exports to configured endpoint unless dry-run.

Run `python examples/library-companions/16_phoenix_opentelemetry_trace.py --help` for the generated CLI reference.

### `17_fastapi_agent_service.py` — Typed agent-facing HTTP service

**Libraries:** FastAPI + Uvicorn + Pydantic

Exposes health and triage endpoints with request/response validation.

**Arguments:** `[--host HOST] [--port INT] [--reload]`

**Execution:** Starts a local web server.

Run `python examples/library-companions/17_fastapi_agent_service.py --help` for the generated CLI reference.

### `18_pandas_product_experiment.py` — AI product experiment analysis

**Libraries:** pandas + SciPy

Aggregates product metrics, runs a contingency test, and applies a release rule.

**Arguments:** `--data PATH --baseline NAME --candidate NAME [--max-latency-increase-pct FLOAT] [--output PATH]`

**Execution:** Local.

Run `python examples/library-companions/18_pandas_product_experiment.py --help` for the generated CLI reference.

### `19_google_adk_agent.py` — Function-tool agent

**Libraries:** Google ADK

Defines an ADK agent and tool; dry-run emits its configuration.

**Arguments:** `--request TEXT [--model MODEL] [--dry-run] [--output PATH]`

**Execution:** Remote unless dry-run.

Run `python examples/library-companions/19_google_adk_agent.py --help` for the generated CLI reference.

### `20_semantic_kernel_agent.py` — Plugin-based agent

**Libraries:** Semantic Kernel

Registers a kernel plugin and invokes a chat-completion agent.

**Arguments:** `--request TEXT [--deployment MODEL] [--dry-run] [--output PATH]`

**Execution:** Remote unless dry-run.

Run `python examples/library-companions/20_semantic_kernel_agent.py --help` for the generated CLI reference.

### `21_chromadb_rag.py` — Persistent vector retrieval

**Libraries:** ChromaDB

Upserts documents into a persistent collection and returns nearest matches.

**Arguments:** `--documents PATH --query TEXT [--persist-dir PATH] [--collection NAME] [--top-k INT] [--output PATH]`

**Execution:** Local; embedding function may download model.

Run `python examples/library-companions/21_chromadb_rag.py --help` for the generated CLI reference.

### `22_pydantic_context_contracts.py` — Context-contract validation

**Libraries:** Pydantic

Validates evidence and budget constraints and emits JSON Schema.

**Arguments:** `--input PATH [--schema PATH] [--output PATH]`

**Execution:** Local.

Run `python examples/library-companions/22_pydantic_context_contracts.py --help` for the generated CLI reference.

## Chapter-to-code map

The canonical machine-readable map is [`chapter_code_map.csv`](chapter_code_map.csv). The table below makes it readable in Markdown.

| Ch. | Topic | Code pack | Library companion(s) | Python libraries | Scenario implementation |
|---:|---|---|---|---|---|
| 1 | [AI Foundations: From Rules to Agents](../01-foundations/01-ai-foundations-from-rules-to-agents.md) | Foundations and ML | [`01_sklearn_ticket_classifier.py`](../examples/library-companions/01_sklearn_ticket_classifier.py) | `numpy; pandas; scikit-learn; pydantic` | [`examples/01-ai-foundations`](../examples/01-ai-foundations) |
| 2 | [Machine Learning Fundamentals](../01-foundations/02-machine-learning-fundamentals.md) | Foundations and ML | [`01_sklearn_ticket_classifier.py`](../examples/library-companions/01_sklearn_ticket_classifier.py) | `numpy; pandas; scikit-learn; pydantic` | [`examples/02-machine-learning`](../examples/02-machine-learning) |
| 3 | [Deep Learning and Representation Learning](../01-foundations/03-deep-learning-and-representation-learning.md) | Deep learning | [`02_torch_mlp_classifier.py`](../examples/library-companions/02_torch_mlp_classifier.py) | `torch; numpy` | [`examples/03-deep-learning`](../examples/03-deep-learning) |
| 4 | [Transformers and Attention](../01-foundations/04-transformers-and-attention.md) | Transformers and LLMs | [`03_transformers_generation.py`](../examples/library-companions/03_transformers_generation.py) | `transformers; torch; openai` | [`examples/04-transformers`](../examples/04-transformers) |
| 5 | [Large Language Models](../01-foundations/05-large-language-models.md) | Transformers and LLMs | [`03_transformers_generation.py`](../examples/library-companions/03_transformers_generation.py) | `transformers; torch; openai` | [`examples/05-large-language-models`](../examples/05-large-language-models) |
| 6 | [Prompt Engineering Fundamentals](../02-prompt-engineering/01-prompt-engineering-fundamentals.md) | Prompting and optimization | [`04_openai_structured_output.py`](../examples/library-companions/04_openai_structured_output.py)<br>[`12_dspy_classifier.py`](../examples/library-companions/12_dspy_classifier.py) | `openai; pydantic; dspy` | [`examples/06-prompt-engineering`](../examples/06-prompt-engineering) |
| 7 | [Retrieval-Augmented Generation and Retrieval Fundamentals](../03-rag/01-rag-and-retrieval-fundamentals.md) | RAG and retrieval | [`05_sentence_transformers_faiss_rag.py`](../examples/library-companions/05_sentence_transformers_faiss_rag.py)<br>[`06_llamaindex_rag.py`](../examples/library-companions/06_llamaindex_rag.py)<br>[`21_chromadb_rag.py`](../examples/library-companions/21_chromadb_rag.py) | `sentence-transformers; faiss-cpu; chromadb; llama-index` | [`examples/07-rag`](../examples/07-rag) |
| 8 | [Embeddings and Vector Search](../03-rag/02-embeddings-and-vector-search.md) | RAG and retrieval | [`05_sentence_transformers_faiss_rag.py`](../examples/library-companions/05_sentence_transformers_faiss_rag.py)<br>[`06_llamaindex_rag.py`](../examples/library-companions/06_llamaindex_rag.py)<br>[`21_chromadb_rag.py`](../examples/library-companions/21_chromadb_rag.py) | `sentence-transformers; faiss-cpu; chromadb; llama-index` | [`examples/08-embeddings-vector-search`](../examples/08-embeddings-vector-search) |
| 9 | [Chunking, Reranking, and Retrieval Quality](../03-rag/03-chunking-reranking-and-retrieval-quality.md) | RAG and retrieval | [`05_sentence_transformers_faiss_rag.py`](../examples/library-companions/05_sentence_transformers_faiss_rag.py)<br>[`06_llamaindex_rag.py`](../examples/library-companions/06_llamaindex_rag.py)<br>[`21_chromadb_rag.py`](../examples/library-companions/21_chromadb_rag.py) | `sentence-transformers; faiss-cpu; chromadb; llama-index` | [`examples/09-retrieval-quality`](../examples/09-retrieval-quality) |
| 10 | [Advanced and Agentic RAG](../03-rag/04-advanced-and-agentic-rag.md) | RAG and retrieval | [`05_sentence_transformers_faiss_rag.py`](../examples/library-companions/05_sentence_transformers_faiss_rag.py)<br>[`06_llamaindex_rag.py`](../examples/library-companions/06_llamaindex_rag.py)<br>[`21_chromadb_rag.py`](../examples/library-companions/21_chromadb_rag.py) | `sentence-transformers; faiss-cpu; chromadb; llama-index` | [`examples/10-agentic-rag`](../examples/10-agentic-rag) |
| 11 | [AI Agent Fundamentals and the Execution Loop](../04-agents/01-agent-fundamentals-and-execution-loop.md) | Agent fundamentals | [`07_openai_agents_sdk_support.py`](../examples/library-companions/07_openai_agents_sdk_support.py)<br>[`22_pydantic_context_contracts.py`](../examples/library-companions/22_pydantic_context_contracts.py) | `openai-agents; pydantic` | [`examples/11-agent-fundamentals`](../examples/11-agent-fundamentals) |
| 12 | [Tool Calling and Action Execution](../04-agents/02-tool-calling-and-action-execution.md) | Agent fundamentals | [`07_openai_agents_sdk_support.py`](../examples/library-companions/07_openai_agents_sdk_support.py)<br>[`22_pydantic_context_contracts.py`](../examples/library-companions/22_pydantic_context_contracts.py) | `openai-agents; pydantic` | [`examples/12-tool-calling`](../examples/12-tool-calling) |
| 13 | [Reflection, Evaluation, and Replanning](../04-agents/03-reflection-evaluation-and-replanning.md) | Agent fundamentals | [`07_openai_agents_sdk_support.py`](../examples/library-companions/07_openai_agents_sdk_support.py)<br>[`22_pydantic_context_contracts.py`](../examples/library-companions/22_pydantic_context_contracts.py) | `openai-agents; pydantic` | [`examples/13-reflection-replanning`](../examples/13-reflection-replanning) |
| 14 | [Memory and Persistent State](../04-agents/04-memory-and-persistent-state.md) | Agent fundamentals | [`07_openai_agents_sdk_support.py`](../examples/library-companions/07_openai_agents_sdk_support.py)<br>[`22_pydantic_context_contracts.py`](../examples/library-companions/22_pydantic_context_contracts.py) | `openai-agents; pydantic` | [`examples/14-memory-state`](../examples/14-memory-state) |
| 15 | [LangGraph and Stateful Graph Workflows](../05-frameworks/01-langgraph-and-stateful-graph-workflows.md) | LangGraph | [`08_langgraph_stateful_workflow.py`](../examples/library-companions/08_langgraph_stateful_workflow.py) | `langgraph; pydantic` | [`examples/15-langgraph`](../examples/15-langgraph) |
| 16 | [CrewAI and Role-Based Multi-Agent Systems](../05-frameworks/02-crewai-role-based-multi-agent-systems.md) | CrewAI | [`09_crewai_research_crew.py`](../examples/library-companions/09_crewai_research_crew.py) | `crewai` | [`examples/16-crewai`](../examples/16-crewai) |
| 17 | [AutoGen and Conversational Multi-Agent Systems](../05-frameworks/03-autogen-conversational-multi-agent-systems.md) | AutoGen | [`10_autogen_review_team.py`](../examples/library-companions/10_autogen_review_team.py) | `autogen-agentchat; autogen-ext` | [`examples/17-autogen`](../examples/17-autogen) |
| 18 | [LangChain Agents and Dynamic Tool Routing](../05-frameworks/04-langchain-agents-and-dynamic-tool-routing.md) | LangChain | [`11_langchain_dynamic_tools.py`](../examples/library-companions/11_langchain_dynamic_tools.py) | `langchain; langchain-openai` | [`examples/18-langchain`](../examples/18-langchain) |
| 19 | [Orchestration, Routing, and Shared State](../05-frameworks/05-orchestration-routing-and-shared-state.md) | Orchestration and multi-agent | [`08_langgraph_stateful_workflow.py`](../examples/library-companions/08_langgraph_stateful_workflow.py)<br>[`10_autogen_review_team.py`](../examples/library-companions/10_autogen_review_team.py)<br>[`25_networkx_agent_graph_analysis.py`](../examples/library-companions/25_networkx_agent_graph_analysis.py) | `langgraph; autogen-agentchat; networkx` | [`examples/19-orchestration`](../examples/19-orchestration) |
| 20 | [Manager-Worker and Planner-Executor-Reviewer Patterns](../06-multi-agent/01-manager-worker-and-planner-executor-reviewer.md) | Orchestration and multi-agent | [`08_langgraph_stateful_workflow.py`](../examples/library-companions/08_langgraph_stateful_workflow.py)<br>[`10_autogen_review_team.py`](../examples/library-companions/10_autogen_review_team.py)<br>[`25_networkx_agent_graph_analysis.py`](../examples/library-companions/25_networkx_agent_graph_analysis.py) | `langgraph; autogen-agentchat; networkx` | [`examples/20-multi-agent-patterns`](../examples/20-multi-agent-patterns) |
| 21 | [Debate, Critique, and Hierarchical Multi-Agent Patterns](../06-multi-agent/02-debate-critique-and-hierarchical-patterns.md) | Orchestration and multi-agent | [`08_langgraph_stateful_workflow.py`](../examples/library-companions/08_langgraph_stateful_workflow.py)<br>[`10_autogen_review_team.py`](../examples/library-companions/10_autogen_review_team.py)<br>[`25_networkx_agent_graph_analysis.py`](../examples/library-companions/25_networkx_agent_graph_analysis.py) | `langgraph; autogen-agentchat; networkx` | [`examples/21-debate-hierarchy`](../examples/21-debate-hierarchy) |
| 22 | [Multi-Agent Failure Modes and Reliability Controls](../06-multi-agent/03-multi-agent-failure-modes-and-reliability-controls.md) | Orchestration and multi-agent | [`08_langgraph_stateful_workflow.py`](../examples/library-companions/08_langgraph_stateful_workflow.py)<br>[`10_autogen_review_team.py`](../examples/library-companions/10_autogen_review_team.py)<br>[`25_networkx_agent_graph_analysis.py`](../examples/library-companions/25_networkx_agent_graph_analysis.py) | `langgraph; autogen-agentchat; networkx` | [`examples/22-multi-agent-reliability`](../examples/22-multi-agent-reliability) |
| 23 | [Guardrails, Human Overrides, and Safe Agent Control](../07-control-safety/01-guardrails-human-overrides-and-safe-agent-control.md) | Safety and evaluation | [`15_ragas_deepeval_eval.py`](../examples/library-companions/15_ragas_deepeval_eval.py)<br>[`16_phoenix_opentelemetry_trace.py`](../examples/library-companions/16_phoenix_opentelemetry_trace.py) | `pydantic; ragas; deepeval; opentelemetry` | [`examples/23-guardrails-control`](../examples/23-guardrails-control) |
| 24 | [Evaluation and Responsible AI](../07-control-safety/02-evaluation-and-responsible-ai.md) | Safety and evaluation | [`15_ragas_deepeval_eval.py`](../examples/library-companions/15_ragas_deepeval_eval.py)<br>[`16_phoenix_opentelemetry_trace.py`](../examples/library-companions/16_phoenix_opentelemetry_trace.py) | `pydantic; ragas; deepeval; opentelemetry` | [`examples/24-evaluation-responsible-ai`](../examples/24-evaluation-responsible-ai) |
| 25 | [Explainability, Bias, and Fairness](../07-control-safety/03-explainability-bias-and-fairness.md) | Safety and evaluation | [`15_ragas_deepeval_eval.py`](../examples/library-companions/15_ragas_deepeval_eval.py)<br>[`16_phoenix_opentelemetry_trace.py`](../examples/library-companions/16_phoenix_opentelemetry_trace.py) | `pydantic; ragas; deepeval; opentelemetry` | [`examples/25-explainability-fairness`](../examples/25-explainability-fairness) |
| 26 | [AI Security and Threat Modeling](../07-control-safety/04-ai-security-and-threat-modeling.md) | Safety and evaluation | [`15_ragas_deepeval_eval.py`](../examples/library-companions/15_ragas_deepeval_eval.py)<br>[`16_phoenix_opentelemetry_trace.py`](../examples/library-companions/16_phoenix_opentelemetry_trace.py) | `pydantic; ragas; deepeval; opentelemetry` | [`examples/26-ai-security-threat-modeling`](../examples/26-ai-security-threat-modeling) |
| 27 | [Application Layer and Agent UX](../08-ux-performance/01-application-layer-and-agent-ux.md) | UX performance and operations | [`17_fastapi_agent_service.py`](../examples/library-companions/17_fastapi_agent_service.py)<br>[`16_phoenix_opentelemetry_trace.py`](../examples/library-companions/16_phoenix_opentelemetry_trace.py) | `fastapi; pydantic; opentelemetry` | [`examples/27-agent-ux`](../examples/27-agent-ux) |
| 28 | [Latency, Cost, and Performance Optimization](../08-ux-performance/02-latency-cost-and-performance-optimization.md) | UX performance and operations | [`17_fastapi_agent_service.py`](../examples/library-companions/17_fastapi_agent_service.py)<br>[`16_phoenix_opentelemetry_trace.py`](../examples/library-companions/16_phoenix_opentelemetry_trace.py) | `fastapi; pydantic; opentelemetry` | [`examples/28-performance-optimization`](../examples/28-performance-optimization) |
| 29 | [Production Observability and Operations](../08-ux-performance/03-production-observability-and-operations.md) | UX performance and operations | [`17_fastapi_agent_service.py`](../examples/library-companions/17_fastapi_agent_service.py)<br>[`16_phoenix_opentelemetry_trace.py`](../examples/library-companions/16_phoenix_opentelemetry_trace.py) | `fastapi; pydantic; opentelemetry` | [`examples/29-production-observability`](../examples/29-production-observability) |
| 30 | [AI-Native Product Management](../09-product-management/01-ai-native-product-management.md) | AI product management | [`18_pandas_product_experiment.py`](../examples/library-companions/18_pandas_product_experiment.py) | `pandas; scipy; pydantic` | [`examples/30-ai-native-product-management`](../examples/30-ai-native-product-management) |
| 31 | [End-to-End Support Triage Agent Project](../10-projects/01-end-to-end-support-triage-agent-project.md) | End-to-end projects | [`17_fastapi_agent_service.py`](../examples/library-companions/17_fastapi_agent_service.py)<br>[`07_openai_agents_sdk_support.py`](../examples/library-companions/07_openai_agents_sdk_support.py) | `fastapi; openai-agents; pydantic` | [`examples/31-support-triage-agent`](../examples/31-support-triage-agent) |
| 32 | [End-to-End Supplier Recommendation Agent Project](../10-projects/02-end-to-end-supplier-recommendation-agent-project.md) | End-to-end projects | [`17_fastapi_agent_service.py`](../examples/library-companions/17_fastapi_agent_service.py)<br>[`07_openai_agents_sdk_support.py`](../examples/library-companions/07_openai_agents_sdk_support.py) | `fastapi; openai-agents; pydantic` | [`examples/32-supplier-recommendation-agent`](../examples/32-supplier-recommendation-agent) |
| 33 | [End-to-End Project Coordination Agent Project](../10-projects/03-end-to-end-project-coordination-agent-project.md) | End-to-end projects | [`17_fastapi_agent_service.py`](../examples/library-companions/17_fastapi_agent_service.py)<br>[`07_openai_agents_sdk_support.py`](../examples/library-companions/07_openai_agents_sdk_support.py) | `fastapi; openai-agents; pydantic` | [`examples/33-project-coordination-agent`](../examples/33-project-coordination-agent) |
| 34 | [End-to-End Competitive Research System](../10-projects/04-end-to-end-competitive-research-system.md) | End-to-end projects | [`17_fastapi_agent_service.py`](../examples/library-companions/17_fastapi_agent_service.py)<br>[`07_openai_agents_sdk_support.py`](../examples/library-companions/07_openai_agents_sdk_support.py) | `fastapi; openai-agents; pydantic` | [`examples/34-competitive-research-system`](../examples/34-competitive-research-system) |
| 35 | [Agentic AI Interview Guide and Architecture Exercises](../11-interview-guide/01-interview-guide-and-architecture-exercises.md) | Interview and architecture | [`22_pydantic_context_contracts.py`](../examples/library-companions/22_pydantic_context_contracts.py)<br>[`24_typer_rich_architecture_cli.py`](../examples/library-companions/24_typer_rich_architecture_cli.py) | `pydantic; rich; typer` | [`examples/35-interview-architecture`](../examples/35-interview-architecture) |
| 36 | [Advanced Prompting and Reasoning Patterns](../02-prompt-engineering/02-advanced-prompting-and-reasoning-patterns.md) | Prompting and optimization | [`04_openai_structured_output.py`](../examples/library-companions/04_openai_structured_output.py)<br>[`12_dspy_classifier.py`](../examples/library-companions/12_dspy_classifier.py) | `openai; pydantic; dspy` | [`examples/36-advanced-prompting`](../examples/36-advanced-prompting) |
| 37 | [Prompt Evaluation and Optimization](../02-prompt-engineering/03-prompt-evaluation-and-optimization.md) | Prompting and optimization | [`04_openai_structured_output.py`](../examples/library-companions/04_openai_structured_output.py)<br>[`12_dspy_classifier.py`](../examples/library-companions/12_dspy_classifier.py) | `openai; pydantic; dspy` | [`examples/37-prompt-evaluation`](../examples/37-prompt-evaluation) |
| 38 | [AI Product Discovery and Prioritization](../09-product-management/02-ai-product-discovery-and-prioritization.md) | AI product management | [`18_pandas_product_experiment.py`](../examples/library-companions/18_pandas_product_experiment.py) | `pandas; scipy; pydantic` | [`examples/38-product-discovery-prioritization`](../examples/38-product-discovery-prioritization) |
| 39 | [AI Product Experimentation and Optimization](../09-product-management/03-ai-product-experimentation-and-optimization.md) | AI product management | [`18_pandas_product_experiment.py`](../examples/library-companions/18_pandas_product_experiment.py) | `pandas; scipy; pydantic` | [`examples/39-product-experimentation`](../examples/39-product-experimentation) |
| 40 | [MCP and Agent-to-Agent Interoperability](../12-interoperability/01-mcp-and-agent-to-agent-interoperability.md) | Interoperability | [`13_mcp_server.py`](../examples/library-companions/13_mcp_server.py)<br>[`14_a2a_client.py`](../examples/library-companions/14_a2a_client.py) | `mcp; a2a-sdk; httpx` | [`examples/40-mcp-a2a`](../examples/40-mcp-a2a) |
| 41 | [Modern Agent SDKs and Programming Frameworks](../12-interoperability/02-modern-agent-sdks-and-programming-frameworks.md) | Modern SDKs | [`07_openai_agents_sdk_support.py`](../examples/library-companions/07_openai_agents_sdk_support.py)<br>[`19_google_adk_agent.py`](../examples/library-companions/19_google_adk_agent.py)<br>[`20_semantic_kernel_agent.py`](../examples/library-companions/20_semantic_kernel_agent.py)<br>[`12_dspy_classifier.py`](../examples/library-companions/12_dspy_classifier.py) | `openai-agents; google-adk; semantic-kernel; dspy` | [`examples/41-modern-agent-sdks`](../examples/41-modern-agent-sdks) |
| 42 | [Evaluation and Observability Frameworks](../13-evaluation-observability/01-evaluation-and-observability-frameworks.md) | Evaluation platforms | [`15_ragas_deepeval_eval.py`](../examples/library-companions/15_ragas_deepeval_eval.py)<br>[`16_phoenix_opentelemetry_trace.py`](../examples/library-companions/16_phoenix_opentelemetry_trace.py) | `ragas; deepeval; opentelemetry` | [`examples/42-evaluation-observability`](../examples/42-evaluation-observability) |
| 43 | [Workflow Automation and Production Deployment with n8n, FastAPI, Docker, and CI/CD](../14-production-deployment/01-workflow-automation-and-production-deployment.md) | Deployment | [`17_fastapi_agent_service.py`](../examples/library-companions/17_fastapi_agent_service.py) | `fastapi; uvicorn; pydantic; httpx` | [`examples/43-production-deployment`](../examples/43-production-deployment) |
| 44 | [Context Engineering: Designing the Information Environment](../15-engineering-disciplines/01-context-engineering.md) | Context engineering | [`22_pydantic_context_contracts.py`](../examples/library-companions/22_pydantic_context_contracts.py)<br>[`context_budget_cli.py`](../examples/44-context-engineering/context_budget_cli.py)<br>[`23_tiktoken_context_estimator.py`](../examples/library-companions/23_tiktoken_context_estimator.py) | `pydantic; tiktoken` | [`examples/44-context-engineering`](../examples/44-context-engineering) |
| 45 | [Context Operations: Retrieval, Memory, Compression, and Routing](../15-engineering-disciplines/02-context-operations-retrieval-memory-compression.md) | Context operations | [`05_sentence_transformers_faiss_rag.py`](../examples/library-companions/05_sentence_transformers_faiss_rag.py)<br>[`context_pipeline_cli.py`](../examples/45-context-operations/context_pipeline_cli.py) | `scikit-learn; numpy; sentence-transformers; faiss-cpu` | [`examples/45-context-operations`](../examples/45-context-operations) |
| 46 | [Agent Harness Engineering](../15-engineering-disciplines/03-agent-harness-engineering.md) | Harness engineering | [`07_openai_agents_sdk_support.py`](../examples/library-companions/07_openai_agents_sdk_support.py)<br>[`harness_runtime_cli.py`](../examples/46-harness-engineering/harness_runtime_cli.py) | `pydantic; openai-agents; opentelemetry` | [`examples/46-harness-engineering`](../examples/46-harness-engineering) |
| 47 | [Agent Loop Engineering](../15-engineering-disciplines/04-agent-loop-engineering.md) | Loop engineering | [`08_langgraph_stateful_workflow.py`](../examples/library-companions/08_langgraph_stateful_workflow.py)<br>[`loop_controller_cli.py`](../examples/47-loop-engineering/loop_controller_cli.py)<br>[`25_networkx_agent_graph_analysis.py`](../examples/library-companions/25_networkx_agent_graph_analysis.py) | `langgraph; networkx; pydantic` | [`examples/47-loop-engineering`](../examples/47-loop-engineering) |
| 48 | [Future Development and Research Frontiers in Agentic AI](../16-future-directions/01-future-development-and-research-frontiers.md) | Future research portfolio | [`research_portfolio_cli.py`](../examples/48-future-directions/research_portfolio_cli.py) | `pandas; pydantic` | [`examples/48-future-directions`](../examples/48-future-directions) |

## Design conventions

- **Contracts first:** Pydantic models or dataclasses represent inputs, outputs, evidence, actions, and state.
- **Configuration through arguments:** scenario files, model IDs, budgets, endpoints, and output locations are CLI arguments rather than source edits.
- **Safe remote execution:** API keys come from environment variables; dry-run output reveals the planned contract without making a call.
- **Bounded loops:** retries, turns, tool calls, and budgets are explicit.
- **JSON output:** examples can be incorporated into CI, evaluation harnesses, or notebooks without scraping console prose.
- **Separation of concerns:** domain rules remain independent from framework adapters so a scenario can be ported between libraries.

## Environment and secret rules

Never commit API keys. Set provider credentials in the shell, secret manager, CI environment, or container secret. Model and endpoint names should remain configurable because provider catalogs and deployment identifiers change.

## Additional utility companions

### `23_tiktoken_context_estimator.py` — tokenizer-aware budgeting

**Libraries:** tiktoken

Counts serialized context with a selected tokenizer encoding and checks whether the input fits after reserving output capacity.

```bash
python examples/library-companions/23_tiktoken_context_estimator.py \
  --input examples/library-companions/context.json \
  --encoding cl100k_base \
  --limit 4096 \
  --reserve 800 \
  --output /tmp/token-report.json
```

### `24_typer_rich_architecture_cli.py` — developer-facing scenario CLI

**Libraries:** Typer and Rich

Demonstrates typed CLI arguments, validation, subcommands, and readable terminal scorecards for architecture practice.

```bash
python examples/library-companions/24_typer_rich_architecture_cli.py scenarios
python examples/library-companions/24_typer_rich_architecture_cli.py score \
  --scenario support-triage \
  --reliability 4 \
  --safety 5 \
  --observability 4 \
  --output /tmp/architecture-score.json
```

### `25_networkx_agent_graph_analysis.py` — workflow graph analysis

**Libraries:** NetworkX

Checks terminal reachability, cycles, dead ends, graph size, and whether an agent workflow is acyclic.

```bash
python examples/library-companions/25_networkx_agent_graph_analysis.py \
  --graph examples/library-companions/workflow_graph.json \
  --start planner \
  --terminal finish \
  --output /tmp/graph-report.json
```
