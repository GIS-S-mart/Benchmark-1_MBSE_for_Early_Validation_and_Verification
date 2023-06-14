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

<!-- - MoP1: (boolean) Number of verified specifications. -->
- MoP1: (integer) Number $`n_{new\_req}`$ of newly discovered requirements (or additions made to the initial requirements), either refining or further constraining the design. Higher is better.

- MoP2: (float) Final verification rate $`\mathcal{V} = \frac{| \mathcal{R}_{valid} |}{| \mathcal{R} |}`$, i.e., total number of verified requirement $`| \mathcal{R}_{valid} |`$ over the total number of requirements $`| \mathcal{R} |`$. Higher is better.

- MoP3: (float) Final element-wise verification rate $`\mathcal{V}' = \sum_{r \in \mathcal{R}} \frac{\sum_{e \in r} \frac{|e_{valid}|}{|e|}}{| \mathcal{R} |}`$, i.e., total number of elements $`|e_{valid}|`$ for each requirement $`r \in \mathcal{R}`$ verifying requirement $`r`$ (given $`|e|`$ elements concerned by this requirement), over the total number of requirements $`|\mathcal{R}|`$. Higher is better.

- MoP4: (integer) $`\mathcal{X} =\lVert \mathbf{x}_{lab} \rVert_1 + \lambda_{\frac{lab}{ind}} \lVert \mathbf{x}_{ind} \rVert_1 + \lambda_0 \lVert \mathbf{x} \rVert_0`$, where $`\lVert \cdot \rVert_1`$ and $`\lVert \cdot \rVert_0`$ denote the $`\ell_1`$ and $`\ell_0`$ norms respectively, and $`\mathbf{x}`$ is the concatenation of $`\mathbf{x}_{lab}`$ and $`\mathbf{x}_{ind}`$ gathering the number of experiments per laboratory and industrial use case (if any laboratory use case is used). The first two terms penalise the total number of experiments, with higher weights on experiments performed on industrial use cases (a 1:5 ratio is used, $`\lambda_{\frac{lab}{ind}}=5`$). The last term penalises the use of multiple use cases (here, $`\lambda_0 = 2`$). Lower is better.

<!-- - Overall MoP: (float) ratio of verified MoP. -->


> Note: MoP1 to MoP3 assess the solution's effectiveness (ability to identify missing requirements, verify and validate), whereas MoP4 assesses the solution's sufficiency (ability to verify and validate with as few experiments as possible, i.e., as early as possible).

## Datasets

- [Robot arm] <span style="color:red">tbd</span>

- [WONKA case study](wonka_case_study/wonka_case_study.md)
**GOAL: verify and validate a scientific approach on multiple *industrial systems*, given some *laboratory systems*. The solution shall enable systems engineer to correct, complete and verify specifications as early as possible (before/after experiments on laboratory systems, before/after experiments on industrial systems).**
Five use cases are considered: 3 laboratory systems (1 coffee machine, 1 robot arm, 1 3D printer) and 2 industrial systems (1 temperature-controlled vehicle testbed denoted $`ind1`$ and 1 mixing/conching machine from a chocolate factory denoted $`ind2`$). Additional instrumentation come with all systems.
This case study consists of (i) all five cyber-physical systems in their environments with their description (system, purpose and initial requirements), (ii) an ontology tailored to mechatronic systems, (iii) a formal description of all use cases using this ontology.
[see more details](wonka_case_study/wonka_case_study.md)

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

| Solution | MoP1  |                      MoP2                      |                       MoP3                       |     MoP4      |
| -------- | :---: | :--------------------------------------------: | :----------------------------------------------: | :-----------: |
| WONKA    |  $`n_{new\_req}=3`$  | $`\mathcal{V}_{ind1}=50\%`$<br />$`\mathcal{V}_{ind2}=68\%`$ | $`\mathcal{V}'_{ind1}=75\%`$<br />$`\mathcal{V}'_{ind2}=96\%`$ | $`\mathcal{X}=`$ |

  <!-- 
  | Solution | MoP1  | MoP2  | MoP3  | MoP4  |
  | -------- | :---: | :---: | :---: | :---: |
  |          |       |       |       |       |
  -->


## Meta-Analysis <span style="color:red">tbd</span>

## References

[1] Delabeye, R., Penas, O., & Plateaux, R. (2022, October). Scalable ontology-based V&V process for heterogeneous systems and applications. In Proceedings of the 25th International Conference on Model Driven Engineering Languages and Systems: Companion Proceedings (pp. 341-350).