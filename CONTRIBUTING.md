# Contributing

Thank you for helping improve this community resource. This repository is a Markdown-only curated awesome list, not a data mirror, software platform, benchmark hosting service, or exhaustive bibliography.

The goal of these guidelines is to make community and automated pull requests easy to review.

## Quick Contribution Rules

- Add only publicly verifiable resources.
- Prefer one resource per pull request, or a small themed batch of up to five resources.
- Add concise awesome-list entries, not long descriptions.
- Link to an official, archival, publisher, project, institution, or clearly maintained source.
- Do not add datasets, copied benchmark files, PDFs, notebooks, scripts, generated data, or implementation artifacts.
- If access, license, symbolic component, task, or relevance is unclear, open an issue before adding the item to the main list.

## Where to Add a Resource

Use this decision path:

1. If the resource is a benchmark or dataset, add it to one primary subsection under `Benchmark Catalog` in `README.md`.
2. If the resource is a benchmark suite, shared task, benchmark generator, or evaluation campaign, add it under `Benchmark Suites and Generators`.
3. If the resource is primarily about metrics, methodology, benchmark design, or evaluation practice, add it under `Evaluation and Methodology` or `Surveys and Reading Lists`.
4. If the resource is relevant but the public link, data access, symbolic component, or benchmark status is unclear, open an issue with the available evidence instead of adding it directly.

Primary benchmark sections:

- `Concept Quality and Reasoning Shortcuts`
- `Visual and Abstract Reasoning`
- `Video, Temporal, and Physical Reasoning`
- `Vision-Language and Knowledge-Based VQA`
- `Language, Semantic Parsing, and Compositional Generalization`
- `Ontology and Knowledge Graph Reasoning`
- `Logic, Entailment, and Theorem Proving`
- `Program Synthesis and Executable Reasoning`
- `Robotics, Embodied Reasoning, and Planning`
- `Autonomous Driving and Safety-Constrained Reasoning`
- `Scientific and Domain-Specific Benchmarks`

## Entry Format

Use this one-line format for main list entries:

```markdown
- [Benchmark Name](https://official.example.org/) - One concise, neutral sentence. Tags: 🖼️ vision ✅ constraints 🔁 OOD 🟢 data+code.
```

Use the shortest accurate description possible. Avoid promotional wording.

## Required Information

Every main-list resource should have enough public documentation to verify:

- Benchmark or resource name.
- Official URL.
- Maintainer, institution, publisher, or project.
- One-sentence description.
- Task or evaluation purpose.
- Symbolic component, such as rules, ontology, Knowledge Graph, scene graph, program, proof, constraint, plan, SQL/SPARQL query, or concept labels.
- Modality, such as vision, language, video, Knowledge Graph, robotics, driving, scientific data, synthetic reasoning, or multimodal data.
- Main metrics, such as accuracy, F1, MRR, Hits@N, exact match, execution accuracy, success rate, proof quality, concept F1, concept collapse, OOD drop, or constraint satisfaction.
- Data/code/paper status.
- License, terms, or access status, if available.

## Tags

Use the README tag vocabulary exactly. Tags combine one compact symbol with a short label.

Modality and domain tags:

- 🖼️ vision
- 📝 language
- 🎥 video
- 🔊 audio
- 🕸️ KG
- 🤖 robotics
- 🚗 driving
- 🧪 science
- 🧩 synthetic
- 🔀 multimodal

Capability and status tags:

- 🧠 concepts
- ⚠️ shortcuts
- 🔁 OOD
- 🧰 generator
- ✅ constraints
- 🔍 proofs
- 📏 metrics
- 🟢 data+code
- 🟡 data
- 🔵 paper

Do not call something 🟢 data+code unless there is a clear public repository or implementation path. Use 🔵 paper when a benchmark is described in a publication but released data or code is not clearly available.

## Main List or Issue First

Add to the main list only when all of these are true:

- The URL is official, archival, institutionally reliable, or clearly maintained.
- The resource is directly useful for evaluating neuro-symbolic learning, reasoning, grounding, planning, symbolic faithfulness, concept quality, or constraint satisfaction.
- The task and evaluation purpose are clear.
- The symbolic component is clear or the entry states why the resource is neuro-symbolically relevant.
- The description can be supported by public documentation.

Open an issue first when:

- The resource was mentioned in a paper, talk, or notes but has no clear public landing page.
- The license, access status, data availability, symbolic component, or benchmark status is unclear.
- It may be useful but needs maintainer review before being presented as a benchmark.
- It is primarily a model, framework, course, survey, or bibliography rather than a benchmark.

## Automated PR Checklist

Automated pull requests should include this information in the PR body:

```markdown
## Resource

- Name:
- Official URL:
- Maintainer / institution:
- Proposed README section:
- Proposed tags:
- Task:
- Symbolic component:
- Metrics:
- Data/code/paper status:
- License / terms URL:
- Why it belongs:

## Verification

- [ ] I used an official, archival, publisher, institutional, or clearly maintained URL.
- [ ] I did not add datasets, copied benchmark files, scripts, notebooks, or generated artifacts.
- [ ] I checked whether the resource belongs in the main list or should be proposed through an issue first.
- [ ] I used the README tag vocabulary.
- [ ] I added a concise, neutral one-sentence description.
- [ ] I placed the resource in only one primary section.
```

## Scope Policy

Do not contribute:

- Mirrors of benchmark data or files.
- Copied tables, figures, benchmark samples, or long paper excerpts.
- Code, notebooks, workflows, package files, generated datasets, or implementation artifacts.
- Resources with no stable public documentation.
- Entries whose relevance depends only on a broad mention of "AI" or "reasoning" without a clear neuro-symbolic evaluation angle.

Respect benchmark licenses, dataset terms, citation expectations, and community norms. When in doubt, link to official documentation rather than copying content.

## Review Checklist

Maintainers can review a PR by checking:

- Does the PR touch only Markdown guidance/list files?
- Is each new URL official, archival, institutionally reliable, or clearly maintained?
- Is each new resource directly relevant to neuro-symbolic benchmarking?
- Is the task, symbolic component, and metric clear?
- Are tags accurate and from the README vocabulary?
- Is license or access information available or easy to find?
- Is the wording concise, neutral, and non-promotional?
- Does the PR avoid copied data, PDFs, scripts, notebooks, or implementation artifacts?
- Should the item be discussed in an issue before being added?

## Style Guide

- Use one line per resource.
- Keep descriptions short and factual.
- Use sentence case.
- Keep tags short and consistent.
- Do not overclaim.
- Use 🔵 paper when data or code release is unclear.
- Prefer official project pages, archival pages, publisher pages, or maintained repositories.
- Do not quote non-public notes, correspondence, restricted documents, or project materials.
