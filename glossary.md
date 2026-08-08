# Glossary

## Agent

A software system that uses a model to pursue a goal through one or more actions. An agent commonly combines instructions, planning, tool use, state, and control logic.

## Agentic AI

A system design approach in which AI models participate in multi-step, goal-directed workflows rather than producing only a single response.

## Artificial Intelligence (AI)

The broad field concerned with creating systems that perform tasks associated with intelligent behavior, such as perception, prediction, language processing, planning, and decision support.

## Context

Information supplied to a model for the current task. Context may include the user request, retrieved documents, tool observations, conversation state, policies, and examples.

## Deep Learning

A family of machine-learning methods based on multi-layer neural networks that learn useful representations from data.

## Foundation Model

A broadly trained model that can be adapted to many downstream tasks through prompting, retrieval, fine-tuning, or other techniques.

## Guardrail

A control that restricts, validates, or monitors model and agent behavior. Guardrails can operate on inputs, outputs, tool calls, state transitions, and policies.

## Large Language Model (LLM)

A model trained to process and generate language by predicting likely token sequences from context.

## Machine Learning (ML)

A branch of AI in which systems learn patterns from data rather than relying only on explicitly programmed rules.

## Memory

Information retained across steps or interactions. Agent memory can include current conversation state, prior decisions, user preferences, summaries, or retrieved knowledge.

## Model

A learned computational function that maps inputs to predictions, representations, or generated outputs.

## Orchestrator

A component that classifies requests, selects agents or tools, coordinates execution, manages shared state, and returns results.

## Prompt

The instructions and contextual information given to a language model.

## Retrieval-Augmented Generation (RAG)

An architecture that retrieves relevant external information and includes it in the model context before generation.

## Tool

An external capability an agent can invoke, such as a search service, database query, calculator, API, or code executor.

## Calibration

The degree to which predicted probabilities correspond to observed outcome frequencies.

## Classification

A supervised-learning task that predicts one category from a defined set of categories.

## Concept Drift

A change in the relationship between model inputs and the outcome the model is intended to predict.

## Data Drift

A change in the statistical distribution of model inputs after deployment.

## Data Leakage

The accidental use of information during training or evaluation that would not be available when a real prediction is made.

## Feature

An input variable or learned representation supplied to a model.

## Label

The known target outcome associated with a training or evaluation example.

## Overfitting

A condition in which a model learns training-specific noise or accidental patterns and performs worse on new data.

## Precision

The proportion of predicted-positive cases that are truly positive.

## Recall

The proportion of truly positive cases identified by the model.

## Regression

A supervised-learning task that predicts a continuous numeric value.

## Reinforcement Learning

A learning paradigm in which an agent selects actions in an environment and learns from rewards or penalties.

## Training

The process of estimating model parameters from data by reducing a loss function or otherwise improving an objective.

## Validation Set

A held-out dataset used for model selection, threshold tuning, and hyperparameter decisions.

## Activation Function

A nonlinear function applied to a neuron's weighted input. Activations such as ReLU, sigmoid, GELU, and softmax allow neural networks to represent complex relationships.

## Backpropagation

An efficient application of the chain rule that computes how each trainable parameter contributes to the model's loss.

## Batch

A group of training examples processed together before one optimization update.

## Convolutional Neural Network (CNN)

A neural-network architecture that uses local filters and shared weights to learn spatial patterns, especially in images and signals.

## Embedding

A learned vector representation of an item such as a word, document, image, product, or user. Embeddings are commonly used for similarity search, clustering, retrieval, and recommendation.

## Epoch

One pass through the training dataset.

## Fine-Tuning

The process of adapting a pretrained model by updating some or all of its parameters on a target dataset.

## Gradient

A set of derivatives indicating how a small change in each parameter would change the loss.

## Neural Network

A parameterized model composed of connected layers that transform inputs into predictions or learned representations.

## Optimizer

An algorithm that updates model parameters using gradients. Examples include stochastic gradient descent and Adam.

## Representation Learning

The automatic learning of useful internal features or embeddings from data rather than relying entirely on manually designed features.

## Residual Connection

A connection that adds a layer's input to its transformed output, helping information and gradients move through deep networks.

## Transfer Learning

The reuse of a model trained on one task or broad dataset as the starting point for another task.

## Attention

A learned mechanism that scores relationships between queries and keys, then uses the resulting weights to combine value vectors.

## Causal Mask

A visibility rule that prevents a sequence position from attending to future positions during autoregressive language-model training and generation.

## Cross-Attention

An attention operation in which queries come from one sequence while keys and values come from another sequence or modality.

## Key-Value Cache

Stored key and value tensors from previous autoregressive generation steps. The cache avoids recomputing the full prefix at every new token, trading memory for speed.

## Layer Normalization

A normalization operation applied across hidden features that helps stabilize optimization in deep neural networks.

## Multi-Head Attention

A transformer mechanism that runs several attention operations with different learned projections, concatenates their outputs, and applies an output projection.

## Positional Encoding

Information added to or incorporated into token representations so that a transformer can distinguish token order and relative position.

## Query, Key, and Value

The three learned representations used by attention. A query specifies what a position seeks, a key supports relevance matching, and a value carries the information to be combined.

## Self-Attention

An attention operation in which queries, keys, and values are derived from the same input sequence.

## Transformer

A neural-network architecture built from attention, feed-forward layers, normalization, and residual connections. Transformers are the foundation of most modern large language models.

## Autoregressive Generation

A generation process that predicts one token at a time, appends the selected token to the context, and repeats until a stop condition is reached.

## Base Model

A pretrained model before application-specific instruction tuning, preference optimization, or task adaptation.

## Context Window

The maximum tokenized input and output workspace available to a model for one request. It may contain instructions, messages, retrieved evidence, tool outputs, and reserved output tokens.

## Cross-Entropy Loss

A training objective that penalizes a model when it assigns low probability to the correct class or next token.

## Greedy Decoding

A decoding strategy that selects the highest-probability token at each generation step.

## Hallucination

An output that is fabricated, unsupported by authoritative evidence, or inconsistent with the relevant source material.

## In-Context Learning

The ability of a model to adapt its behavior from instructions and examples supplied in the current prompt without updating model parameters.

## Instruction Tuning

Additional training on instruction-response examples that helps a pretrained model behave more reliably as an assistant.

## Large Language Model (LLM)

A large neural language model, usually transformer-based, trained on broad text or code data to predict and generate token sequences.

## Logit

An unnormalized model score for a candidate output token or class before softmax converts scores into probabilities.

## Perplexity

A language-model evaluation measure derived from average negative log probability. Lower perplexity means the model assigned higher probability to the evaluated token sequence, within the limits of the dataset and tokenizer.

## Preference Optimization

A family of methods that adjusts model behavior using preferences between candidate responses or other feedback signals.

## Prompt Injection

An attack or failure mode in which untrusted input attempts to override intended instructions or redirect model behavior.

## Structured Output

Model output constrained to a defined schema or grammar, such as JSON or function arguments, for validation and downstream processing.

## Temperature

A decoding parameter that changes how concentrated or diffuse the next-token probability distribution is before sampling.

## Token

A discrete text unit produced by a tokenizer. A token may represent a word, part of a word, punctuation, whitespace pattern, byte sequence, or code symbol.

## Tokenization

The process of converting text or another modality into discrete token IDs that a model can process.

## Top-k Sampling

A decoding strategy that samples only from the k highest-probability candidate tokens.

## Top-p Sampling

A decoding strategy that samples from the smallest candidate set whose cumulative probability reaches a selected threshold p.

## Prompt Engineering

The discipline of designing, structuring, testing, and operating the instructions, context, examples, constraints, and output requirements supplied to a language model.

## Zero-Shot Prompting

Prompting that supplies a task instruction without a worked example.

## One-Shot Prompting

Prompting that supplies one worked example to clarify the desired task, label, style, or output format.

## Few-Shot Prompting

Prompting that supplies several representative examples so a model can infer the desired pattern in the current context.

## Prompt Template

A reusable prompt structure with placeholders for task-specific context, user input, evidence, constraints, and output requirements.

## Decomposition

The process of breaking a complex objective into smaller, observable subtasks that can be executed and evaluated separately.

## ReAct

A reasoning-and-action pattern in which an agent selects an action, receives an observation from a tool or environment, and uses that observation to decide the next step.

## Plan-and-Execute

An agent pattern that separates task planning from step execution, usually with persistent state, review, and replanning.

## Prompt Regression Test

A repeatable test that verifies a prompt or model change has not degraded previously acceptable behavior across a representative evaluation set.

## Trust Boundary

A boundary that separates instructions or data with different assurance levels, such as trusted system policy and untrusted user or retrieved content.

## Chunk

A retrievable unit of source content created during ingestion. A chunk should be focused enough to match a query and complete enough to support an answer.

## Chunking

The process of dividing source content into retrievable units while preserving useful structure, metadata, and source relationships.

## Citation Correctness

The degree to which a cited source actually supports the claim associated with that citation.

## Context Assembly

The process of selecting, ordering, deduplicating, labeling, and fitting retrieved evidence into the model's available context budget.

## Cosine Similarity

A vector-similarity measure based on the angle between two vectors. It is commonly used to rank query and document embeddings.

## Grounding

The requirement that generated claims be supported by the evidence or authoritative data supplied to the model.

