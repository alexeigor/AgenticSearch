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

## Deep Research

- **Tongyi DeepResearch Technical Report**, Oct 2025, [arxiv](https://arxiv.org/abs/2510.24701)
  Describes an agentic research model (~30.5B parameters, 3.3B active per inference step) trained via a fully-automated, human-label-free data pipeline with dedicated environments for each training stage. Achieves leading results on deep-research benchmarks including Humanity's Last Exam, BrowseComp, BrowseComp-ZH, and WebWalkerQA, with model and training framework released publicly.

## Evaluation Agentic Search

_No papers yet — contributions welcome._

## Contributing

Add new papers under the relevant topic section (create a new `##` section if none fits) using the format:

```
- **Title**, Month Year, [arxiv](link)
  A 2-3 sentence summary.
```

Update the Table of Contents if you add a new section.
