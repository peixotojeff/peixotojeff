
# Helix — 15-Minute Presentation Deck

## Slide 1 — Title

**Helix: Multi-Agent Orchestration Platform**  
Governed AI runs for B2B marketing operations at Grupo Studio.

Speaker note: Position Helix as a production AI platform, not a prompt collection.

---

## Slide 2 — The Business Problem

- B2B campaign production depends on many handoffs.
- Briefings lose context across strategy, copy, SEO, design, review, and approval.
- External agency dependency adds cost and latency.
- AI usage without governance is hard to measure, trust, or improve.

Speaker note: Focus on operational friction and measurable cost of coordination.

---

## Slide 3 — What Helix Does

- Receives a business briefing.
- Routes work through specialist agents.
- Retrieves company and campaign memory.
- Pauses for human approval when needed.
- Tracks tokens, model spend, run quality, and estimated business impact.
- Produces reusable outputs and learnings.

Speaker note: Keep this concrete: one briefing becomes one auditable run.

---

## Slide 4 — Business Impact

- Projected 78% reduction in campaign production time.
- Projected 65% reduction in external agency dependency.
- Cost tracking per run, model, and agent.
- Impact API estimates hours saved and BRL savings.
- Next milestone: replace projections with metrics from 20-30 internal runs.

Speaker note: Be explicit that current headline numbers are projected until benchmarked.

---

## Slide 5 — Architecture

```text
React Dashboard
  -> Express Gateway
  -> FastAPI Runtime
  -> LangGraph StateGraphs
  -> PostgreSQL Checkpoints
  -> Hybrid Memory: Cognee + Neo4j + Qdrant
  -> Evaluation + Impact APIs
```

Speaker note: The core architecture choice is durable graph state plus operator UI.

---

## Slide 6 — Why LangGraph

- Explicit state machines instead of uncontrolled chat loops.
- Durable `interrupt()` and `resume` for approvals.
- Conditional routing through `route_fn`.
- Node-level retry and failure-aware paths.
- Better fit for auditable enterprise workflows than linear `AgentExecutor`.

Speaker note: This is the main staff-level trade-off slide.

---

## Slide 7 — CEO Orchestrator Pattern

- Supervisor reads the briefing and context.
- Specialist agents execute focused steps.
- Supervisor routes, reviews, and decides next step.
- Checkpoints stop the graph when human input is needed.
- Future upgrade: ReAct/planning supervisor with dynamic tool access.

Speaker note: Explain where autonomy exists and where governance constrains it.

---

## Slide 8 — Cost Governance

- `CostTrackingCallback` records token usage and estimated spend.
- Model routing sends simple work to Flash and complex reasoning to Pro.
- `/api/impact/summary` connects spend with hours saved and quality.
- Next: budget alerts, p95 latency, retry cost, and cost-per-output dashboards.

Speaker note: Show that cost is managed as a product metric, not a billing surprise.

---

## Slide 9 — Evaluation Framework

- LLM-as-Judge scores relevance, completeness, brand voice, actionability, and accuracy.
- Ragas hooks measure faithfulness and contextual precision for RAG outputs.
- Results persist in `run_quality_summary`.
- Next: task success rate, checkpoint intervention rate, approval rate, and A/B testing.

Speaker note: Evaluation is the foundation for improving prompts and routing policies.

---

## Slide 10 — Resilience

- PostgreSQL-backed graph persistence.
- Retry wrapper per agent node.
- Failure state returned to the graph instead of crashing the whole run.
- Next: circuit breakers, adaptive retry, rate limiting, backpressure, and state versioning.

Speaker note: Tie resilience to long-running workflows and real human approval delays.

---

## Slide 11 — Demo Flow

1. Submit a briefing.
2. Watch supervisor routing.
3. Inspect agent outputs.
4. Respond to checkpoint.
5. Resume run.
6. Review quality and cost metrics.

Speaker note: The demo should be short and controlled. One successful run beats ten features.

---

## Slide 12 — What Makes It Staff-Level

- Clear product/business outcome.
- Explicit architecture trade-offs.
- Cost, quality, and reliability instrumentation.
- Human-in-the-loop production workflow.
- Roadmap from prototype to governed platform.

Speaker note: End by framing Helix as platform engineering for applied AI.