## Hybrid Retrieval

A retrieval approach that combines lexical search, semantic vector search, metadata filtering, or other ranking signals.

## Index

A data structure that supports efficient retrieval over documents, chunks, fields, or vectors.

## Ingestion

The workflow that extracts, parses, normalizes, chunks, enriches, and indexes source content for later retrieval.

## Lexical Retrieval

Retrieval based on exact or weighted term matches between a query and indexed content.

## Metadata Filter

A constraint that limits retrieval candidates using fields such as product, region, status, date, language, tenant, or authorization group.

## Reranker

A model, rule set, or ranking stage that reorders an initial candidate set to place the most answer-bearing evidence first.

## Retrieval Recall

The proportion of relevant evidence found within the retrieved result set, often measured at a selected value of k.

## Retriever

A component that searches one or more indexes and returns candidate evidence for a query.

## Semantic Search

Retrieval based on vector representations intended to capture conceptual similarity rather than only exact term overlap.

## Top-k Retrieval

The selection of the k highest-ranked search results for subsequent filtering, reranking, or context assembly.

## Vector Database

A data system optimized to store vector representations and perform nearest-neighbor similarity search, often together with metadata filtering.

## Approximate Nearest Neighbor (ANN)

A search method that reduces vector-query cost by exploring only promising parts of an index, accepting a measurable chance of missing a true nearest neighbor.

## ANN Recall

The proportion of exact nearest neighbors retained by an approximate vector index for a given query set and search configuration.

## Bi-Encoder

A retrieval model that encodes the query and candidate passage independently so candidate vectors can be precomputed and searched efficiently.

## Content Hash

A deterministic fingerprint of content used to detect changes, duplicates, and whether re-embedding is required.

## Cosine Similarity

A vector-similarity measure based on the angle between two vectors. It emphasizes direction and is commonly used with normalized embeddings.

## Cross-Encoder

A model that processes a query and candidate together to produce a relevance score, commonly used to rerank a smaller retrieved candidate set.

## Dense Vector

A numeric representation in which most dimensions contain non-zero values, commonly produced by neural embedding models.

## Dot Product

The sum of element-wise products between two vectors. It measures alignment and is affected by vector magnitude unless vectors are normalized.

## Embedding

A numeric vector representation of text, images, audio, records, or other inputs in a learned feature space.

## Exact Nearest-Neighbor Search

A vector search that compares the query with every eligible stored vector and returns the true ranking for the selected metric.

## Feature Hashing

A technique that maps input features into a fixed-dimensional vector using a deterministic hash function, often without maintaining a vocabulary.

## Inverted-File Vector Index

An approximate vector-index family that partitions vectors into clusters and searches only the most promising clusters for a query.

## Late Interaction

A retrieval approach that independently encodes inputs but retains multiple token-level representations for richer query-document comparison after encoding.

## Maximum Marginal Relevance (MMR)

A selection method that balances query relevance with novelty to reduce redundant retrieval results.

## Mean Reciprocal Rank (MRR)

A retrieval metric that averages the reciprocal rank of the first relevant result across queries.

## Metadata Filter

A structured condition applied to search candidates, such as region, approval status, language, role, or effective date.

## Normalized Discounted Cumulative Gain (nDCG)

A ranked-retrieval metric that rewards highly relevant results near the top and supports graded relevance labels.

## Product Quantization

A vector-compression technique that represents subvectors with compact codes to reduce memory and search cost at the expense of approximation error.

## Sparse Vector

A vector in which most dimensions are zero, commonly used for lexical representations such as bag-of-words or TF-IDF.

## Vector Normalization

The process of scaling a vector, commonly to unit length, so similarity behavior matches the selected scoring contract.

## Answer-Bearing Evidence

A source span that contains enough information to directly support part or all of an answer, including relevant qualifiers, exceptions, and scope.

## Candidate Generation

The high-recall retrieval stage that finds a manageable set of potentially relevant items before more expensive filtering or reranking.

## Context Compression

The process of reducing retrieved content to query-relevant evidence while preserving traceability and factual support.

## Coverage-Aware Selection

A selection strategy that ensures the final evidence set addresses the distinct aspects or sub-questions in a complex request.

## Evidence Coverage

The proportion of required answer aspects for which the retrieved context contains supporting evidence.

## Fixed-Size Chunking

A chunking strategy that divides content using a fixed character, word, or token limit, usually with optional overlap.

## Parent-Child Retrieval

A retrieval pattern that searches small child chunks for precision and then expands a match to a larger parent section for complete context.

## Query Decomposition

The process of splitting a complex question into smaller retrieval questions whose evidence can later be combined.

## Query Rewriting

The transformation of a user question into a search-oriented expression while retaining the original request for answer generation.

## Reciprocal Rank Fusion (RRF)

A rank-combination method that merges several ranked result lists using reciprocal rank contributions rather than directly comparing incompatible raw scores.

## Retrieval Cascade

A staged search architecture that uses inexpensive high-recall retrieval first, followed by filtering, reranking, diversity selection, and context assembly.

## Semantic Chunking

A chunking method that creates boundaries using topic or embedding-similarity changes rather than only fixed length or document formatting.

## Sentence-Window Retrieval

A pattern that indexes individual sentences or small units but returns a bounded window of surrounding text when a match is selected.

## Structure-Aware Chunking

A chunking strategy that preserves meaningful document structures such as headings, clauses, procedures, code units, tables, or question-answer pairs.


## Agentic RAG

A retrieval-augmented generation architecture in which a bounded controller decides when and how to retrieve, selects sources or tools, evaluates evidence, replans when useful, and terminates with an answer, clarification, refusal, or escalation.

## Bounded Autonomy

A design approach that permits runtime model decisions only within explicit limits such as allowlisted actions, timeouts, call budgets, retry limits, approval thresholds, and deterministic policy guards.

## Control Plane

The part of an agentic system that decides what operation should happen next. It commonly performs classification, planning, routing, retry, stop, and escalation decisions.

## Data Plane

The part of an agentic system that executes retrieval and tool operations, such as vector search, keyword search, database queries, API calls, or graph traversals.

## Evidence Contract

A structured definition of the fields, source qualities, and acceptance rules required before a workflow step can be considered supported by evidence.

## Evidence Sufficiency

The condition in which retrieved evidence adequately covers the required answer aspects and satisfies authority, freshness, specificity, consistency, and authorization requirements.

## Multi-Hop Retrieval

A retrieval pattern in which the result of one lookup supplies information needed to formulate or route a subsequent lookup.

## Productive Replan

A revision to an execution plan that changes a meaningful variable and improves progress, such as adding a missing constraint, selecting a different source, or resolving a failed dependency.

## Retrieval State

Structured workflow data describing the retrieval trajectory, including queries, sources searched, evidence collected, rejected results, coverage, contradictions, errors, and remaining budgets.

## Terminal State

A valid workflow outcome after which execution stops. Examples include answered, clarified, partially answered, refused, cancelled, or escalated.

## Tool Contract

A typed specification describing an external capability, including its purpose, input schema, output schema, permissions, side effects, errors, and validation requirements.

## Trajectory Evaluation

The assessment of the sequence of planning, routing, retrieval, tool, retry, and escalation decisions taken by an agent, not only the quality of its final response.

## Action

A typed operation selected by an agent to advance a goal, such as calling a tool, asking a question, producing a draft, requesting approval, or terminating a workflow.

## Action Signature

A normalized representation of an action name and its arguments, used to detect duplicate or repeated actions in an execution loop.

## Agent Autonomy Level

The degree of operational freedom granted to an agent, ranging from answer-only behavior to recommendation, drafting, reversible execution, bounded workflow execution, or broad autonomous control.

## Completion Contract

An explicit set of conditions that must be satisfied before an agent can terminate successfully, such as required fields, evidence, approvals, policy checks, and side-effect confirmation.

## Execution Budget

A limit on agent activity, such as maximum steps, tool calls, retries, elapsed time, tokens, cost, or repeated no-progress actions.

## Human-in-the-Loop (HITL)

A control pattern in which a person reviews, approves, edits, rejects, pauses, or resumes an agent workflow at defined points.

## Idempotency

The property that repeating an operation with the same request identifier does not create an additional side effect. Idempotency is essential for safely retrying write actions.

## No-Progress Loop

An execution pattern in which an agent continues taking actions without reducing uncertainty, completing a subgoal, or changing relevant state.

## Observation

A structured representation of the result of an action, including status, normalized data, source, error category, retryability, freshness, and side-effect information.

## Tool Registry

A controlled catalog of tools available to an agent, including schemas, permissions, execution adapters, timeouts, error behavior, and approval requirements.

## Working State

Structured, task-scoped data that records an agent's current goal, plan, completed and pending steps, observations, errors, approvals, budgets, and completion status.

## Approval Binding

The practice of associating a human approval with the exact normalized tool name, arguments, workflow, approver, and validity period so that changed or expired actions cannot reuse the approval.

## Argument Validation

The process of checking model-generated tool parameters for schema correctness, business meaning, and policy compliance before execution.

## Compensation

A follow-up operation that attempts to counteract a previously completed side effect when a later workflow step fails. Compensation may restore business state without literally erasing the original action.

## Confirmation Read

A read operation performed after a critical write to verify that the external system reached the approved and expected state.

## Credential Broker

