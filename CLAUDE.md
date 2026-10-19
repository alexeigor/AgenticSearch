# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A curated reading list of papers and blog posts on agentic search. There is no code, build, lint, or test step. `README.md` holds all of the content, and GitHub Pages renders it through Jekyll (`_config.yml`, `jekyll-theme-slate`).

## Adding an entry

Most changes add one paper to `README.md`. The rules below come from the README's Contributing section and the existing entries:

- Put the entry under the right `##` topic section (currently Retrieval, Search Agents, Deep Research, Evaluation Agentic Search). If you create a new section, add it to the Table of Contents at the top too, and keep Contributing as the last section.
- Format:
  ```
  - **Title**, Mon YYYY, [source](link) · [code](repo-link)
    A 2-3 sentence summary.
  ```
  - The source label is `arxiv` for arXiv papers. For blog posts it is the publisher's name (for example `Databricks`, `Exa`, `Chroma`, `Keenable`).
  - Add `· [code](...)` only when there is a public implementation repo.
  - The summary is indented two spaces on the next line and kept as one unwrapped line. It covers the core idea, the method, and the headline results or benchmarks.
- Within a section, entries are sorted by date, newest first.
- Leave one blank line between entries.
- If you change a convention, update the README's Contributing section too, so it stays in sync with this file.

## Commits

Commit messages follow the pattern `Add <paper/short name> under <Section>` (for example `Add Search-R1 paper under Retrieval`). Don't add a `Co-Authored-By: Claude` trailer.
