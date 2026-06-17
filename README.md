# Awesome Neuro-Symbolic Benchmarks

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![License: CC BY 4.0](https://img.shields.io/badge/license-CC%20BY%204.0-green.svg)](https://creativecommons.org/licenses/by/4.0/) [![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](#contributing) [![Curated List](https://img.shields.io/badge/curated-awesome%20list-blue.svg)](#how-to-use-this-list)

Benchmarks, datasets, suites, tasks, and evaluation resources for neuro-symbolic AI, learning-and-reasoning systems, symbolic faithfulness, and multi-modal reasoning.

Neuro-symbolic AI benchmarks often combine perceptual inputs with explicit symbolic structures such as logic rules, ontologies, knowledge graphs, scene graphs, functional programs, proofs, constraints, or plans. This list emphasizes resources that help evaluate not only final task performance, but also concept quality, reasoning shortcuts, compositional generalization, symbolic consistency, explainability, robustness, and small-data behavior. Neuro-symbolic AI is abbreviated as NeSy where space is tight.

## Contents

- [Legend](#legend)
- [How to Use This List](#how-to-use-this-list)
- [Core Benchmark Suites](#core-benchmark-suites)
- [Concept Quality and Reasoning Shortcuts](#concept-quality-and-reasoning-shortcuts)
- [Ontology, Knowledge Graph, and Semantic Web Benchmarks](#ontology-knowledge-graph-and-semantic-web-benchmarks)
- [Visual Reasoning and Scene Understanding](#visual-reasoning-and-scene-understanding)
- [Video, Temporal, and Physical Reasoning](#video-temporal-and-physical-reasoning)
- [Vision-Language and Knowledge-Based VQA](#vision-language-and-knowledge-based-vqa)
- [Language, Semantic Parsing, and Compositional Generalization](#language-semantic-parsing-and-compositional-generalization)
- [Logical Reasoning, Entailment, and Theorem Proving](#logical-reasoning-entailment-and-theorem-proving)
- [Program Synthesis and Executable Reasoning](#program-synthesis-and-executable-reasoning)
- [Robotics, Embodied Reasoning, and Planning](#robotics-embodied-reasoning-and-planning)
- [Autonomous Driving and Safety-Constrained Reasoning](#autonomous-driving-and-safety-constrained-reasoning)
- [Scientific and Domain-Specific Neuro-Symbolic Benchmarks](#scientific-and-domain-specific-neuro-symbolic-benchmarks)
- [Evaluation Metrics and Benchmarking Methodology](#evaluation-metrics-and-benchmarking-methodology)
- [Surveys, Position Papers, and Reading Lists](#surveys-position-papers-and-reading-lists)
- [Gaps and Wanted Contributions](#gaps-and-wanted-contributions)

## Legend

### Modality Tags

- 🖼️ Vision.
- 📝 Language.
- 🎥 Video.
- 🔊 Audio.
- 🕸️ Knowledge Graph / Ontology.
- 🤖 Robotics / Embodied AI.
- 🚗 Autonomous Driving.
- 🧪 Scientific / Domain.
- 🧩 Abstract / Synthetic Reasoning.
- 🔀 Multimodal.

### Capability Tags

- 🧠 Concept Quality.
- ⚠️ Reasoning Shortcuts.
- 🔁 OOD / Compositional Generalization.
- 🧰 Data Generator.
- ✅ Formal Verification / Constraints.
- 🔍 Explainability / Proofs.
- 📏 Metrics / Evaluation.
- 📚 Survey / Meta-resource.
- 🟢 Data + Code.
- 🟡 Data Only / Partial Code.
- 🔵 Paper / Description.

## How to Use This List

Use the task-family sections to find benchmark candidates and the tags to scan by modality or evaluation property. A strong neuro-symbolic benchmark should make clear what dataset is provided, what task is evaluated, what symbolic component is available or induced, which metrics are used, and whether it can test properties such as OOD generalization, compositionality, small-data learning, symbolic faithfulness, robustness, verifiability, explainability, scalability, and actionability.

## Core Benchmark Suites

- [rsbench](https://unitn-sml.github.io/rsbench/) - Benchmark suite for concept quality and reasoning shortcuts in neural, neuro-symbolic, concept-bottleneck, and foundation models; code is available on [GitHub](https://github.com/unitn-sml/rsbench). Tags: 🧠 ⚠️ 🔁 🧰 ✅ 🟢. Symbolic: Prior knowledge in CNF, task rules, concepts, and constraints. Metrics: Label F1, concept F1, concept confusion, concept collapse, OOD drop, shortcut count.
- [OAEI](https://oaei.ontologymatching.org/) - Ontology Alignment Evaluation Initiative with tracks for ontology matching across anatomy, conference, food, biodiversity, ecology, knowledge graphs, pharmacogenomics, and other domains. Tags: 🕸️ 📏 🟢. Symbolic: Ontologies and mappings. Metrics: Precision, recall, F1, semantic precision/recall, runtime, consistency, conservativity.
- [LLMs4OL](https://sites.google.com/view/llms4ol2025) - Shared task and benchmark series for ontology learning with large language models, including term typing, taxonomy discovery, and relation extraction tasks. Tags: 🕸️ 📝 📏. Symbolic: Ontology classes, taxonomies, and relations. Metrics: Precision, recall, F1.
- [CLEVR](https://cs.stanford.edu/people/jcjohns/clevr/) - Diagnostic visual reasoning dataset with rendered scenes, scene graphs, and functional programs for compositional question answering. Tags: 🖼️ 🔀 🧩 🟡. Symbolic: Scene graphs and functional programs. Metrics: Answer accuracy.
- [GQA](https://cs.stanford.edu/people/dorarad/gqa/about.html) - Scene-graph-based visual question answering benchmark for real-world images and compositional reasoning. Tags: 🖼️ 📝 🧩 🟡. Symbolic: Scene graphs and functional programs. Metrics: Accuracy, consistency, validity, plausibility, grounding.
- [CFQ](https://research.google/blog/measuring-compositional-generalization/) - Compositional Freebase Questions benchmark for semantic parsing and compositional generalization over Freebase-style queries. Tags: 📝 🕸️ 🔁 🟡. Symbolic: SPARQL queries and Knowledge Graph schema. Metrics: Exact match, query accuracy, compound divergence split performance.
- [BabyAI](https://github.com/mila-iqia/babyai/tree/iclr19) - Instruction-following gridworld benchmark with symbolic language goals and a verifier for sample-efficient grounded language learning. Tags: 🤖 📝 ✅ 🟢. Symbolic: Grid objects, instructions, plans, and verifier. Metrics: Success rate, sample efficiency.
- [ALFRED](https://askforalfred.com/) - Embodied household instruction-following benchmark with visual observations, language instructions, and high-level action plans. Tags: 🤖 🖼️ 📝 🟡. Symbolic: Task plans, object states, and action sequences. Metrics: Success rate, goal-condition success.
- [EntailmentBank](https://allenai.org/data/entailmentbank) - Natural-language question answering benchmark with structured entailment-tree explanations. Tags: 📝 🔍 ✅ 🟡. Symbolic: Entailment trees and proof-like reasoning chains. Metrics: Answer accuracy, tree correctness, proof quality.
- [ProofWriter](https://allenai.org/data/proofwriter) - Synthetic rule-based natural-language reasoning dataset with generated implications and proofs. Tags: 📝 🔍 ✅ 🟡. Symbolic: Facts, rules, implications, proofs. Metrics: Answer accuracy, proof accuracy, generalization by proof depth.
- [TPTP](https://www.tptp.org/) - Thousands of Problems for Theorem Provers, a long-running formal problem library and infrastructure for automated theorem proving. Tags: ✅ 🧩 📏 🟢. Symbolic: Formal logic problems and proofs. Metrics: Problems solved, proof status, proof quality, runtime.
- [HolStep](https://arxiv.org/abs/1703.00426) - Higher-order logic theorem-proving dataset derived from HOL Light proofs for premise selection and proof-step prediction. Tags: ✅ 🧩 🔵. Symbolic: HOL formulas, theorems, and proof steps. Metrics: Premise selection precision/recall, proof-step prediction accuracy.

## Concept Quality and Reasoning Shortcuts

Reasoning shortcuts occur when a model solves the downstream reasoning task without learning the intended concept semantics. This is especially important for neuro-symbolic systems because high task accuracy can hide poor concept grounding, concept collapse, or unsafe reliance on spurious concept substitutions.

- [rsbench](https://unitn-sml.github.io/rsbench/) - Anchor suite for studying reasoning shortcuts, concept quality, and OOD effects across arithmetic, logic, visual, and autonomous-driving learning-and-reasoning tasks. Tags: 🧠 ⚠️ 🔁 🧰 ✅ 🟢. Symbolic: Concepts, prior knowledge, CNF constraints, and task generators. Metrics: Label F1 / accuracy, concept F1, concept confusion matrices, concept collapse, OOD performance drop, shortcut counting with `countrss`.

| Task | Description |
| --- | --- |
| MNMath | Arithmetic learning-and-reasoning task based on systems of MNIST equations. Tags: 🧩 🧠 ⚠️ 🧰. Symbolic: Linear equations over digit concepts. Metrics: Label F1, concept F1, shortcut risk, OOD drop. |
| MNAdd-Half | MNIST addition variant with guaranteed reasoning shortcuts. Tags: 🧩 🧠 ⚠️. Symbolic: Sum constraints over two digit concepts. Metrics: Label F1, concept F1, concept collapse. |
| MNAdd-EvenOdd | MNIST addition variant supporting OOD and continual-learning settings. Tags: 🧩 🧠 ⚠️ 🔁. Symbolic: Addition rules over even/odd digit splits. Metrics: Label F1, concept F1, OOD F1, concept confusion. |
| MNLogic | Logical formula satisfaction over MNIST-style bits. Tags: 🧩 ✅ ⚠️ 🧰. Symbolic: Boolean formulas and CNF knowledge. Metrics: Label F1, concept F1, shortcut count. |
| Kand-Logic | Kandinsky-pattern-inspired visual reasoning with shape/color concepts and shortcut risk. Tags: 🖼️ 🧠 ⚠️ 🧰. Symbolic: Logical predicates over shapes and colors. Metrics: Label F1, concept F1, concept collapse. |
| CLE4EVR | CLEVR-inspired 3D scene reasoning benchmark designed to expose concept collapse and shortcuts. Tags: 🖼️ 🧠 ⚠️ 🔁. Symbolic: Scene concepts and logical constraints. Metrics: Label F1, concept F1, OOD performance. |
| BDD-OIA | Real autonomous-driving action decision dataset with concept annotations and traffic-law constraints. Tags: 🚗 🖼️ ✅ ⚠️. Symbolic: Traffic concepts and action constraints. Metrics: Action F1, concept F1, constraint consistency. |
| SDD-OIA | Synthetic 3D traffic-scene benchmark with configurable OOD scenarios and traffic rules. Tags: 🚗 🖼️ ⚠️ 🔁 🧰. Symbolic: Traffic concepts, rules, and configurable OOD generation. Metrics: mF1, concept mF1, OOD mF1, concept collapse. |

- [KANDY](https://arxiv.org/abs/2402.17431) - Incremental neuro-symbolic learning benchmark using Kandinsky-pattern curricula and rule-based ground truth. Tags: 🖼️ 🧩 🧠 🔁 🔵. Symbolic: Shape/color rules and curricula. Metrics: Classification accuracy, continual-learning performance, generalization.
- [Reasoning Shortcut Analysis](https://arxiv.org/abs/2305.19951) - Study of reasoning shortcuts in concept-based and neuro-symbolic models that motivates concept-level evaluation beyond final labels. Tags: 🧠 ⚠️ 📏 🔵. Symbolic: Concept mappings and shortcut analyses. Metrics: Concept quality, downstream accuracy, OOD behavior.

## Ontology, Knowledge Graph, and Semantic Web Benchmarks

- [FB15k-237](https://www.microsoft.com/en-us/download/details.aspx?id=52312) - Knowledge base completion benchmark derived from Freebase triples with inverse-relation leakage reduced relative to FB15k. Tags: 🕸️ 📏 🟡. Symbolic: Knowledge Graph triples and relations. Metrics: MRR, Hits@1/3/10.
- [LLMs4OL](https://sites.google.com/view/llms4ol2025) - Ontology learning benchmark for extracting and structuring ontology terms, types, taxonomies, and relations from text. Tags: 🕸️ 📝 📏. Symbolic: Ontology schemas and relation labels. Metrics: Precision, recall, F1.
- [OAEI](https://oaei.ontologymatching.org/) - Community evaluation campaign for ontology and Knowledge Graph alignment, including biomedical, domain, and cross-lingual tracks. Tags: 🕸️ 📏 🟢. Symbolic: Ontologies, alignments, semantic constraints. Metrics: Precision, recall, F1, semantic precision/recall, runtime, consistency, conservativity.
- [WN18RR](https://github.com/TimDettmers/ConvE) - WordNet-derived Knowledge Graph completion benchmark that removes many inverse relation artifacts from WN18. Tags: 🕸️ 📏 🟡. Symbolic: Synsets and lexical relations. Metrics: MRR, Hits@1/3/10.
- [YAGO3](https://yago-knowledge.org/downloads/yago-3) - Large ontology-derived Knowledge Graph combining Wikipedia, WordNet, GeoNames, and multilingual facts; YAGO3-10 is commonly used for link prediction. Tags: 🕸️ 📏 🟡. Symbolic: Type hierarchies, relations, temporal/spatial facts. Metrics: MRR, Hits@1/3/10.

## Visual Reasoning and Scene Understanding

- [ARC-AGI](https://github.com/fchollet/ARC-AGI) - Abstraction and Reasoning Corpus for grid-based visual program induction and few-shot abstract reasoning. Tags: 🖼️ 🧩 🔁 🟢. Symbolic: Latent transformation programs and object relations. Metrics: Task success, exact output match.
- [Bongard-LOGO](https://github.com/NVlabs/Bongard-LOGO) - Synthetic Bongard problem generator for visual concept learning and analogical reasoning. Tags: 🖼️ 🧩 🧰 🟢. Symbolic: Shape relations and concept rules. Metrics: Classification accuracy, concept generalization.
- [CLEVR](https://cs.stanford.edu/people/jcjohns/clevr/) - Synthetic diagnostic benchmark for compositional visual reasoning with scene graphs and executable functional programs. Tags: 🖼️ 🔀 🧩 🟡. Symbolic: Scene graphs and functional programs. Metrics: Answer accuracy.
- [CLEVR-CoGenT](https://cs.stanford.edu/people/jcjohns/clevr/) - CLEVR split for compositional generalization across color-shape combinations. Tags: 🖼️ 🔁 🧩 🟡. Symbolic: Scene graphs and controlled concept splits. Metrics: Accuracy, generalization gap.
- [GQA](https://cs.stanford.edu/people/dorarad/gqa/about.html) - Real-image visual reasoning benchmark with scene graphs, compositional questions, and balanced evaluation. Tags: 🖼️ 📝 🧩 🟡. Symbolic: Scene graphs and functional programs. Metrics: Accuracy, consistency, validity, plausibility.
- [KANDY](https://arxiv.org/abs/2402.17431) - Kandinsky-pattern benchmark for incremental learning, symbolic compositionality, and sparse supervision. Tags: 🖼️ 🧩 🧠 🔁 🔵. Symbolic: Pattern rules and visual concepts. Metrics: Accuracy, curriculum transfer, generalization.
- [NLVR / NLVR2](https://lil.nlp.cornell.edu/nlvr/) - Natural-language visual reasoning datasets requiring reasoning about image pairs or synthetic visual worlds. Tags: 🖼️ 📝 🔁 🟡. Symbolic: Structured visual configurations and language constraints. Metrics: Accuracy, consistency.
- [PGM](https://github.com/google-deepmind/abstract-reasoning-matrices) - Procedurally generated matrix reasoning benchmark for abstract visual reasoning. Tags: 🖼️ 🧩 🔁 🟢. Symbolic: Latent relational rules. Metrics: Answer accuracy, regime-specific generalization.
- [RAVEN](https://wellyzhang.github.io/project/raven.html) - Relational and analogical visual reasoning dataset based on Raven-style progressive matrices. Tags: 🖼️ 🧩 🔁 🟡. Symbolic: Structured figure configurations and relational rules. Metrics: Answer accuracy.
- [Visual Genome](https://arxiv.org/abs/1602.07332) - Dense image annotation resource with objects, attributes, relationships, region descriptions, and question-answer pairs. Tags: 🖼️ 📝 🕸️ 🟡. Symbolic: Scene graphs and WordNet-linked annotations. Metrics: Detection, relation, grounding, and VQA metrics depending on task.

## Video, Temporal, and Physical Reasoning

- [CLEVRER](https://arxiv.org/abs/1910.01442) - Diagnostic video reasoning benchmark for physical events, collisions, causal relations, prediction, and counterfactuals. Tags: 🎥 🧩 🔁 🔵. Symbolic: Object states, events, causal structure, and question programs. Metrics: Answer accuracy by descriptive, explanatory, predictive, and counterfactual question type.
- [IntPhys](https://arxiv.org/abs/1803.07616) - Physical scene understanding benchmark designed around intuitive physics and expectation violation. Tags: 🎥 🖼️ 🧩 🔵. Symbolic: Physical object permanence and plausibility constraints. Metrics: Accuracy, preference for possible over impossible events.
- [PHYRE](https://arxiv.org/abs/1908.05656) - Benchmark for physical reasoning in 2D environments with action-based problem solving. Tags: 🎥 🧩 🔁 🟢. Symbolic: Objects, physical rules, goals, and actions. Metrics: Success rate, sample efficiency, generalization.
- [Physion](https://physion-benchmark.github.io/) - Physical prediction benchmark using simulated videos of object interactions. Tags: 🎥 🧩 📏 🟡. Symbolic: Object properties, physical interactions, and prediction targets. Metrics: Prediction accuracy, consistency with physical outcomes.
- [SUTD-TrafficQA](https://github.com/SUTDCV/SUTD-TrafficQA) - Video question answering benchmark for traffic-event reasoning. Tags: 🎥 🚗 📝 🟡. Symbolic: Traffic events and temporal relations. Metrics: Answer accuracy.

Video benchmarks with explicit symbolic constraints, concept-level annotations, temporal logic, and counterfactual splits remain comparatively underdeveloped.

## Vision-Language and Knowledge-Based VQA

- [A-OKVQA](https://arxiv.org/abs/2206.01718) - Augmented outside-knowledge VQA benchmark with rationales for knowledge-intensive visual question answering. Tags: 🖼️ 📝 🔀 🔍 🟡. Symbolic: External knowledge and rationales. Metrics: Answer accuracy, rationale quality.
- [FVQA](https://github.com/GT-Vision-Lab/VQA_Lol_FVQA) - Fact-based visual question answering benchmark that links visual recognition with supporting knowledge facts. Tags: 🖼️ 📝 🕸️ 🔍 🟡. Symbolic: Relation triples and supporting facts. Metrics: Answer accuracy, fact retrieval quality.
- [GQA](https://cs.stanford.edu/people/dorarad/gqa/about.html) - Scene-graph VQA benchmark for compositional language-grounded visual reasoning. Tags: 🖼️ 📝 🧩 🟡. Symbolic: Scene graphs and programs. Metrics: Accuracy, consistency, validity.
- [KVQA](https://malllabiisc.github.io/resources/kvqa/) - Knowledge-aware VQA benchmark over named entities and Knowledge Graph reasoning. Tags: 🖼️ 📝 🕸️ 🔀 🟡. Symbolic: Entity links and KG facts. Metrics: Answer accuracy, entity-reasoning performance.
- [OK-VQA](https://okvqa.allenai.org/) - Outside-knowledge VQA benchmark where image content is insufficient without commonsense or factual knowledge. Tags: 🖼️ 📝 🔀 🟡. Symbolic: Retrieved external knowledge and facts. Metrics: Answer accuracy.
- [Retrieval-Augmented Visual Question Answering](https://github.com/LinWeizheDragon/Retrieval-Augmented-Visual-Question-Answering) - Resource for outside-knowledge VQA with retrieval-augmented reasoning. Tags: 🖼️ 📝 🕸️ 🔀 🟢. Symbolic: Retrieved knowledge passages and facts. Metrics: Answer accuracy, retrieval quality.
- [Visual Dialog](https://visualdialog.org/) - Visual conversational QA benchmark that can be adapted for neuro-symbolic dialogue reasoning, especially coreference and state tracking. Tags: 🖼️ 📝 🔀 🟡. Symbolic: Dialogue state, visual references, and possible external knowledge. Metrics: Retrieval metrics, answer ranking, generative quality.
- [VQA v2.0](https://visualqa.org/) - Visual question answering benchmark with balanced image-question pairs to reduce language priors. Tags: 🖼️ 📝 🔀 🟡. Symbolic: Implicit object, attribute, and relation reasoning. Metrics: VQA accuracy.

## Language, Semantic Parsing, and Compositional Generalization

- [bAbI](https://research.facebook.com/downloads/babi/) - Synthetic text reasoning task suite for memory, induction, deduction, path finding, and multi-hop QA. Tags: 📝 🧩 🔁 🟡. Symbolic: Facts, rules, supporting statements, and latent reasoning chains. Metrics: Answer accuracy.
- [CFQ](https://research.google/blog/measuring-compositional-generalization/) - Semantic parsing benchmark for compositional generalization from natural language to SPARQL over Freebase. Tags: 📝 🕸️ 🔁 🟡. Symbolic: SPARQL logical forms and KG schema. Metrics: Exact match, query accuracy, split generalization gap.
- [CLUTRR](https://github.com/facebookresearch/clutrr) - Text benchmark for systematic generalization in family-relation reasoning. Tags: 📝 🧩 🔁 🟢. Symbolic: Kinship relation rules and story graphs. Metrics: Relation classification accuracy, OOD generalization.
- [COGS](https://github.com/najoungkim/COGS) - Compositional generalization benchmark mapping English sentences to logical forms. Tags: 📝 🧩 🔁 🟢. Symbolic: Logical forms and structural generalization splits. Metrics: Exact match, generalization accuracy.
- [GeoQuery](https://github.com/jkkummerfeld/text2sql-data) - Classic semantic parsing benchmark for geography questions and executable logical queries. Tags: 📝 🧩 🟡. Symbolic: Logical forms and database queries. Metrics: Exact match, execution accuracy.
- [HotpotQA](https://hotpotqa.github.io/) - Multi-hop question answering benchmark useful for studying explainable retrieval and reasoning, though not inherently neuro-symbolic. Tags: 📝 🔍 🔀 🟡. Symbolic: Supporting facts and evidence chains. Metrics: Answer F1, supporting-fact F1, exact match.
- [SCAN](https://github.com/brendenlake/SCAN) - Simple navigation command benchmark for compositional generalization from language to action sequences. Tags: 📝 🧩 🔁 🟢. Symbolic: Command grammar and action programs. Metrics: Exact match over action sequences.

## Logical Reasoning, Entailment, and Theorem Proving

- [EntailmentBank](https://allenai.org/data/entailmentbank) - Dataset for explaining QA answers with multi-step entailment trees. Tags: 📝 🔍 ✅ 🟡. Symbolic: Entailment trees and intermediate conclusions. Metrics: Final answer accuracy, tree correctness, proof quality.
- [HolStep](https://arxiv.org/abs/1703.00426) - Higher-order logic benchmark for learning premise selection and proof-step prediction from formal proofs. Tags: ✅ 🧩 🔵. Symbolic: HOL formulas and proof steps. Metrics: Premise selection precision/recall, proof-step accuracy.
- [HOList](https://arxiv.org/abs/1904.03241) - Higher-order theorem-proving environment and benchmark derived from HOL Light. Tags: ✅ 🧩 🟢. Symbolic: HOL Light goals, premises, tactics, and proof states. Metrics: Proof success rate, theorem coverage.
- [LeanDojo](https://github.com/lean-dojo/LeanDojo) - Toolkit and benchmark environment for interacting with Lean programmatically and extracting theorem-proving data. Tags: ✅ 🧩 🟢. Symbolic: Lean proofs, premises, tactics, and states. Metrics: Proof success, premise selection, tactic prediction.
- [miniF2F](https://github.com/openai/miniF2F) - Formal mathematics benchmark for theorem proving across Lean, Isabelle, Metamath, and other systems. Tags: ✅ 🧩 🟢. Symbolic: Formal theorem statements and proofs. Metrics: Proof success rate.
- [ProofWriter](https://allenai.org/data/proofwriter) - Natural-language rule reasoning dataset with generated implications, proofs, and abductive statements. Tags: 📝 🔍 ✅ 🟡. Symbolic: Facts, rules, proof chains. Metrics: Answer accuracy, proof accuracy, depth generalization.
- [TPTP](https://www.tptp.org/) - Formal problem library and infrastructure for automated theorem proving systems. Tags: ✅ 🧩 📏 🟢. Symbolic: First-order and higher-order logic problems. Metrics: Problems solved, proof status, runtime.

## Program Synthesis and Executable Reasoning

- [ARC-AGI](https://github.com/fchollet/ARC-AGI) - Grid transformation benchmark often treated as program-like abstraction and synthesis from examples. Tags: 🖼️ 🧩 🔁 🟢. Symbolic: Latent transformation programs. Metrics: Exact output match, task success.
- [CFQ](https://research.google/blog/measuring-compositional-generalization/) - Natural-language-to-SPARQL benchmark where executable logical forms are central. Tags: 📝 🕸️ 🔁 🟡. Symbolic: SPARQL programs. Metrics: Exact match, execution accuracy.
- [DeepCoder](https://www.microsoft.com/en-us/research/publication/deepcoder-learning-write-programs/) - Program synthesis benchmark and approach for learning to write small programs from input-output examples. Tags: 🧩 🔵. Symbolic: DSL programs and input-output specifications. Metrics: Program recovery, execution accuracy.
- [DreamCoder](https://github.com/ellisk42/ec) - Program-learning system and benchmark collection for synthesizing programs while learning reusable symbolic abstractions. Tags: 🧩 🔁 🟢. Symbolic: DSL programs and learned libraries. Metrics: Task solved, search efficiency, generalization.
- [Karel](https://github.com/carpedm20/karel) - Program synthesis dataset for inferring Karel programs from input-output grid examples. Tags: 🧩 🟢. Symbolic: Karel DSL programs and grid states. Metrics: Execution accuracy, exact program match.
- [SCAN](https://github.com/brendenlake/SCAN) - Command-to-action benchmark interpretable as program generation from compositional language. Tags: 📝 🧩 🔁 🟢. Symbolic: Grammar and action programs. Metrics: Exact sequence match.
- [Spider](https://yale-lily.github.io/spider) - Cross-domain text-to-SQL benchmark for executable database reasoning. Tags: 📝 🧩 🟡. Symbolic: SQL queries and database schemas. Metrics: Exact match, execution accuracy, test-suite accuracy.
- [WikiSQL](https://github.com/salesforce/WikiSQL) - Large semantic parsing corpus for natural-language interfaces to relational tables. Tags: 📝 🧩 🟢. Symbolic: SQL queries and table schemas. Metrics: Logical-form accuracy, execution accuracy.

## Robotics, Embodied Reasoning, and Planning

- [AI2-THOR](https://ai2thor.allenai.org/) - Interactive 3D environment for embodied AI tasks with object states, physics, and household scenes. Tags: 🤖 🖼️ 🟢. Symbolic: Object states, scene metadata, actions, and goals. Metrics: Task success, navigation and manipulation metrics.
- [ALFRED](https://askforalfred.com/) - Embodied instruction-following benchmark for household tasks with visual observations and action plans. Tags: 🤖 🖼️ 📝 🟡. Symbolic: Task plans, subgoals, object states. Metrics: Success rate, goal-condition success.
- [ALFWorld](https://alfworld.github.io/) - Text and embodied environment aligning ALFRED-style household tasks with symbolic planning and language interaction. Tags: 🤖 📝 ✅ 🟢. Symbolic: PDDL-like tasks, object states, and plans. Metrics: Success rate, goal satisfaction.
- [BabyAI](https://github.com/mila-iqia/babyai/tree/iclr19) - Gridworld instruction-following benchmark with symbolic verifier and compositional language. Tags: 🤖 📝 ✅ 🟢. Symbolic: Objects, instructions, goal verifier. Metrics: Success rate, sample efficiency.
- [CausalWorld](https://github.com/rr-learning/CausalWorld) - Robotic manipulation benchmark for causal structure and transfer learning. Tags: 🤖 🧩 🔁 🟢. Symbolic: Object factors, interventions, and task structure. Metrics: Success rate, transfer performance, sample efficiency.
- [LogiCity](https://sairlab.org/datasets/logicity/) - Urban simulation benchmark using customizable first-order logic rules for dynamic multi-agent reasoning. Tags: 🤖 🚗 ✅ 🔁 🟢. Symbolic: FOL rules, semantic and spatial concepts, agent policies. Metrics: Safe path success, action prediction accuracy, compositional generalization.
- [MiniGrid](https://github.com/Farama-Foundation/Minigrid) - Configurable gridworld environment for instruction following, symbolic goals, and planning research. Tags: 🤖 📝 🧩 🟢. Symbolic: Grid objects, missions, and goal conditions. Metrics: Success rate, sample efficiency.
- [Neuro-Symbolic Action Planning](https://michaal94.github.io/project/ns-ap) - Benchmark for visual and manipulation reasoning with symbolic subgoals and action planning. Tags: 🤖 🖼️ ✅ 🔵. Symbolic: Subgoal programs and planning structure. Metrics: Scenario success rate, subgoal execution.

## Autonomous Driving and Safety-Constrained Reasoning

- [BDD-OIA](https://unitn-sml.github.io/rsbench/) - Real driving-image action decision dataset in rsbench with concept annotations and traffic-rule constraints. Tags: 🚗 🖼️ ✅ ⚠️ 🟡. Symbolic: Traffic concepts and action constraints. Metrics: Action F1, concept F1, constraint consistency.
- [LogiCity](https://sairlab.org/datasets/logicity/) - Dynamic urban reasoning benchmark with first-order traffic and interaction rules. Tags: 🚗 🤖 ✅ 🔁 🟢. Symbolic: FOL rules over agents, priorities, spatial relations, and behaviors. Metrics: Safe navigation success, action prediction accuracy.
- [ROAD-R](https://arxiv.org/abs/2210.01597) - Road-event reasoning benchmark for autonomous driving with logical requirements over road events. Tags: 🚗 🎥 ✅ 🟡. Symbolic: Road agents, events, relations, and logical constraints. Metrics: Detection, relation, event-reasoning, and constraint-violation metrics.
- [SDD-OIA](https://unitn-sml.github.io/rsbench/) - Synthetic 3D driving benchmark in rsbench with configurable OOD traffic scenes and rules. Tags: 🚗 🖼️ ⚠️ 🔁 🧰 🟢. Symbolic: Traffic concepts, rules, and emergency-condition variants. Metrics: mF1, concept mF1, OOD mF1, shortcut risk.
- [SUTD-TrafficQA](https://github.com/SUTDCV/SUTD-TrafficQA) - Traffic video question answering benchmark for reasoning over events and road situations. Tags: 🚗 🎥 📝 🟡. Symbolic: Traffic events, temporal relations, and scene entities. Metrics: Answer accuracy.

## Scientific and Domain-Specific Neuro-Symbolic Benchmarks

Domain coverage is uneven. Biology, law, ecology, medicine, materials science, and social science need more benchmarks that combine learned perception or language understanding with explicit rules, taxonomies, ontologies, provenance, constraints, or causal structure.

- [LLMs4OL](https://sites.google.com/view/llms4ol2025) - Ontology learning benchmark with domain tracks spanning biomedicine, materials science, earth and environmental science, medicine, food, plants, chemistry, and the web. Tags: 🧪 🕸️ 📝 📏. Symbolic: Domain ontologies, taxonomies, and relations. Metrics: Precision, recall, F1.
- [OAEI Bio-ML and Domain Tracks](https://oaei.ontologymatching.org/) - Ontology alignment tracks covering biomedical, biodiversity, ecology, food, pharmacogenomics, archaeology, circular-economy, and Knowledge Graph settings. Tags: 🧪 🕸️ 📏 🟢. Symbolic: Domain ontologies and alignments. Metrics: Precision, recall, F1, semantic precision/recall, consistency.

### Wanted

- Biology and biomedical KG reasoning with concept faithfulness.
- Legal reasoning with explicit statutes, exceptions, and jurisdictional rules.
- Ecological evidence synthesis with causal, spatial, and taxonomic knowledge.
- Materials-science process reasoning with templates, ontologies, and experiment provenance.
- Oral-history and cultural heritage reasoning with provenance, access constraints, and community governance.

## Evaluation Metrics and Benchmarking Methodology

### Common Metrics

- Accuracy.
- Precision / Recall / F1.
- Macro-F1 / micro-F1.
- MRR.
- Hits@N.
- Exact match.
- Execution accuracy.
- Success rate.
- Goal-conditioned success.
- BLEU / ROUGE where language generation is relevant.

### Neuro-Symbolic-Specific Metrics

- Symbolic consistency.
- Constraint satisfaction.
- Logical validity.
- Proof quality.
- Explanation faithfulness.
- Concept F1.
- Concept collapse.
- Concept confusion matrices.
- OOD drop.
- Shortcut count / shortcut risk.
- Calibration and uncertainty.
- Robustness to data drift.
- Small-data learning curves.
- Ablation of neural and symbolic components.
- Energy, memory, runtime, and scalability.

### Benchmark Design Checklists

- Does the benchmark clearly specify dataset, task, and metric?
- What symbolic component is present?
- Does it evaluate only final performance or also perception, abstraction, reasoning, and strategy?
- Does it include OOD, compositional, or counterfactual splits?
- Does it include concept labels or only final labels?
- Does it support small-data evaluation?
- Does it permit component-level ablation?
- Can it detect reasoning shortcuts or concept collapse?
- Are license, version, provenance, and maintenance status clear?
- Is there a stable URL and documentation?

## Surveys, Position Papers, and Reading Lists

- [A Neuro-Symbolic Benchmark Suite for Concept Quality and Reasoning Shortcuts](https://unitn-sml.github.io/rsbench/) - rsbench paper and website introducing benchmark tasks, concept-quality metrics, and formal counting of reasoning shortcuts. Tags: 📚 🧠 ⚠️ 📏.
- [Benchmarks in the Neurosymbolic Ecosystem](#footnotes) - Internal Dagstuhl 2025 seed note used to frame benchmark quality as dataset, task, metric, symbolic component, and evaluation property. Tags: 📚 📏 🔵.
- [Neural-Symbolic Learning and Reasoning: A Survey and Interpretation](https://arxiv.org/abs/1711.03902) - Broad survey of neural-symbolic learning and reasoning foundations, systems, and applications. Tags: 📚 🔵.
- [Neuro-Symbolic Artificial Intelligence: Current Trends](https://arxiv.org/abs/2105.05330) - Survey of trends in neuro-symbolic AI integration and systems. Tags: 📚 🔵.
- [Neuro-Symbolic Visual Reasoning](https://arxiv.org/abs/2006.11524) - Position-style benchmark paper disentangling visual perception from reasoning in VQA. Tags: 📚 🖼️ 📏 🔵.
- [Neuro-Symbolic AI: The State of the Art](https://ebooks.iospress.nl/volume/neuro-symbolic-artificial-intelligence-the-state-of-the-art) - Edited volume on neuro-symbolic AI methods, applications, and foundations. Tags: 📚 🔵.
- [The KANDY Benchmark](https://arxiv.org/abs/2402.17431) - Benchmark paper focused on incremental neuro-symbolic learning and reasoning with Kandinsky patterns. Tags: 📚 🖼️ 🧠 🔵.

## Gaps and Wanted Contributions

- Audio-symbolic benchmarks are sparse.
- Time-series benchmarks with temporal logic constraints are sparse.
- Scientific-domain benchmarks are uneven.
- Benchmarks often evaluate final performance but not neural/symbolic component sensitivity.
- Many benchmarks rely on static symbolic formalisms and do not test symbol construction, revision, or explanation.
- Few benchmarks evaluate symbolic faithfulness, trustworthiness, or alignment between neural outputs and symbolic structures.
- Few benchmarks support systematic OOD, continual-learning, small-data, and counterfactual analyses.
- More benchmarks should include data generators, versioned splits, concept annotations, formal constraints, and clear licensing.

## Contributing

Contributions are welcome. Please suggest benchmarks that are documented, accessible, and useful for evaluating neuro-symbolic learning, reasoning, grounding, planning, or symbolic faithfulness. Each entry should include a stable link, a one-sentence description, modality tags, symbolic component, task, metrics, and license if known.

```md
- [Benchmark Name](https://example.org) - One-sentence description. Tags: 🖼️ 🧩 🔁. Symbolic: Scene graph / logic rules / ontology / proof / program. Metrics: Accuracy / F1 / MRR / execution accuracy. License: CC BY / MIT / unknown.
```

## Footnotes

This README was seeded from the attached Dagstuhl 2025 materials and public benchmark pages. The internal note "Benchmarks in the Neurosymbolic Ecosystem" is referenced for conceptual framing until a public citation URL is available.
