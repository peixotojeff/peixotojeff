# Jefferson Peixoto — Senior Generative AI Engineer

**Construindo sistemas multi-agente de produção com LangGraph, LLMOps e Human-in-the-Loop.**

Atuo na interseção entre **Data Engineering**, **Machine Learning** e **Generative AI**, criando plataformas que transformam briefings não estruturados em workflows governados, auditáveis e mensuráveis de negócio.

Atualmente liderando o desenvolvimento da **Helix**, uma plataforma de orquestração multi-agente nativa em LangGraph para operações de marketing B2B e BI no Grupo Studio.

---

## Sobre Mim

Engenheiro de IA com foco em **sistemas agenticos escaláveis** e **LLMOps**. Minha expertise está em projetar, implementar e colocar em produção arquiteturas complexas de Generative AI que entregam impacto mensurável (redução de custo, tempo e dependência externa).

Busco posições **Senior / Staff Generative AI Engineer** (Brasil ou remoto internacional) onde possa liderar tecnicamente iniciativas de alto impacto envolvendo agentes autônomos, RAG híbrido, avaliação de LLMs e governança de custo.

---

## Habilidades Técnicas (Staff Level)

### Core Generative AI
- **Multi-Agent Orchestration**: LangGraph (StateGraph, Supervisor, interrupt/resume), ReAct, dynamic routing
- **LLM Engineering**: Gemini 2.5 Pro/Flash, Llama, Mistral, Claude, dynamic model routing + fallback
- **Advanced RAG**: Hybrid Memory (Qdrant + Neo4j + Cognee), reranking, graph-aware retrieval
- **Fine-tuning & Optimization**: LoRA/QLoRA, vLLM, Triton (em roadmap)
- **Evaluation & Guardrails**: LLM-as-Judge, Ragas, ARES, cost tracking, quality gating
- **Agentic Patterns**: Planning Supervisor, Tool Use, Memory Reflection, Human-in-the-Loop

### MLOps / LLMOps
- LangSmith, Phoenix, MLflow
- FastAPI + WebSocket, PostgreSQL (AsyncPostgresSaver), Docker Compose
- Cost governance (token-level + run-level), observabilidade distribuída

### Data & Backend
- Python (avançado), SQL, Spark, Airflow (experiência)
- React + Express (frontend/backend da Helix)

### Arquitetura & Liderança Técnica
- Trade-off analysis, ADRs, System Design de soluções GenAI em escala
- Governança de custo, resiliência (circuit breaker, retry policies), state versioning

---

## Projeto Principal: Helix — Multi-Agent Orchestration Platform

**Plataforma de produção para workflows de marketing B2B com agentes especializados.**

- **Arquitetura**: LangGraph State Machines + Supervisor (CEO Orchestrator) + Specialist Agents (Strategy, Content, SEO, Social, Visual, Review)
- **Diferenciadores de produção**:
  - Checkpoints persistentes com `AsyncPostgresSaver` + human approval
  - Dynamic Model Routing (Pro → Flash)
  - Hybrid Memory (Vector + Graph + Episodic)
  - Cost Tracking por run/agent + Impact Dashboard (cost vs value)
  - Evaluation Layer (LLM-as-Judge + Ragas)

**Impacto Projetado**:
- -78% no tempo de produção de campanhas
- -65% na dependência de agências externas
- Governança completa de custo e qualidade

**Repositório**: [Helix](https://github.com/peixotojeff/helix) *(privado — disponível sob NDA)*

**Artefatos Staff-level**:
- [Technical One-Pager](technical_one_pager.md)
- [15-min Presentation Deck](helix_15min_deck.md)
- Architecture Decision Records (ADRs)

---

## Experiência Relevante

**Grupo Studio** — *Análise de Power BI / GenAI Engineer*  
Fev/2026 – Presente  
- Liderança técnica do desenvolvimento da Helix (multi-agent platform)
- Integrações de marketing + automações avançadas

**BL BPO** — *Analista de MIS*  
Nov/2024 – Set/2025  
- Redução de 15% no desperdício de recursos via dashboards e análise

**ReConverte** — *Cientista de Dados*  
Jan/2023 – Nov/2023  
- Redução de 10% de churn com agente de IA personalizado no WhatsApp

---

## Formação & Certificações

- Formação Cientista de Dados — Alura (2023-2024)
- Cursos avançados em LangChain, LangGraph, LLMOps e RAG (em andamento)

---

## Próximos Passos na Carreira (2026-2027)

- Evoluir Helix para fully agentic (ReAct Planning Supervisor + memory reflection)
- Implementar A/B testing de prompts e routing policies
- Fortalecer portfólio com projetos open-source em Small Language Models e Multimodal Agents

---

**Aberto para oportunidades Senior/Staff em Generative AI.**

Vamos conversar sobre como construir sistemas de IA que realmente impactam o negócio.

📧 jefferson.-peixoto@hotmail.com.br  
🔗 [LinkedIn](https://www.linkedin.com/in/peixotojeff/)  
📍 Porto Alegre, RS — Remoto / Híbrido / Internacional
