# Agentic Search

A curated collection of papers on agentic search — retrieval systems, benchmarks, and agents built around autonomous, multi-step search and research.

## Table of Contents

- [Retrieval](#retrieval)
- [Deep Research](#deep-research)
- [Evaluation Agentic Search](#evaluation-agentic-search)

## Retrieval

- **ITER: Interaction-Aware Retrieval for Agentic Search**, Aug 2026, [arxiv](https://arxiv.org/abs/2608.27912) · [code](https://github.com/ielab/ITER)
  A dense retriever for agent-based search that conditions on the main question, the agent's pre-search reasoning, and preceding sub-queries, rather than just the current query and results. Trained with trajectory-based signals where previously seen documents act as negatives, it gives an average relative improvement of 6.9% on InfoSeek-Eval and 15.4% on BrowseComp-Plus across multiple agent models.

- **Harness-1: Reinforcement Learning for Search Agents with State-Externalizing Harnesses**, Jun 2026, [arxiv](https://arxiv.org/abs/2606.02373) · [code](https://github.com/pat-jj/harness-1)
  Separates state management from policy decisions in search agents: a stateful harness handles bookkeeping (a candidate pool, importance-tagged curated set, evidence links, verification records, deduplicated observations, budget-aware context rendering) while a 20B RL-trained policy focuses on high-level decisions — what to search for, which documents matter, what to verify, when to stop. Across eight retrieval benchmarks it reaches 0.730 average curated recall, beating the next-best open search subagent by +11.4 points, with especially strong generalization on held-out transfer benchmarks.

- **3x Faster Search: Parallel Test-Time Scaling with Instructed-Retriever-1**, Jun 2026, [Databricks](https://www.databricks.com/blog/3x-faster-search-parallel-test-time-scaling-instructed-retriever-1)
  Introduces Instructed-Retriever-1, a single retrieval-specialized model that runs query generation (broadening search scope) and multi-pivot reranking (improving precision) in parallel instead of sequential agent reasoning, cutting search time by over 3x and halving answer generation time (~2s time-to-first-token) in Databricks' Knowledge Assistant. Trained on synthetic enterprise-style environments and served with FP8 quantization, speculative decoding, and a Mixture-of-Experts architecture, it matches Claude Sonnet 4.5 quality at much lower latency.

- **How Search Quality Shapes RL Outcomes**, May 2026, [Exa](https://exa.ai/blog/rl-search-outcomes)
  Compares RL-trained search agents using Exa's search engine versus a Google SERP baseline with all else held constant, finding Exa-trained agents reach higher pass@k across benchmarks (often beating larger untrained 235B models) while needing 20% fewer tokens and 62% fewer search calls, because Exa surfaces correct answers 10.7% more often per call. The efficiency gains hold even when agents are evaluated with a different search backend at inference time, across MuSiQue, HotpotQA, and out-of-distribution benchmarks like SimpleQA, FRAMES, and 2WikiMultihopQA.

- **Beyond Semantic Similarity: Rethinking Retrieval for Agentic Search via Direct Corpus Interaction**, May 2026, [arxiv](https://arxiv.org/abs/2605.05242) · [code](https://github.com/DCI-Agent/DCI-Agent-Lite)
  Challenges the single-shot embedding-and-vector-index retrieval pipeline, proposing direct corpus interaction (DCI) where agents search raw corpora with general-purpose tools like grep and file operations instead of a fixed semantic retriever. Effective across BRIGHT and BEIR benchmarks, showing retrieval quality depends not just on an agent's reasoning ability but on the resolution of the interface it uses to access the corpus.

- **Learning to Retrieve from Agent Trajectories**, Mar 2026, [arxiv](https://arxiv.org/abs/2604.04949) · [code](https://github.com/Yuqi-Zhou/LRAT)
  Argues that retrieval models for agentic search should be trained directly on agent interaction data rather than human-centric signals. Introduces LRAT, which extracts training signals from agents' browsing actions and reasoning traces, improving evidence recall, task success, and efficiency across different agent architectures.

- **Chroma Context-1: Training a Self-Editing Search Agent**, Mar 2026, [Chroma](https://www.trychroma.com/research/context-1) · [code](https://github.com/chroma-core/context-1-data-gen)
  A 20B-parameter model trained as a specialized search subagent for multi-hop retrieval, ranking relevant documents from large corpora for a downstream reasoning model rather than answering questions itself. Its key idea is "self-editing context" — discarding irrelevant retrieved documents mid-search to stay within bounded context windows — trained via RL with synthetic tasks across web, finance, legal, and email domains, matching much larger frontier models while running up to 10x faster; model weights and the data generation pipeline are released publicly.

- **Instructed Retriever: Unlocking System-Level Reasoning in Search Agents**, Jan 2026, [Databricks](https://www.databricks.com/blog/instructed-retriever-unlocking-system-level-reasoning-search-agents)
  Proposes an architecture that propagates system specifications — instructions, examples, and index schema — through every stage of the search pipeline, letting agents follow complex instructions and reason across heterogeneous sources via query decomposition, relevance assessment, and metadata-to-filter translation. On the new StaRK-Instruct benchmark it achieves 35–50% higher recall than basic retrieval, and deployed in Databricks' Agent Bricks Knowledge Assistant it delivers 70%+ gains over a simple RAG baseline, with fine-tuned smaller models matching larger proprietary models.

- **s3: You Don't Need That Much Data to Train a Search Agent via RL**, May 2025, [arxiv](https://arxiv.org/abs/2505.14146) · [code](https://github.com/pat-jj/s3)
  A model-agnostic RAG framework that decouples the searcher from the generator, training only the searcher via RL with a reward measuring improvement over baseline RAG performance rather than fine-tuning the whole LLM or optimizing retrieval metrics directly. Achieves superior results across multiple benchmarks using just 2,400 training samples — about 70x fewer than competing approaches.

- **Search-R1: Training LLMs to Reason and Leverage Search Engines with Reinforcement Learning**, Mar 2025, [arxiv](https://arxiv.org/abs/2503.09516) · [code](https://github.com/PeterGriffinJin/Search-R1)
  Trains an LLM end-to-end with RL to interleave step-by-step reasoning with autonomously generated search queries against real-time retrieval, using retrieved-token masking for stable training and a simple outcome-based reward rather than process supervision. Supports multiple RL algorithms (PPO, GRPO, REINFORCE), backbone LLMs, and search engines, improving over comparable RAG baselines by 41% on Qwen2.5-7B and 20% on Qwen2.5-3B across seven QA datasets.

## Deep Research

- **Tongyi DeepResearch Technical Report**, Oct 2025, [arxiv](https://arxiv.org/abs/2510.24701) · [code](https://github.com/Alibaba-NLP/DeepResearch)
  Describes an agentic research model (~30.5B parameters, 3.3B active per inference step) trained via a fully-automated, human-label-free data pipeline with dedicated environments for each training stage. Achieves leading results on deep-research benchmarks including Humanity's Last Exam, BrowseComp, BrowseComp-ZH, and WebWalkerQA, with model and training framework released publicly.

## Evaluation Agentic Search

- **Q2D-Web: A Large-Scale Benchmark for Retrieval in Agentic RAG Systems**, Sep 2026, [arxiv](https://arxiv.org/abs/2609.08887)
  Introduces a 190M-document web corpus with 70k agentic search queries across ten languages, reformulated from real user queries to evaluate machine-written (rather than human-written) query reformulations. Benchmarking 13 retrievers shows model rankings stay consistent across judgment sets but diverge by domain, language, and query type, and the authors show subcorpus sampling via reciprocal rank fusion can approximate full-corpus evaluation while preserving ranking accuracy.

## Contributing

Add new papers under the relevant topic section (create a new `##` section if none fits) using the format:

```
- **Title**, Month Year, [arxiv](link) · [code](repo-link)
  A 2-3 sentence summary.
```

If the paper has a public code/implementation repo, include a `[code](link)` link after the source link (omit it otherwise).

Within each section, entries are sorted by date descending (newest first).

Update the Table of Contents if you add a new section.
