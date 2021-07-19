# Benchmark 1. Model-Based Systems Validation and Verification

This benchmark aims at building confidence in the usefulness of the new methods and tools with respect to the validation of specifications and the verification of designs. Qualitative and quantitative standardised metrics help to compare studies and to measure the technical progress.

## Glossary

To share a common undestanding of ambiguous concepts, contributors shall agree upon the following definitions:
- Requirement: 
- Specification: A set of requirements.
- Validation: confirmation, through objective evidence, that the requirements for a specific indended use or application have been fulfilled. A system is able to accomplish its indended use, goals and objectives (i.e., meet stakeholder requirements) in the intended operational environment. The righ system was built.
- Design: Definition of the architecture, system elements, interfaces, and other characteristics of a system or system element.
- Verification: confirmation, through objective evidence, that specified requirements have been fulfilled. 


## Requirements

- The solution shall enable systems engineers to specify correct requirements.
- The solution shall enable systems engineers to specify complete requirements.
- The solution shall enable systems engineers to specify correct specifications.
- The Solution shall enable systems engineers to specify complete specifications.
- The solution shall enable systems engineers to demonstrate that the designs meets the specifications.
- The solution shall enable systems engineers to demonstrate that the implementations meets the specifications.
- The solution shall enable systems engineers to vertically trace requirements.
- The solution shall enable systems engineers to horizontally trace requirements.
- The solution shall enable stakeholders, especially end-users, to experience the intended operational environment and the systems properties (behavioural and tructural) with a high degree of realism

## Measures of performance

## Datasets

- [Robot arm]

## 

|                                                              |                      **OPM**                      |            **Vitech**             |              **SA**               |             **WSAF**              |    **Piaszczyk**     |             **PBSE**              |          **SysML-based**          |                           **RFLP**                           |                         **vVDR**                          |                           **PMM**                            |
| :----------------------------------------------------------: | :-----------------------------------------------: | :-------------------------------: | :-------------------------------: | :-------------------------------: | :------------------: | :-------------------------------: | :-------------------------------: | :----------------------------------------------------------: | :-------------------------------------------------------: | :----------------------------------------------------------: |
| **System** **Simulation** *Discrete* *Continuous* *Hybrid* *Multiphysic* |               Basic logic animation               |       Basic logic Animation       |          Not documented           |   Basic animated logic sequence   |    Not documented    |          Not documented           |        Requires extensions        | Discrete synch Discrete asynch Continuous Hybrid Multiphysic | Discrete synchDiscrete asynchContinuousHybrid Multiphysic |  Discrete synchDiscrete asynchContinuousHybrid Multiphysic   |
|    **Process** *Top-Down* *Zig-**zagging* *Allow* *reuse*    |                  Not documented                   |         Layered top-down          |    Sequential  No zig-zagging     |     Sequential No zig-zagging     |      Sequential      |          Not documented           |  NoneSequential in some methods   |                          Sequential                          |                      Not documented                       | Top-downZig-zagging (Spec -> Design)Allow reuse at any level |
| **Operating** **Scenario** *Interactive* *Executable* *Batch* |                  Not documented                   |     Diagram (animated EFFBD)      |          Not documented           |             Wargaming             |   Diagram (static)   |         Diagram (static)          |         Diagram (static)          |                           Textual                            |                     Executable model                      | Interactive control panelExecutable modelList of executable scenarios |
| **Requirements** **Specification** *Executable* *Graphic* *Formal* |                  Not documented                   |           Informal text           |         Executable model          |           Informal text           |    Informal text     |           Informal text           |           Informal text           |                        Informal text                         |              Graphical modelExecutable model              | Graphical modelExecutable modelTextual statements when needed |
| **Requirements** **Validation** *Correctness* *Completeness* *Traceability* |                  Not documented                   |        Traceability links         |          Not documented           |   Basic animated logic sequence   | Traceability matrix  |          Not documented           |    Traceability links / matrix    |                      Requirements tree                       |                      Not documented                       | Formal validation Factual validation Dynamic traceabilityDerivation validation |
|        **Design**  *Equation* *Architecture* *Safety*        | Behaviour descriptionObject Process Diagram (OPD) | Behaviour descriptionArchitecture | Behaviour descriptionArchitecture | Behaviour descriptionArchitecture |    Not documented    | Behaviour descriptionArchitecture | Behaviour descriptionArchitecture |          Behaviour descriptionEquation Architecture          |                   EquationArchitecture                    |                 Equation ArchitectureSafety                  |
|                **Verification** *Simulation*                 |                  Not documented                   |        Traceability matrix        |          Not documented           |        Traceability links         | Traceability  matrix |        Traceability matrix        |    Traceability links / matrix    |             Traceability matrixParametric rules              |                       Co-simulation                       |                        Co-simulation                         |
|                 **Standards** *ARP* *4754A*                  |                     ISO 19450                     |               DoDAF               |          Not documented           |               DoDAF               |        DoDAF         |          Not documented           |          Not documented           |                        Not documented                        |                      Not documented                       |            ARP 4754A / ED 79AEIA 632ISO/IEC 15288            |
|                     **Tool** *Agnostic*                      |               OPCATGraphic editors                |            Vitech CORE            |          State Database           |            Vitech CORE            |    Not documented    |          Not documented           |         Various solutions         |                        Catia Systems                         |                  Agnostic3 valued logic                   |                           Agnostic                           |
|                   **Language** *Agnostic*                    |           Object Process Language (OPL)           |            Vitech CORE            |                SQL                |            Vitech CORE            |    Not documented    |          Not documented           |               SysML               |                        Catia Systems                         |                  Agnostic3 valued logic                   |                           Agnostic                           |


## Meta-Analysis

## References

