# Jefferson Peixoto — Technical One-Pager

**Data & AI Engineer | GenAI Specialist | Multi-Agent Systems**  
**Foco:** Arquitetura de Soluções Agenticas em Produção | LLMOps | Impacto de Negócio Mensurável  
**Localização:** Porto Alegre, RS | Open to remote / international  

---

## Professional Summary

Engenheiro de Dados & IA com +3 anos de experiência prática, evoluindo rapidamente para papéis Sênior/Staff. Especializado na construção de **sistemas multi-agent production-grade** usando LangGraph, com forte ênfase em governança de custo, avaliação automática, human-in-the-loop e integração com ferramentas de marketing/CRM.

**Maior projeto atual:**  
**Helix** — Plataforma nativa de orquestração multi-agent para operações de marketing B2B no Grupo Studio.

---

## Helix — Flagship Project (Staff-level)

**Descrição:**  
Plataforma LangGraph-native que transforma briefings de negócio não-estruturados em workflows completos (planejamento → pesquisa → criação → revisão → aprovação → archive) com rastreabilidade total.

**Principais Conquistas Técnicas:**

- **Arquitetura Agentica Avançada:**  
  Supervisor (CEO Orchestrator) + Specialist Agents com routing dinâmico. Escolhi LangGraph por suporte nativo a checkpoints, interrupts/resume e controle explícito de estado (superior a CrewAI/AutoGen).

- **Governança de Custo & Performance:**  
  `CostTrackingCallback` granular (por run/agent/modelo). Dynamic model routing (Gemini 2.5 Pro → Flash) com fallback chain. Impact API correlacionando custo × qualidade × horas economizadas.

- **Memory Híbrido:**  
  Combinação estratégica de **Qdrant** (vector), **Neo4j** (graph relationships) e **Cognee** (semantic layer) — essencial para domínio de marketing B2B.

- **Human-in-the-Loop Production:**  
  Implementação robusta usando `AsyncPostgresSaver` + interrupt/resume, permitindo aprovação humana sem perda de estado.

- **Evaluation Framework:**  
  LLM-as-Judge multidimensional + Ragas. Métricas de qualidade (brand voice, actionability, faithfulness) e agentic metrics (intervention rate, approval rate).

**Impacto Projetado:**  
- Redução de ~78% no tempo de produção de campanhas  
- Redução de ~65% na dependência de agências externas  
- Governança completa de custo e qualidade

**Stack Principal:** Python, LangGraph, LangChain, FastAPI, PostgreSQL, Neo4j, Qdrant, React, Docker, Gemini 2.5, OpenRouter.

---

## Technical Competencies (Staff Level)

- **GenAI:** Multi-agent orchestration, RAG híbrido, Fine-tuning strategies, Agentic workflows, Evaluation (Ragas + LLM Judge), Guardrails
- **MLOps/LLMOps:** LangSmith, Phoenix, MLflow, cost governance, observability, resilience (retries, circuit breakers)
- **Engenharia:** Python avançado, SQL, ETL/ELT, Airflow (conhecimento), FastAPI, Docker
- **Soft Skills Técnicas:** System Design, trade-off analysis (custo × qualidade × velocidade), technical leadership, storytelling executivo

---

## Education & Continuous Learning

- Formação Cientista de Dados — Alura (2023-2024)
- Certificações: Pandas, Data Visualization, Estatística com Python
- Aprendizado ativo em: Reasoning Models, Small Language Models, Advanced Agentic AI (2026)

**GitHub:** [sob solicitação]  
**LinkedIn:** linkedin.com/in/peixotojeff  
**Contato:** jefferson.peixoto@hotmail.com

---