A service that issues short-lived, narrowly scoped credentials to a tool adapter after identity and policy checks, keeping long-lived secrets out of model context.

## Error Taxonomy

A stable classification of tool failures, such as validation, authorization, not found, conflict, rate limit, timeout, temporary unavailable, business rule, policy, and unknown.

## Execution Gateway

A controlled service between the agent and external tools that enforces validation, authorization, approval, timeouts, quotas, idempotency, retries, normalization, and audit logging.

## Least Privilege

The security principle of granting an identity or tool only the minimum permissions and access duration required to complete an authorized task.

## Reconciliation

The process of inspecting idempotency records, downstream operation status, or business state to determine whether an action occurred when the original execution result is uncertain.

## Side Effect

A change to external state caused by a tool call, such as creating a record, sending a message, changing a status, issuing a refund, or scheduling an event.

## Tool Adapter

Code that translates a stable agent-facing tool contract into the authentication, request, response, and error conventions of a particular external system.

## Tool Selection

The decision process that determines whether an external capability is required and, if so, which allowed tool best satisfies the current subgoal.

## Uncertain Outcome

A tool-call state in which the executor cannot determine whether a side effect occurred, commonly after a timeout or lost response during a write operation.

## Completion Gate

A non-negotiable validation condition that must pass before a workflow may continue or finalize, such as authorization, policy compliance, required evidence, or approval.

## Evaluator Drift

A change in model-based grading behavior caused by evaluator model, prompt, rubric, configuration, or distribution changes.

## Failure Classification

The process of assigning an observed problem to a stable category, such as transient infrastructure, invalid input, insufficient evidence, authorization, policy, no progress, or unknown failure, so that the correct recovery action can be selected.

## Model-Based Evaluator

A language-model component that grades semantic properties such as relevance, clarity, completeness, or instruction adherence against an explicit rubric and structured output contract.

## No-Progress Detection

A control that identifies repeated actions or iterations that do not add evidence, resolve requirements, reduce uncertainty, or change meaningful state.

## Outcome Evaluation

Assessment of whether the final deliverable and business result satisfy the user's goal, evidence requirements, policy, and quality thresholds.

## Recovery Controller

A control component that uses failure class, risk, budgets, and evaluator results to choose among continue, retry, fallback, replan, escalate, or stop.

## Reflection Record

A structured operational summary of an expected result, observed result, failure class, root cause, material change, expected improvement, and remaining risk.

## Replanning

The revision of a workflow strategy, ordering, source, tool, query, or decomposition after new information or a diagnosed failure. A productive replan changes a material variable.

## Reward Hacking

Behavior in which an agent optimizes an evaluator's measured score without improving the actual task outcome, safety, or business value.

## Step Evaluation

Assessment of whether an individual action was appropriate, permitted, correctly executed, and useful for its current subgoal.

## Agent State

The structured operational record of an agent workflow, including its goal, plan, progress, observations, permissions, approvals, budgets, errors, and completion status.

## Checkpoint

A durable workflow snapshot or event position containing enough state to resume execution safely after a pause, failure, approval wait, or worker restart.

## Conversation History

The ordered sequence of messages in an interaction. Conversation history can inform an agent but is not a substitute for typed workflow state.

## Episodic Memory

A retained representation of a notable past event or completed workflow, including its context, outcome, provenance, and limitations.

## Memory Compaction

The process of reducing detailed events, messages, or observations into a smaller representation while preserving critical facts, constraints, evidence references, approvals, and unresolved issues.

## Memory Namespace

An identity- and scope-derived boundary, such as tenant, user, project, workflow type, and memory type, used to isolate and authorize memory records.

## Memory Poisoning

The corruption of future agent behavior when untrusted, false, adversarial, or unsupported information is written into durable memory.

## Memory Supersession

A versioning pattern in which a new memory record replaces an older one while preserving the history and relationship between both records.

## Optimistic Concurrency

A consistency control that updates state only when its stored version still matches the version read by the worker, preventing silent overwrites from concurrent updates.

## Preference Memory

Durable, scoped, and correctable user-approved choices such as output format, language, timezone, or project defaults.

## Semantic Memory

Reusable facts, definitions, mappings, or conventions stored for future tasks, with provenance and authority information.

## Session Memory

Temporary interaction context retained for a session or thread, such as a conversation summary, unresolved references, and session-scoped preferences.

## Source of Truth

The authoritative external system responsible for a business fact, such as a CRM, payroll database, policy repository, or ticket tracker. Volatile facts should usually be refreshed from this system rather than remembered.

## State Transition

A validated change from one workflow status to another, such as planning to executing, executing to waiting for approval, or evaluating to completed.

## Time to Live (TTL)

A retention interval after which a memory, cache entry, session, or other stored record expires and should no longer be used without refresh.


## Conditional Edge

A graph route selected at runtime from explicit state or validated routing logic rather than a fixed transition.

## Graph Checkpointer

A persistence component that stores thread-scoped graph state at execution boundaries so a workflow can resume, support human review, or recover from failure.

## Graph Node

A bounded unit of work in a stateful workflow. A node reads current state and returns a partial state update.

## Graph Reducer

A rule that determines how a node update is merged into an existing state field, such as overwrite, append, deduplicate, or sum.

## Graph State

The typed shared data model carried through a graph, containing the facts and control fields needed by nodes and routes.

## Human-in-the-Loop Interrupt

A durable pause in graph execution that exposes a review or input request and resumes the same thread when an authorized response is supplied.

## Idempotent Node

A node designed so that repeating it with the same logical input does not create an unintended additional side effect.

## StateGraph

LangGraph's graph builder abstraction for workflows in which nodes communicate by reading and updating a shared state schema.

## Subgraph

A reusable graph embedded within a larger graph to isolate a responsibility, workflow, team boundary, or permission domain.

## Super-Step

A graph execution interval in which one or more scheduled nodes run, potentially in parallel, before their updates are used to schedule the next interval.

## Thread ID

The identifier used to associate checkpointed state with a continuing graph execution or conversation context.

## Trajectory Evaluation

Assessment of the sequence of routes, actions, tool calls, retries, approvals, and state changes used to reach a final result.

## CrewAI Agent

A role-configured specialist in CrewAI that performs tasks using an assigned goal, backstory, model, tools, permissions, and optional memory or delegation behavior.

## CrewAI Crew

A bounded collaborative unit that groups agents and tasks and executes them according to a selected process.

## CrewAI Flow

An event-driven application workflow that coordinates code, models, tools, and crews while managing typed state, routing, persistence, and human interaction.

## CrewAI Task

A specific assignment with a description, expected output, agent, context, tools, output contract, and optional guardrails or human review.

## Hierarchical Process

A CrewAI execution strategy in which a manager model or manager agent dynamically delegates work to specialists and validates completion.

## Role-Based Agent

An agent whose responsibility, goal, tools, permissions, inputs, and evaluation criteria are aligned to a recognizable specialist function.

## Sequential Process

A CrewAI execution strategy in which tasks run in a predefined order and earlier task outputs can provide context to later tasks.

## Structured Handoff

A typed or schema-validated artifact passed between agents or tasks instead of an unbounded natural-language transcript.


## AgentChat

AutoGen's high-level API for building conversational single-agent and multi-agent applications using preset agents, team patterns, termination conditions, state management, tools, and memory integrations.

## Agent Runtime

The AutoGen Core execution environment that manages agent identities, message delivery, lifecycle, and runtime services for standalone or distributed agent systems.

## AutoGen Core

The lower-level event-driven AutoGen framework for building custom agents and multi-agent applications using typed messages, routed agents, topics, and agent runtimes.

## AutoGen Studio

A low-code AutoGen interface for visually prototyping agents, tools, models, teams, termination conditions, and interactive sessions. It is a prototyping environment rather than a complete production application.

## Candidate Function

A function used by a selector-driven team to narrow the set of agents eligible to speak next before model-based selection occurs.

## Conversational Multi-Agent System

A system in which specialist agents coordinate by exchanging messages, selecting or handing off to the next participant, and converging on a shared task result.

## Handoff Message

An explicit message that transfers task ownership or control from one agent to another, ideally including the destination, reason, current state, evidence, and requested next action.

## Max-Message Termination

A hard safety boundary that stops a multi-agent run after a configured number of messages, even when semantic completion has not been reached.

## Model-Based Speaker Selection

A coordination method in which a language model chooses the next agent based on the conversation context and participant descriptions.

## Round-Robin Group Chat

An AutoGen AgentChat team pattern in which participants take turns in a fixed repeated order while sharing conversation context.

## Selector Group Chat

An AutoGen AgentChat team pattern in which a model or custom selector chooses the next speaker from eligible participants using shared conversation context.

## Speaker Selection Policy

The control logic that determines which participant may act next based on task state, capabilities, routing rules, safety constraints, and remaining budgets.

## Swarm

An AutoGen AgentChat team pattern that coordinates participants through explicit handoff messages rather than relying only on a centralized speaker selector.

## Text-Mention Termination

A semantic termination condition that stops a team when a configured text marker appears in an agent response.

## Agent Harness

The prompt, tools, middleware, context, state, policies, budgets, and runtime controls surrounding a model-driven action loop.

## Dynamic Tool Routing

A pattern in which a model selects one or more approved tools at runtime based on the request, current state, and prior observations.

## Hybrid Routing

