# AGENTS.md

## Repository purpose

This repository maintains a curated classification of high-star GitHub projects starred by the `agzis` account. The primary artifact is `github-stars-10k-classified.md`.

## Editing rules

- Write reader-facing content in Chinese. Keep project names, repository names, product names, and common technical terms in their established form.
- Classify every project by its primary purpose and place it in exactly one category.
- Keep conceptually different layers separate. In particular:
  - Agent implementations are distinct from multi-Agent orchestration frameworks and Agent workbenches.
  - Terminal/session environments are distinct from local CLI/TUI utilities and service-access CLIs.
  - Learning resources, research/evaluation tools, datasets, and Notebook environments are separate categories.
  - Security/OSINT is separate from deployment, operations, and networking.
- Within each category, order projects by the recorded Star count in descending order.
- Preserve the four-column project table: project, Star, one-sentence introduction, and target audience.
- Use canonical GitHub repository URLs and concise, factual descriptions. Do not infer unsupported features.
- Treat Star counts and the collection date as a snapshot. Do not silently refresh them while making an unrelated classification or wording change.

## Consistency requirements

After changing classifications or project membership:

1. Update the category overview.
2. Update category numbers and declared project counts in headings.
3. Confirm that the overview count, section count, and unique project count agree.
4. Keep the overall total accurate and ensure no repository appears twice.
5. Review the usage notes when a change affects scope, methodology, or safety guidance.

## Validation

There is no build system or test suite. Validate changes by inspecting the Markdown and checking:

- headings are numbered consecutively;
- every section's declared count matches its table rows;
- the overview counts sum to the stated total;
- repository URLs are unique;
- Markdown tables remain well formed.

Before committing, run `git diff --check` and review `git diff`.

## Commit scope

- Keep commits focused on the requested classification, metadata, or documentation change.
- Do not add generated assets, caches, credentials, or unrelated files.
- Do not rewrite published history unless explicitly requested.
