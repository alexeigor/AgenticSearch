# Agentic Search

A curated collection of papers on agentic search — retrieval systems, benchmarks, and agents built around autonomous, multi-step search and research.

## Taxonomy

- **Retrieval Training** — training/adapting retrieval models specifically for use by search agents
- **Agent Systems** — end-to-end agentic research/search models and their training pipelines
- **Benchmarks & Evaluation** — datasets and evaluation methodology for agentic search

## Papers

| Date | Paper | Taxonomy |
|------|-------|----------|
| 2026-08 | [ITER: Interaction-Aware Retrieval for Agentic Search](https://arxiv.org/abs/2608.27912) | Retrieval Training |
| 2026-03 | [Learning to Retrieve from Agent Trajectories](https://arxiv.org/abs/2604.04949) | Retrieval Training |
| 2025-10 | [Tongyi DeepResearch Technical Report](https://arxiv.org/abs/2510.24701) | Agent Systems |

- **[ITER: Interaction-Aware Retrieval for Agentic Search](https://arxiv.org/abs/2608.27912)** (Chen et al.) — *2026-08 · Retrieval Training*
  A dense retriever for agent-based search that conditions on the main question, the agent's pre-search reasoning, and preceding sub-queries, rather than just the current query and results. Trained with trajectory-based signals where previously seen documents act as negatives, it gives an average relative improvement of 6.9% on InfoSeek-Eval and 15.4% on BrowseComp-Plus across multiple agent models.

- **[Learning to Retrieve from Agent Trajectories](https://arxiv.org/abs/2604.04949)** (Zhou et al.) — *2026-03 · Retrieval Training*
  Argues that retrieval models for agentic search should be trained directly on agent interaction data rather than human-centric signals. Introduces LRAT, which extracts training signals from agents' browsing actions and reasoning traces, improving evidence recall, task success, and efficiency across different agent architectures.

- **[Tongyi DeepResearch Technical Report](https://arxiv.org/abs/2510.24701)** (Tongyi DeepResearch Team) — *2025-10 · Agent Systems*
  Describes an agentic research model (~30.5B parameters, 3.3B active per inference step) trained via a fully-automated, human-label-free data pipeline with dedicated environments for each training stage. Achieves leading results on deep-research benchmarks including Humanity's Last Exam, BrowseComp, BrowseComp-ZH, and WebWalkerQA, with model and training framework released publicly.

## Contributing

Add new papers as a list entry with the title (linked to the arXiv page), authors, publication year-month, taxonomy category, and a 2-3 sentence summary. Also add a row to the table above and, if needed, a new category to the Taxonomy section.
