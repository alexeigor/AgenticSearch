# Agentic Search

A curated collection of papers on agentic search — retrieval systems, benchmarks, and agents built around autonomous, multi-step search and research.

## Table of Contents

- [Retrieval](#retrieval)
- [Deep Research](#deep-research)
- [Evaluation Agentic Search](#evaluation-agentic-search)

## Retrieval

- **ITER: Interaction-Aware Retrieval for Agentic Search**, Aug 2026, [arxiv](https://arxiv.org/abs/2608.27912)
  A dense retriever for agent-based search that conditions on the main question, the agent's pre-search reasoning, and preceding sub-queries, rather than just the current query and results. Trained with trajectory-based signals where previously seen documents act as negatives, it gives an average relative improvement of 6.9% on InfoSeek-Eval and 15.4% on BrowseComp-Plus across multiple agent models.

- **Learning to Retrieve from Agent Trajectories**, Mar 2026, [arxiv](https://arxiv.org/abs/2604.04949)
  Argues that retrieval models for agentic search should be trained directly on agent interaction data rather than human-centric signals. Introduces LRAT, which extracts training signals from agents' browsing actions and reasoning traces, improving evidence recall, task success, and efficiency across different agent architectures.

- **Chroma Context-1: Training a Self-Editing Search Agent**, Mar 2026, [Chroma](https://www.trychroma.com/research/context-1)
  A 20B-parameter model trained as a specialized search subagent for multi-hop retrieval, ranking relevant documents from large corpora for a downstream reasoning model rather than answering questions itself. Its key idea is "self-editing context" — discarding irrelevant retrieved documents mid-search to stay within bounded context windows — trained via RL with synthetic tasks across web, finance, legal, and email domains, matching much larger frontier models while running up to 10x faster; model weights and the data generation pipeline are released publicly.

- **s3: You Don't Need That Much Data to Train a Search Agent via RL**, May 2025, [arxiv](https://arxiv.org/abs/2505.14146)
  A model-agnostic RAG framework that decouples the searcher from the generator, training only the searcher via RL with a reward measuring improvement over baseline RAG performance rather than fine-tuning the whole LLM or optimizing retrieval metrics directly. Achieves superior results across multiple benchmarks using just 2,400 training samples — about 70x fewer than competing approaches.

## Deep Research

- **Tongyi DeepResearch Technical Report**, Oct 2025, [arxiv](https://arxiv.org/abs/2510.24701)
  Describes an agentic research model (~30.5B parameters, 3.3B active per inference step) trained via a fully-automated, human-label-free data pipeline with dedicated environments for each training stage. Achieves leading results on deep-research benchmarks including Humanity's Last Exam, BrowseComp, BrowseComp-ZH, and WebWalkerQA, with model and training framework released publicly.

## Evaluation Agentic Search

- **Q2D-Web: A Large-Scale Benchmark for Retrieval in Agentic RAG Systems**, Sep 2026, [arxiv](https://arxiv.org/abs/2609.08887)
  Introduces a 190M-document web corpus with 70k agentic search queries across ten languages, reformulated from real user queries to evaluate machine-written (rather than human-written) query reformulations. Benchmarking 13 retrievers shows model rankings stay consistent across judgment sets but diverge by domain, language, and query type, and the authors show subcorpus sampling via reciprocal rank fusion can approximate full-corpus evaluation while preserving ranking accuracy.

## Contributing

Add new papers under the relevant topic section (create a new `##` section if none fits) using the format:

```
- **Title**, Month Year, [arxiv](link)
  A 2-3 sentence summary.
```

Update the Table of Contents if you add a new section.
