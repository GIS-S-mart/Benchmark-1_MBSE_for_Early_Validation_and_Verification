# Benchmark 1. MBSE for Early Validation and Verification

This benchmark aims at building confidence in the usefulness of the new methods and tools with respect to the validation of specifications and the verification of designs. Qualitative and quantitative standardised metrics help to compare studies and to measure the technical progress.

## Glossary

To share a common understanding of ambiguous concepts, contributors shall agree upon the following definitions:

- *Requirement*: the result of a formal transformation of one or more needs or parent requirements into an agreed-to obligation for an object to possess some property within specified constraints under some conditions with acceptable risk.
- *Specification*: a set of requirements.
- *Design*: definition of the architecture, system elements, interfaces, and other characteristics of a system.
- *Verification*: confirmation, through objective evidence, that specified requirements have been fulfilled.
- *Validation*: confirmation, through objective evidence, that the requirements for a specific intended use or application have been fulfilled. A system is able to accomplish its intended use, goals and objectives (i.e., meet stakeholder requirements) in the intended operational environment. The right system was built.

## Requirements

[Ra] Requirement elicitation:

- Ra1: The solution shall enable systems engineers to specify *correct requirements*.
- Ra2: The solution shall enable systems engineers to specify *complete requirements*.
- Ra3: The solution shall enable systems engineers to specify *correct specifications*.
- Ra4: The Solution shall enable systems engineers to specify *complete specifications*.

> Note: in this context, "specify" relates to additions or deletions made to the initial requirements, as part of the early verification and validation process.

[Rb] Requirement enrichment:

- Rb1: The solution shall enable systems engineers to identify inconsistent specifications.
- Rb2: The solution shall enable systems engineers to complete the requirements with the appropriate level of refinement.
- Rb3: The solution shall enable systems engineer to identify missing requirements.

[Rc] Requirement verification & validation:

- Rc1: The solution shall enable systems engineers to prove that the designs meets the specifications.
- Rc2: The solution shall enable systems engineers to prove that the implementations meets the specifications.
- Rc3: The solution shall enable stakeholders, especially end-users, to experience the systems properties (behavioural and structural) in its intended operational environment with a high degree of realism. <span style="color:red">tbd</span>

[Rd] Requirement traceability:

- Rd1: The solution shall enable systems engineers to vertically trace requirements. <span style="color:red">tbd</span>
- Rd2: The solution shall enable systems engineers to horizontally trace requirements. <span style="color:red">tbd</span>

## Measures of performance

values in [N/A, Yes, No]

- MoP1: (boolean) Number of verified specifications.
- Overall MoP: (float) ratio of verified MoP.

## Datasets

- [Robot arm] <span style="color:red">tbd</span>
...

- [WONKA case study](wonka_case_study.md)
**GOAL: verify and validate a scientific approach on multiple *industrial systems*, given *laboratory systems*. The solution should enable systems engineer to correct, complete and verify specifications as early as possible (before/after experiments on laboratory systems, before/after experiments on industrial systems).**
Five use cases are considered: 3 laboratory systems (1 coffee machine, 1 robot arm, 1 3D printer) and 2 industrial systems (1 mixing/conching machine from a chocolate factory and 1 temperature-controlled vehicle testbed). Additional instrumentation come with all systems.
<span style="color:red">TODO 1 descriptive diagram per use case</span>
This case study consists of (i) all five instrumented systems in their environments with their description (system, purpose and initial requirements), (ii) an ontology tailored to mechatronic systems, (iii) a formal description of all use cases using this ontology. 
[see more details](wonka_case_study.md)

## Benchmarking

- [WONKA]: ontology-based early verification and validation on heterogeneous systems [1].
- [Solution B]
- [Solution C]

Requirements tackled by these solutions (values in [N/A, -, =, +]):

| Solution |  Ra1  |  Ra2  |  Ra3  |  Ra4  |
| -------- | :---: | :---: | :---: | :---: |
| WONKA    |  N/A  |  N/A  |  N/A  |  N/A  |

| Solution |  Rb1  |  Rb2  |  Rb3  |
| -------- | :---: | :---: | :---: |
| WONKA    |   +   |   +   |   +   |

| Solution |  Rc1  |  Rc2  |  Rc3  |
| -------- | :---: | :---: | :---: |
| WONKA    |   +   |   +   |   -   |

| Solution |  Rd1  |  Rd2  |
| -------- | :---: | :---: |
| WONKA    |  N/A  |  N/A  |

Measure of performance:

| Solution | MoP1  | overall MoP |
| -------- | :---: | :---------: |
| WONKA    |  N/A  |     N/A     |


## Meta-Analysis <span style="color:red">tbd</span>

## References

[1] Delabeye, R., Penas, O., & Plateaux, R. (2022, October). Scalable ontology-based V&V process for heterogeneous systems and applications. In Proceedings of the 25th International Conference on Model Driven Engineering Languages and Systems: Companion Proceedings (pp. 341-350).