An orchestration pattern in which deterministic code first constrains the business domain or available capabilities, after which an agent dynamically selects from the permitted subset.

## LangChain Agent

A configurable model-and-tool harness created with LangChain, typically using `create_agent`, that calls tools in a loop until it reaches a stopping condition.

## Middleware

Composable logic that intercepts or modifies agent execution around the agent, model, or tool lifecycle to add concerns such as retries, context management, guardrails, routing, and human approval.

## Provider Strategy

A structured-output strategy that uses a model provider's native schema-enforcement capability when the selected provider and model support it.

## Runtime Context

Trusted per-invocation data and dependencies, such as authenticated user identity, tenant, database connections, locale, or feature flags, injected into tools and middleware outside the natural-language prompt.

## Tool Strategy

A structured-output strategy that uses model tool calling to produce data conforming to a requested schema when provider-native structured output is unavailable or not selected.

## Tool Selection Accuracy

The proportion of evaluation cases in which an agent chooses an expected or allowed tool and avoids forbidden or unnecessary tools.

## ToolRuntime

The LangChain/LangGraph runtime interface available inside tools for accessing invocation context, long-term stores, execution identity, state, and custom streaming facilities.

## Manager-Worker Pattern

A multi-agent topology in which a coordinating manager decomposes an objective, assigns bounded work orders to specialist workers, tracks dependencies, and synthesizes the final result.

## Planner-Executor-Reviewer Pattern

A multi-agent topology that separates task planning, action execution, and independent acceptance review, usually with a bounded revision or escalation loop.

## Work Order

A typed delegation contract that identifies a work item, owner, inputs, deliverable, dependencies, permissions, acceptance criteria, and execution budget.

## Capability Registry

A structured catalog of available agents, tools, or services, including their supported task types, permissions, input and output contracts, costs, latency, and operational constraints.

## Merge Policy

Explicit rules for normalizing, deduplicating, reconciling, and synthesizing outputs from multiple workers while preserving evidence and provenance.

## Progress Proof

A measurable indication that another iteration has moved a workflow closer to completion, such as increased evidence coverage, fewer failed criteria, or a materially changed artifact.

## Circular Delegation

A failure mode in which agents repeatedly pass the same work to one another without ownership, progress, or a terminating condition.

## Final Decision Owner

The agent, deterministic service, or human role that has explicit responsibility for approving, publishing, escalating, or safely stopping the workflow outcome.

## Debate Pattern

A multi-agent coordination pattern in which independent participants present and challenge competing positions before a declared judge or decision owner selects, combines, escalates, or rejects them.

## Critique Contract

A typed record that identifies the target artifact or position, defect category, severity, evidence, affected criterion, and requested correction.

## Evidence Ledger

A shared provenance-aware catalog of evidence items, including source identity, authority, freshness, access scope, supported claims, conflicts, and usage by agents.

## Independent First Pass

A debate control in which agents form initial positions before seeing other agents' conclusions, reducing anchoring and premature consensus.

## False Consensus

A failure mode in which agents converge because they share models, prompts, evidence, or anchoring rather than because the evidence genuinely supports agreement.

## Performative Disagreement

A failure mode in which agents produce rhetorical opposition without adding new evidence, identifying a testable defect, or changing the decision state.

## Evidence Laundering

The transformation of an unsupported agent statement into apparently verified evidence when another agent repeats it without checking the original source.

## Model Judge

A language model assigned to compare candidate artifacts or positions against an explicit rubric and return a structured decision.

## Decision Record

A structured final artifact containing the selected position, rubric scores, unresolved issues, rationale, confidence, required next actions, and human-approval status.

## Hierarchical Multi-Agent System

A multi-agent topology in which a top-level orchestrator delegates domain outcomes to managers, who may create bounded work orders for specialist agents and return synthesized results upward.

## Delegation Depth

The number of manager-to-child handoff levels in a hierarchical workflow. Production systems normally impose a maximum depth to prevent unbounded delegation.

## Local Critique Gate

A domain-level review or debate step that validates specialist output before it is promoted to a higher-level manager or final judge.

## Debate Overhead

The additional latency, model calls, tokens, tool usage, cost, and coordination state introduced by deliberation relative to a simpler baseline.

## Critique Precision

The proportion of critique findings that correspond to genuine defects in the target artifact or position.

## Revision Value

The measurable improvement produced by revising an artifact in response to critique, such as increased correctness, evidence coverage, policy compliance, or task completion.

## Livelock

A failure state in which agents remain active and exchange messages or revisions, but the workflow makes no measurable progress toward its acceptance criteria.

## Deadlock

A failure state in which two or more agents, resources, or approval steps wait on one another and no valid transition can proceed.

## Retry Storm

A cascading failure in which multiple layers independently retry the same operation, multiplying tool calls, latency, cost, and the risk of duplicate side effects.

## Attempt Ledger

A workflow-level record of action attempts, failure classes, backoff decisions, retry counts, outcomes, and next allowed execution times.

## Idempotency Key

A stable identifier for a logical side-effecting action that allows duplicate requests to return the prior result rather than execute the effect again.

## Ambiguous Write Outcome

A condition in which a caller does not know whether an external write succeeded, commonly after a timeout or lost response, and must reconcile against the system of record before retrying.

## Circuit Breaker

A reliability control that temporarily blocks calls to a repeatedly failing dependency and later permits a limited probe to determine whether service has recovered.

## Bulkhead

A resource-isolation pattern that separates worker pools, queues, limits, or credentials so failure in one capability cannot exhaust the entire system.

## No-Progress Detector

A control that compares successive workflow states against a declared progress function and stops, replans, or escalates when improvement remains below threshold.

## Fault Injection

The deliberate introduction of controlled failures such as timeouts, stale state, tool errors, or approval unavailability to verify that recovery and safety controls operate as designed.

## Safe Completion Rate

The proportion of workflows that either satisfy their acceptance criteria or reach an approved safe terminal state without uncontrolled or unauthorized side effects.

## Reliability Control Plane

The system layer that independently enforces identity, permissions, budgets, retries, timeouts, idempotency, state versions, approval status, stop conditions, and audit events around agent execution.

## Guardrail

A deterministic, model-assisted, or human control that allows, transforms, pauses, denies, escalates, or safely stops an agent request, plan, action, or output.

## Policy Decision Point

A service or component that evaluates identity, capability, arguments, context, impact, and policy rules and returns a machine-readable control decision.

## Policy Enforcement Point

The component that applies a policy decision by allowing, transforming, pausing, denying, or stopping an operation before it reaches a protected resource.

## Trust Boundary

A point where data, identity, authority, or instructions move between components with different security assumptions and therefore require validation and control.

## Approval Packet

A structured human-review artifact containing the exact action, arguments, evidence, risk, expected impact, approver role, expiration, and action hash.

## Action Hash

A cryptographic digest of the canonical tool name, operation, arguments, resource, and impact class used to bind approval and idempotency to one exact logical action.

## Interrupt

A control transition that pauses a workflow before a protected action while preserving state for review and possible resume.

## Reset

A control transition that restores a workflow to a declared safe checkpoint while normally preserving its immutable audit history.

## Abort

A terminal control transition that prevents further workflow actions, reconciles in-flight effects where possible, and preserves evidence for review.

## Fail Closed

A safety posture in which an operation is blocked when authorization, approval, redaction, or another critical control cannot be verified.

## Fail Open

A posture in which an operation continues despite a control failure; it is normally unsuitable for high-impact agent actions.

## Authorization-Aware Retrieval

Retrieval that applies user, tenant, role, resource, and data-classification filters before document content reaches the model.

## Knowledge Poisoning

The insertion or modification of retrieval content to introduce false facts, malicious instructions, or unsafe behavior into an AI system.

## Safety Control Plane

An independent system layer that enforces policy, permissions, approvals, budgets, idempotency, redaction, stop conditions, and audit events around agent execution.

## Near Miss

An unsafe or unauthorized proposal that is detected and blocked before it causes a real-world side effect.

## Safe Stop

A terminal outcome that preserves state and evidence, performs no further unsafe action, and clearly reports why the workflow could not continue.

## System Contract

A measurable definition of the tasks, evidence, tools, actions, quality thresholds, safety boundaries, escalation rules, and operational budgets an AI system must satisfy.

## Evaluation Unit

The object being scored in an evaluation, such as a component, workflow step, full agent trajectory, final outcome, or operational behavior.

## Golden Case

A curated evaluation case containing the input, user context, available evidence, acceptable routes, required and prohibited behavior, expected tools, escalation expectation, and grading criteria.

## Deterministic Evaluator

A reproducible programmatic check used for formal properties such as schema validity, permissions, citations, latency budgets, state transitions, and prohibited content.

## Judge Calibration

The process of measuring and adjusting a model-based evaluator against expert-labeled cases to understand agreement, false passes, false failures, subgroup differences, and stability.

## Claim-Level Evaluation

An evaluation method that decomposes an answer into individual claims and checks each claim for support, contradiction, absence, or unverifiability against approved evidence.

## Faithfulness

The degree to which an AI response is supported by the evidence, context, or tool results supplied to the system, regardless of whether the claims happen to be true elsewhere.

## Factual Consistency

The degree to which statements in an AI response are correct and do not contradict reliable facts or the system's approved sources.

## Counterfactual Testing

A fairness test that changes a sensitive or group-associated attribute while holding task-relevant facts constant to determine whether the system's outcome changes materially.

