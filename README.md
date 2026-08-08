# Agentic AI Handbook

> From language models to production-ready agentic systems

## Purpose

This handbook converts the uploaded Agentic AI board into a structured, standalone learning resource. The board is the primary source for the original terminology, examples, diagrams, and learning sequence. Concise board material is expanded into full explanations, engineering patterns, scenarios, and executable examples.

Sections marked **Supplementary** add implementation guidance or research material beyond the board.

## Intended audience

- AI, GenAI, and ML engineers
- Software engineers and solution architects
- Product managers building AI-enabled products
- Technical leaders evaluating agentic systems
- Learners progressing from LLM fundamentals to production architecture

## Current milestone

The content-expansion milestone is complete:

- 48 chapters across foundations, prompting, RAG, agents, frameworks, multi-agent systems, safety, UX, performance, product management, projects, interoperability, evaluation, deployment, context engineering, harness engineering, loop engineering, and future research.
- A chapter-specific scenario implementation for every topic.
- Reusable Python library companions covering classical ML, PyTorch, Transformers, OpenAI SDKs, RAG libraries, agent frameworks, MCP, A2A, evaluation, observability, APIs, and product analytics.
- CLI arguments, scenario inputs, requirements packs, dry-run modes, and machine-readable output conventions.
- A machine-readable chapter-to-code map and a 48-topic scenario runner.

The next milestone is the final editorial, cheat-sheet, combined-Markdown, repository-validation, and publication-packaging pass.

## Start here

1. [Browse the complete table of contents](SUMMARY.md).
2. [Read the Python library guide and chapter map](15-code-companions/01-python-library-guide-and-topic-map.md).
3. [Browse the scenario catalog](15-code-companions/03-scenario-based-code-catalog.md).
4. Run `python examples/scenario-runner/run_scenario.py --list`.
5. Begin with [Chapter 1](01-foundations/01-ai-foundations-from-rules-to-agents.md) or jump directly to [Context Engineering](15-engineering-disciplines/01-context-engineering.md).

## Repository structure

```text
01-foundations/              AI, ML, deep learning, transformers, LLMs
02-prompt-engineering/       prompting, reasoning patterns, optimization
03-rag/                      retrieval, embeddings, reranking, agentic RAG
04-agents/                   execution loops, tools, reflection, memory
05-frameworks/               LangGraph, CrewAI, AutoGen, LangChain, orchestration
06-multi-agent/              collaboration patterns and reliability
07-control-safety/           guardrails, evaluation, fairness, security
08-ux-performance/           application UX, latency, observability
09-product-management/       AI-native product practice and experiments
10-projects/                 end-to-end production scenarios
11-interview-guide/          architecture and interview practice
12-interoperability/         MCP, A2A, and modern SDKs
13-evaluation-observability/ evaluation and trace platforms
14-production-deployment/    FastAPI, n8n, Docker, CI/CD
15-engineering-disciplines/  context, harness, and loop engineering
16-future-directions/        research frontiers and adoption roadmap
15-code-companions/          library map, CLI guide, scenario catalog
examples/                    runnable chapter and library implementations
```

## Source convention

Board references use this form:

```text
[Board, p. 51]
```

This points to the corresponding page in the uploaded 51-page PDF export of the Miro board.

## Execution and safety conventions

- Create isolated virtual environments per requirements pack.
- Inspect every script with `--help`.
- Use `--dry-run` before remote provider calls where available.
- Supply secrets through environment variables or a secret manager.
- Keep writes idempotent and approval-gated.
- Treat sample connectors and datasets as learning artifacts, not production integrations.

## License and usage note

This repository is a learner-oriented transformation of user-provided material. Confirm organizational permissions before publishing externally.
