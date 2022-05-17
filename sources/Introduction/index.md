| [Introduction](../Introduction/index.md) | [News and events](.../News-and-events/index.md) | [_eFMI Standard_](../eFMI-Standard/index.md) | [Tools](../Tools/index.md) | [Resources](../Resources/index.md) | [FAQ](../FAQ/index.md) | [About](../About/index.md) |
| ---------------------------------------- | ----------------------------------------------- | ------------------------------------------ | -------------------------- | ---------------------------------- | ---------------------- | -------------------------- |

| [About eFMI](index.md) | [eFMI highlights](efmi-highlights.md) | [Project organization and community](project-organization-and-community.md) |
| ----------------------- | ----------------------- | ----------------------------------------------------------- |

![header-A4](resources\header-A4.png)

> The _eFMI Standard_ is an open standard for step-wise development of advanced control functions suited for safety-critical and real time targets. It is about the _development_ of _credible embedded solutions from high-level models_, such that not only functional, but also _non-functional quality requirements_ like MISRA C:2012, static memory allocation, worst time execution, traceability and documentation are met. It defines a common container architecture to foster interaction and integration of the _various stake-holders and tooling_ that are involved on the various levels of model transformation down to actual embedded code.

# About eFMI

The main purpose of the _"[Modelica Association](https://modelica.org/) Project Functional Mock-up Interface for embedded systems"_ (MAP eFMI) is the development, standardization and promotion of the _eFMI Standard_. The _eFMI Standard_ is an open standard for step-wise development and validation of advanced control functions suited for safety-critical and real time targets. It enables the application of high-level abstraction and simulation models -- like a-causal physics models -- in embedded real-time and safety-critical software by providing a container architecture for the step-wise refinement of a first high-level algorithmic solution to an embedded implementation for some dedicated target environment.

The _eFMI Standard_ can be thought of as a bridge closing the gap between the modelling and simulation world and the embedded software world. Its container architecture, and respective tooling, capture all activities of the required credible model transformation process:

- Behavior / reference results for testing (eFMI Behavioral Model containers).
- Target-independent algorithmic solution with guarantees on exception-free execution, error handling, worst time execution and memory requirements (eFMI Algorithm Code container) based on eFMI GALEC (_**G**_uarded _**A**_lgorithmic _**L**_anguage for _**E**_mbedded _**C**_ontrol).
- C implementations, tailored and optimized for the requirements of specific embedded execution environments (eFMI Production Code containers).
- Binary distributions and their build recipes, ready for embedded system integration (eFMI Binary Code containers).

Instances of these various container types -- each reflecting one aspect/step of the automatic transformation of some high-level model to an embedded solution -- are bundled in eFMUs. Each eFMU is one _shared_ development workspace; shared hereby means that different stake-holders, designers and developers are working together using various eFMI tooling from different tool vendors to eventually implement the final embedded solution(s). The various containers of the eFMU reflect the development steps and intermediate artefacts that have been incrementally developed. Each used tool can be dedicated and shine on one abstraction and transformation level. The whole toolchain compatibility is ensured by the _eFMI Standard_ and its common means for cross-referencing and dependency tracking for traceability, hashing (checksums) for automatic stale-artefact analysis and copyright, licensing and description annotations for intellectual property protection and documentation.

The general eFMI workflow is sketched by the following figure, demonstrating actual eFMI prototype tooling that has been developed in the [EMPHYSIS](https://itea4.org/project/emphysis.html) research project [which finished February 2021](../About/history.md):

![eFMI-workflow](resources/eFMI-workflow.png)

The individual, mostly automatized development steps are:

* Generation of an algorithmic GALEC program from an a-causal physics-equations model in [Modelica](https://modelica.org/modelicalanguage.html) (eFMI Algorithm Code container generated with, e.g., Amesim, Dymola or SimulationX).
* Design and generation of reference test scenarios from simulations of the physics model (eFMI Behavioral Model containers generated with, e.g., Dymola).
* Generation of production codes from the algorithmic GALEC solution (eFMI Production Code containers generated with, e.g., CATIA ESP, TargetLink oder SCODE-CONGRA).
* Generation of executable binary codes from production codes (eFMI Binary Code containers for, e.g., the [AUTOSAR Adaptive Platform](https://www.autosar.org/) generated with, e.g., AUTOSAR Builder).
* Static program analyses and testing of production and binary codes with, e.g., Astrée and TPT, on a concrete embedded control unit (ECU), e.g., Bosch MDG1.