## Intersectional Analysis

Evaluation of outcomes across combinations of relevant user characteristics rather than only one group attribute at a time.

## Release Gate

A deployment control that combines hard constraints, metric thresholds, risk review, and rollback readiness to decide whether an AI system version may proceed to production.

## Input Drift

A production change in the distribution of requests, languages, file types, user groups, or task complexity relative to the evaluation baseline.

## Knowledge Drift

A production change in the freshness, coverage, consistency, or availability of the documents and data used to ground an AI system.

## Behavior Drift

A measurable change in system outputs or trajectories caused by updates to models, prompts, policies, tools, routing, or runtime configuration.

## Outcome Drift

A change in user, safety, fairness, operational, or business outcomes even when individual system components appear healthy.

## AI Incident

An event in which an AI system causes or creates a credible risk of incorrect, unsafe, unauthorized, unfair, private, or otherwise unacceptable behavior that requires containment and investigation.

## Residual Risk

The risk that remains after controls, evaluation, and mitigation have been applied and that must be explicitly accepted, transferred, further reduced, or avoided by an accountable owner.

## Transparency

Visibility into what an AI system is, what information and capabilities it uses, its limitations, and the conditions under which it operates.

## Interpretability

The degree to which a human can directly understand a model, rule, feature, or mechanism that contributes to an outcome.

## Explainability

A useful, audience-appropriate account of the evidence, policy, actions, uncertainty, and controls behind a specific AI output or action.

## Contestability

The ability of an affected person or reviewer to question, correct, appeal, or override an AI-assisted outcome.

## Explanation Packet

A structured artifact containing an outcome, task interpretation, material reasons, evidence provenance, policy basis, tools used, uncertainty, human controls, and correction or appeal options.

## Explanation Faithfulness

The degree to which an explanation accurately reflects the evidence, rules, actions, and control path that actually produced an outcome rather than supplying a merely plausible rationale.

## Harm Model

A use-case-specific description of affected populations, potential benefits and harms, error asymmetry, reversibility, and acceptable review or remediation paths.

## Selection-Rate Parity

A fairness criterion that compares the frequency of a positive allocation or decision across groups.

## Equal Opportunity

A fairness criterion that compares true-positive rates across groups for cases that genuinely satisfy the positive condition.

## Equalized Odds

A fairness criterion that compares both true-positive and false-positive rates across groups.

## Predictive Parity

A fairness criterion that compares positive predictive value across groups.

## Group Calibration

The property that cases assigned a particular score or probability experience the corresponding outcome at similar rates within each evaluated group.

## Abstention Parity

Comparison of how often an AI system declines, requests clarification, or refuses to decide across groups.

## Escalation Parity

Comparison of how often cases are routed to human review or a higher-cost workflow across groups, interpreted in the context of legitimate case differences.

## Service-Quality Parity

Comparison of task completion, evidence quality, explanation usefulness, latency, retries, tool failures, and correction outcomes across groups.

## Counterfactual Consistency

The degree to which an AI system preserves an outcome and its supporting evidence when a group-associated attribute changes but task-relevant facts remain constant.

## Fairness Event

A privacy-governed record of an AI case containing the versions, outcome, relevant cohort attributes, errors, routing, evidence quality, latency, explanation coverage, and correction result needed for fairness analysis.


## Threat Model

A structured description of the assets, actors, entry points, trust boundaries, misuse cases, risks, controls, verification methods, and incident paths for a system.

## Security Asset

Data, capability, identity, model, prompt, policy, tool, record, credential, service, or operational resource that requires protection from unauthorized disclosure, modification, misuse, or disruption.

## Entry Point

A location where data, instructions, code, files, model output, tool results, or agent messages enter an AI system and may influence its behavior.

## Indirect Prompt Injection

A prompt-injection attack in which malicious instructions are embedded in content that an agent later retrieves or processes, such as a document, email, webpage, ticket, or tool response.

## Retrieval Poisoning

The insertion, modification, promotion, or retention of misleading, malicious, unauthorized, or stale content in a retrieval source so that it influences generated answers or agent actions.

## Confused Deputy

A security failure in which a privileged component uses its authority on behalf of a caller who is not entitled to the requested action or data.

## Tool Gateway

A deterministic control layer that validates tool names and arguments, verifies identity and authorization, classifies impact, obtains approval where required, executes with least privilege, reconciles results, and records audit events.

## Data-Loss Prevention

Controls that detect and prevent unauthorized disclosure of sensitive information through prompts, retrieval, model responses, tools, files, logs, caches, or memory.

## Model Extraction

An attack that uses repeated or strategically selected queries to approximate, imitate, or steal proprietary model behavior, prompts, decision boundaries, or specialized capabilities.

## Supply-Chain Attack

Compromise introduced through a model, package, container, connector, dataset, prompt template, build system, hosted service, or other third-party or upstream dependency.

## Security Control Plane

A framework-independent layer that applies identity, authorization, policy, validation, approval, idempotency, isolation, telemetry, and incident controls to AI workflows and tool execution.

## Residual Security Risk

Security risk that remains after mitigations are implemented and that must be explicitly accepted, further reduced, transferred, or avoided by an accountable owner.

## Application Layer

The user-facing and channel-facing layer that manages identity, session behavior, input capture, rendering, progress, approvals, feedback, accessibility, and telemetry around an AI or agent workflow.

## Agent UX

The design of the human-control loop around an agentic system, including task framing, visible state, evidence, uncertainty, approvals, recovery, and correction.

## Interaction Contract

A clear statement of the user goal, required inputs, available capabilities, boundaries, approval model, expected output, and recovery path for an agentic experience.

## Hybrid Interaction

An interface pattern that combines natural-language conversation with structured controls such as forms, selectors, validation, and approval cards.

## Progressive Disclosure

A presentation strategy that shows the primary result first and makes supporting reasons, evidence, action history, and technical detail available in progressively deeper levels.

## Action Preview

A structured representation of a proposed consequential action that displays its target, exact arguments, expected impact, reversibility, evidence, and required approval before execution.

## Event Streaming

Delivery of meaningful workflow-status events, such as planning, retrieval, tool execution, approval, validation, and recovery, from the backend to the application as they occur.

## Presentation State

Client- or application-oriented state used to render the experience, such as expanded panels, local drafts, selected tabs, and visible progress, distinct from authoritative workflow state.

## Backend-for-Frontend

An application backend tailored to one or more user interfaces that validates client commands, subscribes to workflow events, maintains display-oriented state, and applies channel-specific rendering and privacy controls.

## Perceived Latency

The user’s experience of waiting, influenced by time to first meaningful progress, responsiveness, transparency, and control rather than only total backend execution time.

## Completion Receipt

An authoritative, user-visible record of a completed action containing identifiers, status, timestamps, material before-and-after values, approval information, and a link or reference to the system of record.

## Latency Budget

An explicit allocation of the total allowed response time across routing, retrieval, tools, model inference, validation, persistence, and rendering.

## Critical Path

The longest chain of dependent operations that determines the completion time of a workflow.

## Time to First Progress

The elapsed time from request acceptance until the application presents a meaningful workflow-state update rather than a generic loading indicator.

## Time to First Token

The elapsed time from request acceptance until the first generated token is available for streaming.

## Time to First Useful Result

The elapsed time until the system presents the first actionable or decision-relevant output, such as validated evidence, a result card, or an action preview.

## Tail Latency

The slow end of a latency distribution, commonly measured at percentiles such as p95 or p99.

## Service-Level Indicator

A measured value used to assess service behavior, such as p95 latency, successful task rate, queue time, or cost per completed workflow.

## Service-Level Objective

A target for one or more service-level indicators over a defined period and workload.

## Cost per Successful Task

The total cost of executing a workflow divided by the number of tasks that meet the required quality, safety, and completion criteria.

## Semantic Cache

A cache that reuses results for requests judged to be meaningfully similar rather than exactly identical, requiring strict identity, authorization, freshness, and quality controls.

## Negative Caching

Short-lived storage of a missing or unavailable result to prevent repeated calls for the same absent resource.

## Backpressure

A mechanism that slows, queues, degrades, or rejects incoming work when downstream capacity is saturated.

## Admission Control

A decision layer that determines whether a request may begin based on capacity, priority, quota, expected cost, deadline, and system health.

## Workload Isolation

Separation of interactive, batch, evaluation, high-risk, or tenant-specific work into distinct queues or capacity pools to prevent one workload from exhausting shared resources.

## Model Cascade

A sequence in which a lower-cost model or deterministic path is tried first and the request escalates to a more capable model or human only when measurable validation conditions fail.

## Speculative Execution

Starting likely-needed, cancelable, side-effect-free work before the final execution route is known in order to reduce the eventual critical path.

## Performance Release Gate

A deployment criterion that combines latency, cost, quality, safety, reliability, and capacity thresholds rather than evaluating speed in isolation.

## Agent Observability

The practice of understanding an agentic system through correlated operational, behavioral, quality, safety, cost, and user-experience signals across the complete task trajectory.

## Telemetry Envelope

The common set of correlation, identity, tenant, version, and execution attributes attached to logs, metrics, traces, events, evaluations, and feedback for one workflow run.

## Distributed Trace

A correlated representation of one request as it moves across application, orchestration, model, retrieval, tool, state, policy, and human-review components.

