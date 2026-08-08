# Library Examples and CLI Conventions

## Purpose

The library companions are small, explicit programs. They are not intended to hide architecture behind a notebook. Each script has a command-line interface so that the same scenario can be exercised manually, in CI, from a shell workflow, or from another program.

## Common conventions

### Discover arguments

```bash
python examples/library-companions/04_openai_structured_output.py --help
```

### Use a dry run first

```bash
python examples/library-companions/04_openai_structured_output.py \
  --ticket "The invoice amount is incorrect" \
  --model YOUR_MODEL_DEPLOYMENT \
  --dry-run \
  --output /tmp/openai-plan.json
```

A dry run validates arguments, environment expectations, and structured contracts without sending data to an external model.

### Write machine-readable output

```bash
python examples/library-companions/22_pydantic_context_contracts.py \
  --input examples/library-companions/context.json \
  --schema /tmp/context.schema.json \
  --output /tmp/context.validated.json
```

### Keep model and service identifiers configurable

Do not hard-code production model names, deployment IDs, tenant IDs, endpoints, index names, or database credentials. Supply them as arguments or environment variables.

## Argument patterns

| Argument | Meaning | Typical validation |
|---|---|---|
| `--data`, `--documents`, `--input` | Local scenario or dataset | Exists, readable, expected columns/schema |
| `--text`, `--query`, `--request`, `--ticket` | User/task input | Length and content boundaries |
| `--model`, `--deployment` | Provider model/deployment identifier | Non-empty, allowlisted in production |
| `--top-k` | Retrieval depth | Positive and bounded |
| `--temperature` | Sampling control | Provider-supported range |
| `--max-turns`, `--epochs` | Loop/training budget | Positive upper bound |
| `--timeout` | Network deadline | Positive and below workflow SLO |
| `--dry-run` | Build/validate without remote execution | No side effects |
| `--output` | JSON report path | Parent writable, atomic write in production |

## Error handling

The examples fail loudly when a dependency is absent and print the minimal install command. Production code should additionally classify failures into validation, authorization, transient dependency, permanent dependency, policy, and internal errors.

## Reproducibility

Training and simulation examples expose a seed. Evaluation examples retain the input dataset and configuration alongside output. Remote model behavior can still vary; record provider, model/deployment, prompt version, tool versions, retrieval index version, and sampling settings.

## Suggested workflow

```text
Read chapter
  -> run standard-library scenario
  -> inspect scenario JSON
  -> install one requirements pack
  -> run library example in dry-run mode
  -> run live against a test environment
  -> compare trace and output contracts
  -> add evaluation and release gates
```

## Remote-service safety

- Use non-production data unless the service is approved for the data classification.
- Redact personal or confidential values before sending them.
- Use read-only tools until action policies and approval gates exist.
- Put deadlines around every network call.
- Add idempotency keys to writes.
- Store traces without raw secrets or unnecessary prompt content.

## Extending an example

When adapting a script, keep four layers separate:

1. **Domain contract** — the typed request, evidence, action, and result.
2. **Policy** — authorization, budget, approval, and completion rules.
3. **Framework adapter** — OpenAI Agents SDK, LangGraph, CrewAI, AutoGen, LangChain, ADK, Semantic Kernel, DSPy, MCP, or A2A.
4. **Infrastructure adapter** — API, database, vector store, queue, trace collector, and secret provider.

This separation lets the same scenario be implemented with multiple libraries without rewriting the business policy.
