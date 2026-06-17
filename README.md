# Awesome Neuro-Symbolic Benchmarks

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![License: CC BY 4.0](https://img.shields.io/badge/license-CC%20BY%204.0-green.svg)](https://creativecommons.org/licenses/by/4.0/) [![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](#contributing)

A curated catalog of benchmarks, datasets, suites, tasks, and evaluation resources for neuro-symbolic AI.

Neuro-symbolic benchmarks connect learned perception or language processing with explicit symbolic structure: rules, ontologies, Knowledge Graphs, scene graphs, functional programs, proofs, SQL/SPARQL queries, constraints, plans, or concept labels.

## Contents

- [How to Read](#how-to-read)
- [Benchmark Catalog](#benchmark-catalog)
- [Benchmark Suites and Generators](#benchmark-suites-and-generators)
- [Evaluation and Methodology](#evaluation-and-methodology)
- [Surveys and Reading Lists](#surveys-and-reading-lists)
- [Gaps](#gaps)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

<a id="how-to-read"></a>

## 🔎 How to Read

Tags are intentionally compact:

- Modality and domain: `🖼️ vision`, `📝 language`, `🎥 video`, `🔊 audio`, `🕸️ KG`, `🤖 robotics`, `🚗 driving`, `🧪 science`, `🧩 synthetic`, `🔀 multimodal`.
- Capability: `🧠 concepts`, `⚠️ shortcuts`, `🔁 OOD`, `🧰 generator`, `✅ constraints`, `🔍 proofs`, `📏 metrics`.
- Availability: `🟢 data+code`, `🟡 data`, `🔵 paper`.

Good entries should expose the benchmark's task, symbolic component, and main evaluation signal. If a benchmark fits several places, it is listed where it is most useful for quick discovery.

<a id="benchmark-catalog"></a>

## 📚 Benchmark Catalog

### Concept Quality and Reasoning Shortcuts

- [BDD-OIA](https://unitn-sml.github.io/rsbench/) - Real autonomous-driving action-decision benchmark with concept annotations and traffic-rule constraints. Tags: `🚗 driving` `🖼️ vision` `🧠 concepts` `⚠️ shortcuts` `✅ constraints` `🟡 data`.
- [CLE4EVR](https://unitn-sml.github.io/rsbench/) - CLEVR-inspired 3D scene reasoning benchmark for concept collapse and reasoning shortcut analysis. Tags: `🖼️ vision` `🧩 synthetic` `🧠 concepts` `⚠️ shortcuts` `🔁 OOD`.
- [Kand-Logic](https://unitn-sml.github.io/rsbench/) - Kandinsky-pattern visual reasoning task with shape/color concepts and logical rules. Tags: `🖼️ vision` `🧩 synthetic` `🧠 concepts` `⚠️ shortcuts` `🧰 generator`.
- [MNAdd-EvenOdd](https://unitn-sml.github.io/rsbench/) - MNIST addition variant designed for shortcut, OOD, and continual-learning tests. Tags: `🧩 synthetic` `🧠 concepts` `⚠️ shortcuts` `🔁 OOD`.
- [MNAdd-Half](https://unitn-sml.github.io/rsbench/) - MNIST addition variant with guaranteed reasoning shortcuts. Tags: `🧩 synthetic` `🧠 concepts` `⚠️ shortcuts`.
- [MNLogic](https://unitn-sml.github.io/rsbench/) - Logical formula satisfaction over MNIST-style visual concepts. Tags: `🧩 synthetic` `✅ constraints` `⚠️ shortcuts` `🧰 generator`.
- [MNMath](https://unitn-sml.github.io/rsbench/) - Arithmetic learning-and-reasoning task based on systems of MNIST equations. Tags: `🧩 synthetic` `🧠 concepts` `⚠️ shortcuts` `🧰 generator`.
- [Reasoning Shortcut Analysis](https://arxiv.org/abs/2305.19951) - Paper formalizing shortcut behavior in neuro-symbolic predictors and concept-based models. Tags: `🧠 concepts` `⚠️ shortcuts` `📏 metrics` `🔵 paper`.
- [SDD-OIA](https://unitn-sml.github.io/rsbench/) - Synthetic traffic-scene benchmark with configurable OOD scenarios and traffic rules. Tags: `🚗 driving` `🖼️ vision` `⚠️ shortcuts` `🔁 OOD` `🧰 generator` `🟢 data+code`.

### Visual and Abstract Reasoning

- [ARC-AGI](https://github.com/fchollet/ARC-AGI) - Grid-based abstraction benchmark for few-shot visual program induction. Tags: `🖼️ vision` `🧩 synthetic` `🔁 OOD` `🟢 data+code`.
- [Bongard-LOGO](https://github.com/NVlabs/Bongard-LOGO) - Synthetic Bongard problem generator for visual concept and analogy learning. Tags: `🖼️ vision` `🧩 synthetic` `🧰 generator` `🟢 data+code`.
- [CLEVR](https://cs.stanford.edu/people/jcjohns/clevr/) - Diagnostic visual reasoning benchmark with scene graphs and functional programs. Tags: `🖼️ vision` `🔀 multimodal` `🧩 synthetic` `🟡 data`.
- [CLEVR-CoGenT](https://cs.stanford.edu/people/jcjohns/clevr/) - CLEVR split for compositional generalization over color-shape combinations. Tags: `🖼️ vision` `🔁 OOD` `🧩 synthetic` `🟡 data`.
- [GQA](https://cs.stanford.edu/people/dorarad/gqa/about.html) - Real-image VQA benchmark grounded in scene graphs and functional programs. Tags: `🖼️ vision` `📝 language` `🔀 multimodal` `🟡 data`.
- [KANDY](https://arxiv.org/abs/2402.17431) - Kandinsky-pattern benchmark for incremental neuro-symbolic learning and rule compositionality. Tags: `🖼️ vision` `🧩 synthetic` `🧠 concepts` `🔁 OOD` `🔵 paper`.
- [NLVR / NLVR2](https://lil.nlp.cornell.edu/nlvr/) - Natural-language visual reasoning datasets over images and structured visual worlds. Tags: `🖼️ vision` `📝 language` `🔁 OOD` `🟡 data`.
- [PGM](https://github.com/google-deepmind/abstract-reasoning-matrices) - Procedurally generated matrix reasoning benchmark for abstract visual rules. Tags: `🖼️ vision` `🧩 synthetic` `🔁 OOD` `🟢 data+code`.
- [RAVEN](https://wellyzhang.github.io/project/raven.html) - Raven-style visual analogy benchmark with structured relational rules. Tags: `🖼️ vision` `🧩 synthetic` `🔁 OOD` `🟡 data`.
- [Visual Genome](https://arxiv.org/abs/1602.07332) - Dense image annotation resource with objects, attributes, relationships, and scene-graph style structure. Tags: `🖼️ vision` `📝 language` `🕸️ KG` `🟡 data`.

### Video, Temporal, and Physical Reasoning

- [CLEVRER](https://arxiv.org/abs/1910.01442) - Video benchmark for physical events, collisions, causality, prediction, and counterfactuals. Tags: `🎥 video` `🧩 synthetic` `🔁 OOD` `🔵 paper`.
- [IntPhys](https://arxiv.org/abs/1803.07616) - Intuitive physics benchmark based on possible/impossible event discrimination. Tags: `🎥 video` `🖼️ vision` `🧩 synthetic` `🔵 paper`.
- [PHYRE](https://arxiv.org/abs/1908.05656) - 2D physical reasoning benchmark with action-based puzzle solving. Tags: `🎥 video` `🧩 synthetic` `🔁 OOD` `🟢 data+code`.
- [Physion](https://physion-benchmark.github.io/) - Physical prediction benchmark using simulated videos of object interactions. Tags: `🎥 video` `🧩 synthetic` `📏 metrics` `🟡 data`.
- [SUTD-TrafficQA](https://github.com/SUTDCV/SUTD-TrafficQA) - Traffic video question-answering benchmark for temporal road-event reasoning. Tags: `🎥 video` `🚗 driving` `📝 language` `🟡 data`.

### Vision-Language and Knowledge-Based VQA

- [A-OKVQA](https://arxiv.org/abs/2206.01718) - Outside-knowledge VQA benchmark with questions requiring commonsense and world knowledge. Tags: `🖼️ vision` `📝 language` `🔀 multimodal` `🔍 proofs` `🟡 data`.
- [FVQA](https://github.com/GT-Vision-Lab/VQA_Lol_FVQA) - Fact-based VQA benchmark connecting visual recognition with supporting knowledge triples. Tags: `🖼️ vision` `📝 language` `🕸️ KG` `🔍 proofs` `🟡 data`.
- [KVQA](https://malllabiisc.github.io/resources/kvqa/) - Knowledge-aware VQA benchmark over named entities and Knowledge Graph facts. Tags: `🖼️ vision` `📝 language` `🕸️ KG` `🔀 multimodal` `🟡 data`.
- [OK-VQA](https://okvqa.allenai.org/) - VQA benchmark where answering requires external knowledge beyond the image. Tags: `🖼️ vision` `📝 language` `🔀 multimodal` `🟡 data`.
- [Retrieval-Augmented VQA](https://github.com/LinWeizheDragon/Retrieval-Augmented-Visual-Question-Answering) - Resource for retrieval-based outside-knowledge visual question answering. Tags: `🖼️ vision` `📝 language` `🕸️ KG` `🟢 data+code`.
- [Visual Dialog](https://visualdialog.org/) - Visual conversational QA benchmark useful for dialogue state, coreference, and grounded reasoning. Tags: `🖼️ vision` `📝 language` `🔀 multimodal` `🟡 data`.
- [VQA v2.0](https://visualqa.org/) - Balanced visual question-answering benchmark reducing simple language-prior shortcuts. Tags: `🖼️ vision` `📝 language` `🔀 multimodal` `🟡 data`.

### Language, Semantic Parsing, and Compositional Generalization

- [bAbI](https://research.facebook.com/downloads/babi/) - Synthetic text reasoning tasks for memory, deduction, induction, and multi-hop QA. Tags: `📝 language` `🧩 synthetic` `🔁 OOD` `🟡 data`.
- [CFQ](https://research.google/blog/measuring-compositional-generalization/) - Compositional Freebase Questions benchmark for mapping language to SPARQL. Tags: `📝 language` `🕸️ KG` `🔁 OOD` `🟡 data`.
- [CLUTRR](https://github.com/facebookresearch/clutrr) - Story-based family-relation benchmark for systematic relational reasoning. Tags: `📝 language` `🧩 synthetic` `🔁 OOD` `🟢 data+code`.
- [COGS](https://github.com/najoungkim/COGS) - Compositional generalization benchmark from English sentences to logical forms. Tags: `📝 language` `🧩 synthetic` `🔁 OOD` `🟢 data+code`.
- [GeoQuery](https://github.com/jkkummerfeld/text2sql-data) - Classic semantic parsing benchmark for geography questions and executable queries. Tags: `📝 language` `🧩 synthetic` `🟡 data`.
- [HotpotQA](https://hotpotqa.github.io/) - Multi-hop QA benchmark with supporting facts for evidence-chain evaluation. Tags: `📝 language` `🔍 proofs` `🟡 data`.
- [SCAN](https://github.com/brendenlake/SCAN) - Command-to-action benchmark for compositional generalization. Tags: `📝 language` `🧩 synthetic` `🔁 OOD` `🟢 data+code`.

### Ontology and Knowledge Graph Reasoning

- [FB15k-237](https://www.microsoft.com/en-us/download/details.aspx?id=52312) - Freebase-derived Knowledge Graph completion benchmark with reduced inverse-relation leakage. Tags: `🕸️ KG` `📏 metrics` `🟡 data`.
- [WN18RR](https://github.com/TimDettmers/ConvE) - WordNet-derived Knowledge Graph completion benchmark with inverse-relation artifacts reduced. Tags: `🕸️ KG` `📏 metrics` `🟡 data`.
- [YAGO3-10](https://yago-knowledge.org/downloads/yago-3) - YAGO-derived Knowledge Graph completion benchmark focused on typed entities and relations. Tags: `🕸️ KG` `📏 metrics` `🟡 data`.

### Logic, Entailment, and Theorem Proving

- [EntailmentBank](https://allenai.org/data/entailmentbank) - Natural-language QA benchmark with structured entailment-tree explanations. Tags: `📝 language` `🔍 proofs` `✅ constraints` `🟡 data`.
- [HolStep](https://arxiv.org/abs/1703.00426) - Higher-order logic theorem-proving dataset for premise selection and proof-step prediction. Tags: `✅ constraints` `🧩 synthetic` `🔵 paper`.
- [HOList](https://arxiv.org/abs/1904.03241) - Higher-order theorem-proving environment and benchmark derived from HOL Light. Tags: `✅ constraints` `🟢 data+code`.
- [LeanDojo](https://github.com/lean-dojo/LeanDojo) - Toolkit and benchmark environment for Lean theorem proving and premise selection. Tags: `✅ constraints` `🟢 data+code`.
- [miniF2F](https://github.com/openai/miniF2F) - Formal mathematics benchmark across proof assistants. Tags: `✅ constraints` `🔍 proofs` `🟢 data+code`.
- [ProofWriter](https://allenai.org/data/proofwriter) - Natural-language rule reasoning benchmark with generated implications and proofs. Tags: `📝 language` `🔍 proofs` `✅ constraints` `🟡 data`.
- [TPTP](https://www.tptp.org/) - Formal problem library and infrastructure for automated theorem proving. Tags: `✅ constraints` `🧩 synthetic` `📏 metrics` `🟢 data+code`.

### Program Synthesis and Executable Reasoning

- [DeepCoder](https://www.microsoft.com/en-us/research/publication/deepcoder-learning-write-programs/) - Program synthesis benchmark for learning small programs from input-output examples. Tags: `🧩 synthetic` `🔵 paper`.
- [DreamCoder](https://github.com/ellisk42/ec) - Program-learning benchmark collection for synthesizing programs and reusable abstractions. Tags: `🧩 synthetic` `🔁 OOD` `🟢 data+code`.
- [Karel](https://github.com/carpedm20/karel) - Program synthesis dataset for inferring Karel programs from grid examples. Tags: `🧩 synthetic` `🟢 data+code`.
- [Spider](https://yale-lily.github.io/spider) - Cross-domain text-to-SQL benchmark for executable database reasoning. Tags: `📝 language` `🧩 synthetic` `🟡 data`.
- [WikiSQL](https://github.com/salesforce/WikiSQL) - Large semantic parsing corpus for natural-language interfaces to tables. Tags: `📝 language` `🧩 synthetic` `🟢 data+code`.

### Robotics, Embodied Reasoning, and Planning

- [AI2-THOR](https://ai2thor.allenai.org/) - Interactive 3D environment for object-centric embodied AI tasks. Tags: `🤖 robotics` `🖼️ vision` `🟢 data+code`.
- [ALFRED](https://askforalfred.com/) - Embodied household instruction-following benchmark with language, vision, and action plans. Tags: `🤖 robotics` `🖼️ vision` `📝 language` `🟡 data`.
- [ALFWorld](https://alfworld.github.io/) - Text and embodied environment aligning household tasks with symbolic planning. Tags: `🤖 robotics` `📝 language` `✅ constraints` `🟢 data+code`.
- [BabyAI](https://github.com/mila-iqia/babyai/tree/iclr19) - Instruction-following gridworld with symbolic verifier and compositional language. Tags: `🤖 robotics` `📝 language` `✅ constraints` `🟢 data+code`.
- [CausalWorld](https://github.com/rr-learning/CausalWorld) - Robotic manipulation benchmark for causal structure and transfer learning. Tags: `🤖 robotics` `🧩 synthetic` `🔁 OOD` `🟢 data+code`.
- [LogiCity](https://sairlab.org/datasets/logicity/) - Urban simulation benchmark with customizable first-order logic rules for dynamic agents. Tags: `🤖 robotics` `🚗 driving` `✅ constraints` `🔁 OOD` `🟢 data+code`.
- [MiniGrid](https://github.com/Farama-Foundation/Minigrid) - Configurable gridworld environment for symbolic goals, instruction following, and planning. Tags: `🤖 robotics` `📝 language` `🧩 synthetic` `🟢 data+code`.
- [Neuro-Symbolic Action Planning](https://michaal94.github.io/project/ns-ap) - Visual manipulation benchmark with symbolic subgoals and action planning. Tags: `🤖 robotics` `🖼️ vision` `✅ constraints` `🔵 paper`.

### Autonomous Driving and Safety-Constrained Reasoning

- [ROAD-R](https://arxiv.org/abs/2210.01597) - Road-event benchmark with logical requirements for autonomous-driving perception. Tags: `🚗 driving` `🎥 video` `✅ constraints` `🟡 data`.
- [SUTD-TrafficQA](https://github.com/SUTDCV/SUTD-TrafficQA) - Traffic-event video QA benchmark. Tags: `🚗 driving` `🎥 video` `📝 language` `🟡 data`.

### Scientific and Domain-Specific Benchmarks

- [LLMs4OL Domain Tracks](https://sites.google.com/view/llms4ol2025) - Ontology learning tasks across biomedicine, materials science, earth science, medicine, food, plants, chemistry, and web domains. Tags: `🧪 science` `🕸️ KG` `📝 language` `📏 metrics`.
- [OAEI Domain Tracks](https://oaei.ontologymatching.org/) - Ontology alignment tracks covering biomedical, biodiversity, ecology, food, pharmacogenomics, archaeology, circular economy, and Knowledge Graph settings. Tags: `🧪 science` `🕸️ KG` `📏 metrics` `🟢 data+code`.

<a id="benchmark-suites-and-generators"></a>

## 🧰 Benchmark Suites and Generators

- [rsbench](https://unitn-sml.github.io/rsbench/) - Neuro-symbolic suite for concept quality, reasoning shortcuts, OOD splits, and formal shortcut counting; code is on [GitHub](https://github.com/unitn-sml/rsbench). Tags: `🧠 concepts` `⚠️ shortcuts` `🔁 OOD` `🧰 generator` `✅ constraints` `🟢 data+code`.
- [LLMs4OL](https://sites.google.com/view/llms4ol2025) - Shared-task benchmark suite for ontology learning with large language models. Tags: `🕸️ KG` `📝 language` `📏 metrics`.
- [OAEI](https://oaei.ontologymatching.org/) - Long-running ontology and Knowledge Graph alignment evaluation initiative. Tags: `🕸️ KG` `📏 metrics` `🟢 data+code`.
- [KANDY](https://arxiv.org/abs/2402.17431) - Benchmark framework and curricula for incremental neuro-symbolic learning with Kandinsky patterns. Tags: `🖼️ vision` `🧩 synthetic` `🧠 concepts` `🧰 generator` `🔵 paper`.

<a id="evaluation-and-methodology"></a>

## 📏 Evaluation and Methodology

### Common Metrics

- Classification: Accuracy, precision, recall, F1, macro-F1, micro-F1.
- Ranking: MRR, Hits@1/3/10.
- Structured prediction: Exact match, logical-form accuracy, execution accuracy, denotation accuracy.
- Embodied tasks: Success rate, goal-conditioned success, sample efficiency, plan validity.
- Explanations and proofs: Proof accuracy, proof quality, entailment-tree correctness, premise selection precision/recall.

### Neuro-Symbolic Checks

- Are dataset, task, symbolic component, and metric explicit?
- Are concept labels or intermediate symbolic states available?
- Does the benchmark test OOD, compositional, counterfactual, continual, or small-data behavior?
- Can models be evaluated for symbolic consistency, constraint satisfaction, logical validity, or proof faithfulness?
- Can the benchmark detect concept collapse, concept confusion, reasoning shortcuts, or neural/symbolic component sensitivity?
- Are provenance, license, version, splits, and maintenance status clear?

<a id="surveys-and-reading-lists"></a>

## 📖 Surveys and Reading Lists

- [A Neuro-Symbolic Benchmark Suite for Concept Quality and Reasoning Shortcuts](https://unitn-sml.github.io/rsbench/) - Paper and project page for rsbench. Tags: `🧠 concepts` `⚠️ shortcuts` `📏 metrics`.
- [Benchmarks in the Neurosymbolic Ecosystem](https://doi.org/10.4230/DagRep.15.7.53) - Dagstuhl report contribution on benchmark structure, metrics, and gaps in the neuro-symbolic ecosystem. Tags: `📏 metrics` `🔵 paper`.
- [Neural-Symbolic Learning and Reasoning: A Survey and Interpretation](https://arxiv.org/abs/1711.03902) - Broad survey of neural-symbolic foundations, systems, and applications. Tags: `🔵 paper`.
- [Neuro-Symbolic Artificial Intelligence: Current Trends](https://arxiv.org/abs/2105.05330) - Survey of integration patterns and current neuro-symbolic research directions. Tags: `🔵 paper`.
- [Neuro-Symbolic AI: The State of the Art](https://ebooks.iospress.nl/volume/neuro-symbolic-artificial-intelligence-the-state-of-the-art) - Edited volume covering neuro-symbolic methods and applications. Tags: `🔵 paper`.
- [Neuro-Symbolic Visual Reasoning](https://arxiv.org/abs/2006.11524) - Work on disentangling visual perception from reasoning in VQA. Tags: `🖼️ vision` `📏 metrics` `🔵 paper`.

<a id="gaps"></a>

## ⚠️ Gaps

- Audio-symbolic and temporal-logic benchmarks are sparse.
- Scientific-domain benchmarks are uneven across biology, law, ecology, medicine, materials science, and social science.
- Many benchmarks evaluate final task performance but not neural/symbolic component sensitivity.
- Few benchmarks test symbol construction, revision, provenance, explanation faithfulness, or trustworthy alignment between neural outputs and symbolic structures.
- More benchmarks should include generators, versioned splits, concept annotations, counterfactual/OOD splits, formal constraints, and clear licenses.

<a id="contributing"></a>

## 🤝 Contributing

Contributions are welcome through issues and pull requests. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before suggesting a new benchmark or resource.

New entries should include a stable public URL, task, symbolic component, primary metrics, data/code/paper status, and compact tags from the README vocabulary. Please keep the list curated rather than exhaustive, add each resource to one primary section, and open an issue first when access, license, symbolic component, or benchmark status is unclear.

Please also follow the [Code of Conduct](CODE_OF_CONDUCT.md).

<a id="license"></a>

## ⚖️ License

This curated list is released under [CC BY 4.0](LICENSE) unless otherwise stated. Each linked resource remains governed by its own license, access conditions, and terms of use.

<a id="acknowledgements"></a>

## ✨ Acknowledgements

Assisted by OpenAI Codex.

This list was seeded by benchmark discussions and the following Dagstuhl report contribution:

- Claudia d’Amato, Jennifer D’Souza, Anna Lisa Gentile, and Hande McGinty, “Benchmarks in the Neurosymbolic Ecosystem,” in “(Actual) Neurosymbolic AI: Combining Deep Learning and Knowledge Graphs (Dagstuhl Seminar 25291),” by Pascal Hitzler, Cogan Shimizu, Daria Stepanova, and Frank van Harmelen, *Dagstuhl Reports* 15, no. 7 (2026): 107–16, [https://doi.org/10.4230/DagRep.15.7.53](https://doi.org/10.4230/DagRep.15.7.53).

Resource selection, review, and maintenance remain community-curated.