## Span

A timed operation within a distributed trace, containing a name, parent relationship, status, duration, and structured attributes.

## Correlation Identifier

A stable identifier such as a request, run, trace, thread, or tenant ID used to join telemetry signals belonging to the same task or context.

## Version Envelope

The immutable collection of application, workflow, prompt, model, knowledge-index, policy, schema, and tool versions used by a particular run.

## Error Budget

The amount of allowed unreliability implied by a service-level objective over a defined measurement window.

## Burn Rate

The rate at which an error budget is being consumed relative to the rate that would exhaust it exactly at the end of the measurement window.

## Operational Contract

A definition of healthy workflow behavior that specifies user goals, required evidence, permitted actions, quality and safety conditions, budgets, terminal states, and observable signals.

## Incident Packet

A structured collection of affected identifiers, symptoms, versions, failing spans, evidence, control decisions, containment actions, ownership, and next steps used to coordinate incident response.

## Runbook

A repeatable operational procedure linked to an alert or incident category that guides diagnosis, containment, recovery, and verification.

## Trajectory Replay

Re-execution or simulation of a historical agent run using recorded versions, evidence, tool responses, and state while preventing real side effects.

## Counterfactual Replay

A replay method that changes one controlled variable, such as a prompt, model, index, policy, or route, to attribute behavioral differences.

## Shadow Deployment

A deployment pattern in which a new system version processes live inputs for comparison but does not control the user-visible answer or execute consequential actions.

## Canary Deployment

A progressive release pattern that sends a limited, controlled share of traffic to a new version and expands only when quality, safety, reliability, latency, and cost gates pass.

## Tail Sampling

A trace-retention strategy that decides whether to keep a trace after observing its outcome, enabling preferential retention of failures, anomalies, or high-risk runs.

## Cardinality

The number of distinct values for a telemetry field or metric label; unbounded cardinality can make metrics systems expensive or unstable.

## Change Attribution

The process of connecting a behavior or metric change to the specific workflow, prompt, model, knowledge, policy, schema, tool, or experiment version that produced it.

## Human Review Queue

The operational queue of agent escalations, approval requests, edits, and exception cases that require assigned human decisions and measurable service objectives.

## AI-Native Product Management

A product operating model that uses AI to shorten and improve the learning loop across discovery, planning, design, delivery, launch, measurement, and optimization while retaining accountable human judgment.

## Product Learning Loop

A continuous cycle in which customer behavior produces governed signals, analysis creates hypotheses, product judgment selects an action, an experiment or release changes the experience, and the resulting outcomes become new evidence.

## Decision Contract

A structured record of a product decision containing the decision question, options, evidence, assumptions, uncertainties, selected action, owner, review date, and reversal condition.

## Evidence Quality

A measure of how trustworthy and decision-relevant a set of product signals is, considering source diversity, freshness, coverage, provenance, and contradiction.

## Experiment Contract

A structured definition of an experiment containing the hypothesis, target population, primary metric, guardrail metrics, thresholds, stop conditions, owner, and required follow-up decision.

## Product Metric Tree

A hierarchy connecting a north-star product outcome to user value, business value, experience, AI quality, agent behavior, safety, fairness, reliability, latency, and cost metrics.

## Guardrail Metric

A metric that defines a boundary an experiment or release must not cross, such as harmful-action rate, privacy incidents, security regressions, or severe cohort disparity.

## Bounded Autonomy

An operating mode in which an AI system may execute only predefined, reversible, policy-approved actions within explicit permissions, budgets, validation rules, and escalation paths.

## Artifact Acceleration

The use of AI to produce more documents, summaries, or plans without measurably improving evidence quality, decision speed, product outcomes, or learning.

## Decision Provenance

The traceable record of the evidence, assumptions, versions, analyses, human judgments, and approvals that produced a product decision.

## Support Triage

The process of classifying an incoming support request, estimating impact and urgency, selecting an owner, determining escalation, and recommending or executing the next permitted action.

## Severity

The intrinsic seriousness of a problem, such as service unavailability, data loss, or security impact, independent of queue order or customer language.

## Support Priority

The operational ordering assigned to a support case after considering severity, customer impact, affected scope, workaround availability, entitlement, policy, and uncertainty.

## Multi-Intent Ticket

A support request that contains two or more materially distinct issues which may require different owners, policies, service levels, or child work items.

## Least-Powerful-Action Principle

The design rule that an agent should use the least consequential capability that can satisfy the immediate goal, preferring explanation or recommendation over a write when possible.

## Priority Floor

A policy constraint that prevents a case from being assigned below a specified priority when a critical condition, such as confirmed data loss or a tenant-wide outage, is present.

## Priority Ceiling

A policy constraint that prevents a case from being assigned above a specified priority when its scope and impact do not justify a more urgent operational response.

## Severity-Weighted Error

An evaluation method that assigns greater penalty to dangerous classification mistakes, such as missing a critical outage, than to lower-impact differences between neighboring priorities.

## Action Proposal

A structured, reviewable description of a proposed tool action containing the capability, normalized arguments, risk class, approval requirement, and idempotency key.

## Assistive Triage

A deployment mode in which the system recommends classification, priority, ownership, and next actions while a human support agent remains responsible for confirmation and execution.

## Supplier Eligibility

The determination that a supplier satisfies every mandatory condition for a sourcing request, including approval, region, capacity, delivery, quality, certification, budget, and policy constraints.

## Hard Constraint

A mandatory decision condition that cannot be compensated for by strengths in other criteria; failure excludes a candidate unless an explicitly authorized exception exists.

## Supplier Ranking

The ordered comparison of suppliers that have already passed eligibility, using governed criteria such as landed cost, delivery margin, quality, reliability, and risk.

## Landed Cost

The total comparable cost of acquiring and receiving an item, including unit price, freight, duties, fees, and other approved cost components.

## Delivery Buffer

The number of days between a supplier's expected delivery date and the request's required-by date; a positive value represents schedule margin.

## Weight Governance

The ownership, versioning, approval, testing, and monitoring process applied to the criterion weights used in a decision model.

## Ranking Stability

The degree to which a recommendation remains unchanged when reasonable variations are applied to weights, inputs, or uncertain evidence.

## Pareto Alternative

A candidate that is strongest on a material dimension, such as cost, delivery, quality, or risk, even when it is not the highest-scoring balanced recommendation.

## Supplier Evidence Contract

A structured supplier fact containing its source, version, timestamp, validity, unit, provenance, confidence, and access classification.

## Sourcing Exception

A separately authorized deviation from a procurement constraint, recorded with its policy basis, approver, rationale, scope, and expiration.

## Project Coordination Agent

An agentic workflow that gathers authorized project signals, identifies and ranks blockers, resolves ownership, explains delivery impact, recommends bounded next actions, and preserves evidence, state, controls, and auditability.

## Blocker Evidence Contract

A normalized project evidence record containing source type, source URI, project and work-item scope, owner reference, timestamp, version, authority, access classification, and the text or structured fact used in blocker analysis.

## Confirmed Blocker

A condition supported by current authoritative evidence that prevents or materially delays planned work.

## Emerging Risk

A project signal that may become a blocker but does not yet have sufficient authoritative evidence to confirm that progress is prevented.

## Contradictory Project State

A condition in which current project sources disagree materially, such as a blocked ticket and a newer owner message reporting recovery, requiring explicit reconciliation rather than silent averaging.

## Accountable Owner

The person or team authorized and responsible for driving a blocker toward resolution, distinguished from the person who reported or discussed the issue.

## Dependency Fan-Out

The number or importance of downstream work items that depend on a blocked item, used as one input to delivery-impact assessment.

## Partial Source Availability

An operating condition in which one or more configured project sources are unavailable while sufficient authorized evidence remains to produce a limited report with reduced confidence and explicit limitations.

## Blocker Freshness

An assessment of whether blocker evidence is current enough to support a present-tense conclusion, based on timestamps, source authority, versions, and resolution signals.

## Project Status Draft

A non-published, reviewable status artifact produced by the coordination workflow and held for human approval before distribution.



## Competitive Research System

A governed workflow that converts a bounded market question into a research plan, retrieves permitted evidence, compares normalized findings, reviews claim support, and produces a cited decision brief with explicit uncertainty and human approval.

## Research Contract

A typed definition of a competitive-research task containing scope, competitors, dimensions, geography, segment, as-of date, source permissions, budgets, completion conditions, and output requirements.

## Evidence Ledger

A provenance-preserving collection of normalized evidence records containing source identity, publisher, publication and retrieval times, content hash, authority, directness, relevance, independence group, and access classification.

## Source Independence Group

A grouping of sources that share the same underlying origin, such as an official press release and several syndicated reposts, used to prevent repeated copies from being treated as independent corroboration.

## Claim-Evidence Graph

A structure connecting factual claims to their supporting evidence, interpretations, limitations, and downstream recommendations so that a report can be reviewed, replayed, and corrected.

## Citation Correctness

The degree to which a cited source supports the exact scope and meaning of the claim it accompanies, rather than merely discussing a related topic.

## Availability State

A normalized product status such as generally available, limited availability, preview, partner-delivered, announced, deprecated, or unknown.

## Competitive Comparison Contract

A governed set of dimensions, definitions, units, evidence requirements, and as-of dates applied consistently across all compared products.

## Evidence Laundering

