# Helix — Technical Deep Dive (15-Minute Narrative)

**Documento para apresentação técnica (12-15 minutos)**  
**Autor:** Jefferson Peixoto | Maio 2026

---

## Introdução (1-2 min)

Olá, meu nome é Jefferson Peixoto. Hoje vou apresentar o **Helix**, a plataforma multi-agent que estou construindo no Grupo Studio para transformar a forma como fazemos marketing B2B.

O principal problema que estamos resolvendo é a dependência excessiva de processos manuais e agências externas, com alto tempo de entrega e pouca consistência de marca. Helix transforma um briefing de negócio em um workflow completo e auditável, com agentes especializados, supervisão humana e métricas claras de custo e qualidade.

---

## Contexto de Negócio (2 min)

No Grupo Studio, o time de marketing recebe dezenas de briefings por mês. O fluxo tradicional envolve múltiplos handoffs, revisão manual e produção externa, levando vários dias.

**Objetivo do Helix:**  
Reduzir o tempo médio de produção para menos de 2 horas em campanhas comuns, mantendo ou elevando a qualidade, com total governança.

---

## Arquitetura Geral (3 min)

Helix é construída nativamente sobre **LangGraph**, que oferece um modelo de state machine poderoso. Cada squad é um StateGraph, com um **CEO Orchestrator (Supervisor)** responsável por planejar, rotear e coordenar agentes especialistas (Strategy, Content, SEO, Social, Visual, Review, etc.).

**Decisões-chave de arquitetura:**
- **LangGraph** ao invés de CrewAI/AutoGen: necessidade de checkpoints duráveis e human-in-the-loop.
- **AsyncPostgresSaver**: permite pausar runs para aprovação humana e retomar mesmo após restart do serviço.
- **Dynamic Model Routing**: tarefas complexas vão para Gemini 2.5 Pro, tarefas simples para Flash — com fallback automático.
- **Hybrid Memory**: Qdrant (vetorial), Neo4j (grafos de relacionamento) e Cognee (camada semântica).

---

## Governança de Custo e Qualidade (3 min)

Um dos maiores riscos em produção com GenAI é o custo descontrolado. No Helix implementei:

- `CostTrackingCallback`: rastreia tokens e custo por call, agente, run e squad.
- Impact Dashboard: correlaciona custo × score de qualidade × horas economizadas.
- Evaluation Layer: LLM-as-Judge + Ragas para medir relevance, brand voice, faithfulness e actionability.

---

## Desafios Técnicos e Trade-offs (3 min)

- **Resiliência:** Implementei retry por node, failure-aware routing e planejo circuit breakers.
- **Memory:** Decidi por abordagem híbrida porque marketing exige tanto similaridade semântica quanto compreensão de relacionamentos de negócio.
- **Human-in-the-Loop:** Essencial para aprovação final, mas complexo de implementar com estado consistente.

---

## Roadmap Técnico Atual (2 min)

Próximos 4-6 semanas:
- Evoluir o Supervisor para padrão ReAct + Planning
- Implementar agentic metrics (intervention rate, approval rate, turns to completion)
- Adicionar budget alerts e adaptive routing
- Memory reflection loop pós-aprovação

---

## Conclusão e Competências Demonstradas (1-2 min)

Helix representa meu nível atual de maturidade técnica: capacidade de projetar, implementar e operar sistemas GenAI complexos em ambiente de produção, com forte alinhamento entre tecnologia e impacto de negócio.

Este projeto me permite demonstrar competências Staff-level em:
- Arquitetura de Multi-Agent Systems
- LLMOps (custo, avaliação, observabilidade)
- System Design e trade-off decisions
- Liderança técnica em projetos end-to-end

Estou à disposição para perguntas técnicas ou demonstração ao vivo.

---
*Documento ideal para entrevistas Sênior/Staff ou apresentações internas.*