The appearance of independent support created when multiple sources repeat the same original statement without adding independent verification.

## Targeted Research Replan

A bounded revision of the research plan that addresses a specific material evidence gap or contradiction without restarting the entire workflow.

## Decision Brief

A concise research output that presents verified findings, evidence strength, limitations, unresolved questions, product implications, and recommended validation actions.

## Strategic Imitation Error

The mistake of concluding that a product should build a capability solely because a competitor offers it, without validating customer need, strategic fit, differentiation, cost, and risk.

## CLEAR Method

A five-step system-design response structure: Clarify the goal and risk, Lay out contracts, Establish the architecture, Add controls, and Review trade-offs and evolution triggers.

## Architecture Decision Ladder

A sequence for selecting the least complex reliable solution, moving from deterministic software to prompted models, RAG, workflows, single agents, and multi-agent systems only when each added capability is justified.

## Interview Scorecard

A structured rubric that rates an architecture answer across requirements, architecture choice, contracts, grounding, tools, state, safety, evaluation, operations, UX, trade-offs, and communication.

## Whiteboard Architecture Checklist

A checklist used during system-design interviews to ensure that application UX, identity, orchestration, models, retrieval, tools, systems of record, guardrails, evaluation, and observability are represented.

## Practice Scenario

A bounded system-design problem used to rehearse requirements clarification, architecture selection, threat modeling, evaluation, operations, and trade-off communication under interview conditions.

## Architecture Evolution Trigger

A measurable change in scale, risk, latency, tools, data boundaries, workflow duration, or reliability requirements that justifies moving to a more sophisticated architecture.


## Advanced Prompting Pattern

A reusable prompt and control-flow structure selected for a task shape, such as direct prompting, staged decomposition, plan-and-execute, ReAct, critique-and-revision, or candidate ensembles.

## Prompt Contract

A typed specification of the model's role, task, context, constraints, output format, authority rules, completion conditions, failure behavior, and permitted actions.

## Authority Contract

The explicit precedence order used when system policy, application policy, user instructions, retrieved evidence, memory, and untrusted content conflict.

## Completion Contract

A set of measurable conditions that must be satisfied before a prompted workflow may return a final result or perform an approved action.

## Failure Contract

The defined behavior for missing evidence, invalid output, tool failure, ambiguity, insufficient confidence, exhausted retries, or unsafe requests.

## Staged Prompting

A prompting design that separates a complex task into bounded model calls with typed intermediate outputs, validators, and explicit handoffs.

## Least-to-Most Prompting

A pattern that solves simpler prerequisite subproblems before using their accepted outputs to solve the complete task.

## Reasoning Artifact

A concise, inspectable intermediate product such as extracted facts, assumptions, evidence identifiers, a plan, decision criteria, calculations, or a brief rationale, used without requesting private chain-of-thought.

## Adaptive Prompt Routing

The selection of a prompt pattern from observable request features such as ambiguity, external-fact needs, tool requirements, risk, action impact, and output complexity.

## Program-Aided Reasoning

A pattern in which a model interprets a problem and extracts variables, deterministic code performs exact computation or validation, and the model explains the verified result.

## Reflection Budget

A limit on critique and revision rounds, latency, cost, or tokens that prevents a reflection loop from continuing without measurable improvement.

## Search-Style Reasoning

A bounded process that generates multiple candidate approaches, evaluates them against explicit criteria, and expands or selects only the most promising supported branches.

## Prompt Plan Hash

A stable digest of a prompt workflow's selected pattern, stages, limits, and completion conditions, used for traceability, approval binding, and change attribution.

## Prompt Evaluation Contract

A versioned specification of the required, prohibited, and failure behaviors for a prompted system, including task success, evidence use, output format, safety, latency, cost, and escalation conditions.

## Prompted System Configuration

The complete unit evaluated in a prompt experiment, including prompt templates, system instructions, model and decoding settings, retrieval, tools, policies, validators, and application behavior.

## Prompt Evaluation Dataset

A governed collection of normal, boundary, ambiguous, adversarial, historical, and slice-labeled test cases used to measure prompted-system behavior.

## Hidden Holdout Set

A protected evaluation subset that is not used during prompt iteration and is reserved for estimating generalization and detecting benchmark overfitting.

## Deterministic Prompt Validator

Code that checks objectively enforceable properties such as schema validity, allowed labels, required fields, numerical ranges, permissions, citation identifiers, data-loss-prevention rules, latency, and cost.

## Model Judge Calibration

The process of comparing a model-based evaluator with expert human labels to measure agreement, false-pass and false-fail rates, position bias, verbosity bias, repeatability, and slice behavior.

## Pairwise Prompt Comparison

An evaluation method that runs two prompt configurations on the same test cases and compares their outputs directly, producing wins, losses, ties, and case-level deltas.

## Prompt Failure Taxonomy

A classification of observed failures into causes such as ambiguous instructions, missing context, poor retrieval, tool-contract errors, authorization gaps, workflow defects, model limitations, or stable domain behavior gaps.

## Prompt Overfitting

A condition in which a prompt is optimized too closely to a development benchmark and fails to generalize to holdout cases, paraphrases, new time periods, or production distributions.

## Prompt Release Gate

A deterministic decision rule that blocks or permits controlled deployment based on hard safety constraints, non-regression thresholds, quality improvement, latency, cost, and critical-slice performance.

## Prompt Registry

A system of record for prompt identifiers, source templates, hashes, owners, compatibility, dependent tools and retrieval systems, evaluation reports, approvals, deployment history, and rollback targets.

## Prompt Drift

A change in prompted-system quality caused by shifts in users, inputs, models, retrieval data, tools, policies, or operating conditions even when the prompt text itself remains unchanged.

## Citation Coverage

The proportion of material generated claims that include a citation or evidence reference.

## Citation Correctness

The proportion of cited claims for which the referenced evidence actually supports the exact scope and meaning of the claim.


## Discovery Evidence Contract

A structured record defining a discovery signal's source, date, user or segment scope, directness, sensitivity, freshness, verifiability, and limitations so generated themes remain traceable.

## Opportunity Registry

A system of record for product problems, desired outcomes, supporting and contradicting evidence, assumptions, constraints, AI suitability, risks, confidence, and next learning actions.

## Evidence Independence

The degree to which multiple evidence items represent distinct observations rather than duplicates, reposts, repeated complaints from one account, or records generated by the same incident.

## Confidence-Adjusted Value

A prioritization concept that scales estimated user or business value by the quality and coverage of supporting evidence before effort and risk penalties are applied.

## AI Suitability Test

A decision check that compares an AI approach with deterministic alternatives and assesses data readiness, evaluation feasibility, uncertainty tolerance, safety, reversibility, and operational burden.

## Product Decision Contract

An accountable human decision record containing the selected option, evidence, assumptions, guardrails, expected outcome, reversal conditions, owner, and review trigger.

## Portfolio Balance

The intentional allocation of product capacity across customer outcomes, discovery, quality and evaluation, safety and governance, reliability and performance, and platform or technical-debt work.

## Negative Evidence

Evidence that challenges, limits, or contradicts a product theme or problem hypothesis and is retained to prevent overconfident interpretation.

## AI Product Experiment Contract

A versioned specification written before exposure begins that defines the decision, hypothesis, variants, population, assignment unit, metrics, thresholds, duration, stopping rules, rollback conditions, analysis plan, and accountable owner.

## Primary Outcome Metric

The single principal measure used to determine whether an experiment achieved its intended user or business outcome.

## Experiment Guardrail Metric

A quality, safety, fairness, latency, cost, or operational measure that must remain within a predefined limit even when the primary outcome improves.

## Diagnostic Metric

A measure used to explain why an experimental outcome changed, such as retrieval recall, clarification rate, tool success, evidence coverage, retries, or abandonment stage.

## Shadow Experiment

A production evaluation in which a candidate processes a sanitized copy of live traffic but does not affect the user-visible response or perform external side effects.

## Canary Release

A limited production exposure used primarily to detect severe safety, reliability, latency, cost, authorization, or operational failures before broader rollout.

## Switchback Experiment

An experimental design that alternates control and treatment across predefined time windows when randomizing individual users is impractical because the system or queue is shared.

## Sample-Ratio Mismatch

A material difference between planned and observed variant allocation that may indicate assignment bugs, selective logging, eligibility defects, or variant-specific failures.

## Cost per Verified Successful Task

The total model, retrieval, tool, infrastructure, and human-review cost divided by outcomes that were independently verified as successful.

## Practical Significance

The degree to which an observed effect is large enough to justify product, operational, financial, or risk trade-offs, regardless of whether it is statistically detectable.

## Experiment Decision Record

An accountable record of the experiment result, uncertainty, constraints, limitations, decision, owner, rollout plan, monitoring requirements, and reversal conditions.

## Interoperability terms

### Agent Card
An A2A discovery document that describes an agent endpoint, supported interfaces, capabilities, skills, security schemes, and operational metadata. Discovery does not itself grant authorization.

### Agent2Agent Protocol (A2A)
An open protocol for communication and collaboration between independent, potentially opaque agentic applications. Its core concepts include Agent Cards, skills, messages, parts, tasks, artifacts, contexts, and task-state transitions.

### A2A artifact
A concrete output produced by an A2A task, such as a report, file, structured result, or other deliverable.

### A2A context
A logical conversation or collaboration scope that can contain multiple related messages and tasks.

### A2A skill
A capability advertised by an agent in its Agent Card. A skill describes a bounded class of work the remote agent can perform.

### A2A task
A stateful unit of delegated work in A2A. Tasks support lifecycle states, status updates, artifacts, streaming, cancellation, and long-running execution.

### Model Context Protocol (MCP)
An open protocol that connects AI applications to external tools, resources, prompt templates, and client-provided capabilities through a standardized model-facing boundary.

### MCP client
The protocol component maintained by an MCP host for communicating with one MCP server.

### MCP host
The AI application that coordinates MCP clients, user consent, model interaction, security policy, and context assembly.

### MCP prompt
A reusable prompt template exposed by an MCP server and selected explicitly by a user or host.

### MCP resource
Contextual data exposed by an MCP server, identified by a URI and generally read without implying an external side effect.

### MCP server
A service that exposes a bounded set of MCP capabilities such as tools, resources, and prompts.

### MCP tool
A callable capability exposed by an MCP server. Tools can compute results, query systems, or perform actions and therefore require explicit schemas, authorization, and side-effect controls.

### Protocol conformance testing
Testing that verifies wire formats, message schemas, transports, version negotiation, and lifecycle rules match a protocol specification.

### Semantic contract testing
Testing that verifies a capability behaves as its description promises, including meaning, authorization, evidence, safety, idempotency, and business outcomes.



## Modern agent SDK and programming terms

### Agent runtime
A software layer that owns an agent's execution loop, including model turns, tool calls, delegation, stopping, errors, and often session or tracing behavior.

### Anti-corruption layer
An adapter boundary that translates framework-specific messages, tools, events, and state into portable domain contracts so that framework concepts do not leak into business logic.

### Context augmentation
The practice of supplying an LM or agent with relevant external data, retrieved evidence, structured records, or tools at runtime rather than relying only on model parameters.

### Framework adapter
A component that maps portable domain requests, tools, events, state, and responses to one framework's APIs while preserving the business contract.

### Framework lock-in
The cost or difficulty of replacing a framework because business logic, state, telemetry, evaluation, or deployment has become coupled to its proprietary abstractions.

### LM program
A composition of typed language-model tasks, modules, tools, retrieval steps, and control flow that can be executed and evaluated as a program.

### DSPy module
A composable LM-program component that implements a task or reasoning strategy using a DSPy signature and ordinary Python control flow.

### DSPy optimizer
An algorithm that improves a DSPy program's prompts, demonstrations, or configuration against examples and a metric.

### DSPy signature
A declarative, typed contract describing the input fields, output fields, and instruction of an LM task.

### Proof of capability
A controlled evaluation in which candidate frameworks implement the same representative, failure, safety, recovery, and operational scenarios before an architecture decision is made.

### Normalized agent event
A framework-independent telemetry or audit event such as a model call, tool call, delegation, retrieval, approval, state write, or evaluation result.

### Microsoft Agent Framework
Microsoft's successor agent framework that combines concepts from Semantic Kernel and AutoGen, with agent abstractions, session-based state, middleware, telemetry, and graph-based workflows.

## Evaluation and observability framework terms

### Evaluation case
A versioned test record containing an input, optional reference output, expected evidence or tools, risk labels, and metadata used to judge an AI system.

### Execution trace
A correlated record of one application run, including intermediate model calls, retrieval, tools, state transitions, policies, approvals, errors, latency, and cost.

### Span
A timed unit of work inside a trace, such as one model call, retrieval operation, tool invocation, guardrail check, or workflow node.

### Offline evaluation
Evaluation performed before deployment on a curated and usually versioned dataset, often for benchmarking, regression testing, or release gating.

### Online evaluation
Evaluation performed on sampled or selected production runs or threads to detect quality, safety, or operational degradation.

### Trajectory evaluation
Evaluation of the sequence of plans, routes, tool calls, observations, retries, handoffs, and state changes that produced an agent outcome.

### Evaluator calibration
The process of measuring an evaluator's agreement, stability, bias, and error rates against trusted human labels or deterministic ground truth.

### Evaluator drift
A change in evaluation scores caused by updates to the judge model, rubric, prompt, threshold, or implementation rather than by a change in the application.

### Critical slice
A defined subset of evaluation cases, such as high-risk actions, a language, a user segment, or an adversarial category, with its own release threshold.

### Trace completeness
The proportion of required execution stages and metadata fields that are present and correlated in an observability trace.

### Ragas
An evaluation framework centered on datasets, experiments, and metrics for RAG and agentic AI applications.

### DeepEval
A local-first LLM evaluation framework that organizes tests around cases, datasets, metrics, traces, and CI-oriented test runs.

### LangSmith
A platform for AI application tracing, dataset curation, experiments, offline evaluation, online evaluation, prompt iteration, and production observability.

### Phoenix
An open-source AI observability and evaluation platform based on OpenTelemetry and OpenInference instrumentation.

### OpenInference
A set of semantic conventions and instrumentation libraries for representing AI operations such as model calls, retrieval, embeddings, reranking, tools, and agents in traces.

### Model judge
A language or multimodal model used to evaluate another system output or trajectory against a rubric.

### Pairwise evaluation
An evaluation method that asks an evaluator to prefer one of two candidate outputs rather than assigning an independent absolute score to each.

### Release gate
A rule that converts evaluation evidence into a ship, hold, canary, rollback, or escalation decision.

### Trace-to-dataset loop
A continuous-improvement workflow in which notable production traces are reviewed, labeled, and promoted into an offline regression dataset.

### Risk-based sampling
A production evaluation strategy that samples more heavily from high-impact actions, low-confidence runs, failures, new versions, or underrepresented cohorts.

## Workflow automation and deployment terms

### Control plane
The application layer that enforces API contracts, identity, policy, approvals, idempotency, state transitions, and audit behavior around agent and workflow execution.

### Workflow plane
The orchestration layer that coordinates triggers, integrations, waits, routing, retries, and cross-system execution.

### n8n queue mode
A scalable n8n deployment pattern in which a main instance receives triggers and schedules executions while worker instances consume jobs through a Redis-backed queue and share persistent database state.

### Liveness probe
A health endpoint that indicates whether a process is alive and should continue running rather than be restarted.

### Readiness probe
A health endpoint that indicates whether an instance is prepared to receive traffic, including whether critical initialization or dependencies are available.

### Idempotency key
A stable request identifier used to ensure that retries or duplicate deliveries return the same result without repeating a business side effect.

### Action hash
A cryptographic digest of an exact proposed action, target, arguments, policy version, and other material fields used to bind approval to that action.

### Confirmation read
A follow-up query to the authoritative system used to verify whether a side effect succeeded, especially after an ambiguous timeout or transport failure.

### Dead-letter workflow
A failure-handling path that preserves an exhausted or unrecoverable workflow execution for operator review rather than silently discarding it.

### Expand-and-contract migration
A backward-compatible deployment strategy that first adds new schema capability, then migrates producers and consumers, and only later removes obsolete fields.

### Immutable image digest
A content-addressed container image reference that identifies exact image bytes and cannot be moved like a mutable tag.

### Build provenance
Verifiable metadata describing where, how, and from which source revision a software artifact was built.

### Deployment environment
A protected CI/CD target such as staging or production with its own credentials, policies, reviewers, and deployment history.

### Canary deployment
A rollout strategy that sends a limited portion of production traffic or tasks to a new version before broader promotion.

### OIDC workload identity
Short-lived federated authentication in which a CI/CD workflow exchanges an OpenID Connect token for cloud permissions instead of storing a long-lived cloud key.

## Context engineering

The deliberate design of the complete inference-time information environment: instructions, user input, retrieved evidence, memory, tool descriptions, workflow state, schemas, policies, and output budget.

## Context contract

A typed specification describing which context categories are allowed, their authority and provenance, their budgets, and the validation rules applied before model invocation.

## Context operation

A transformation that acquires, validates, ranks, deduplicates, compresses, routes, caches, retains, or removes context.

## Agent harness

The runtime control system surrounding a model. It mediates observations, model decisions, tool calls, policy checks, budgets, state, verification, tracing, and termination.

## Harness ablation

An experiment that removes or changes one harness mechanism—such as retries, memory, verification, or tool descriptions—to measure its causal contribution.

## Agent loop engineering

The discipline of designing the recurring observe–decide–validate–act–evaluate cycle as a bounded, measurable, recoverable state machine.

## Progress measure

A typed signal used to determine whether an agent trajectory is moving toward completion, such as unresolved-task count, verified-claim coverage, or completed dependencies.

## No-progress limit

A bound on consecutive turns that fail to improve the selected progress measure, after which the loop must replan, escalate, or stop.

## Action fingerprint

A stable hash or normalized identity for an intended action and its arguments, used to detect duplicate tool calls and protect idempotency.

## Verification budget

The allocated time, model calls, tools, or compute used to check candidate actions and outputs before acceptance.

## Formal verification

The use of mathematically specified properties and proof or model-checking techniques to establish that a system or workflow satisfies defined constraints.

## Test-time compute

Additional inference-time work—such as candidate generation, search, critique, tool use, or verification—used to improve an answer or action without changing model parameters.

## Lifelong agent learning

Research on agents that accumulate, revise, and transfer skills or memory across tasks and time while controlling forgetting, unsafe drift, and provenance.
