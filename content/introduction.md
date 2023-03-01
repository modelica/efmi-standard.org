---
title: Introduction
---

![eFMI-physics-simulation-to-embedded-systems-bridge](/media/introduction/eFMI-bridge.png)

[//]: # "# eFMI introduction: Overview, highlights and project organization"

This page gives an overview of the general objectives and concepts of eFMI, its highlights and our project organization. Information about the project members and history can be found on the [About page](/about/). The topics covered in the following are:
 1. [eFMI Overview](#eFMI-overview)
    - [Objective](#Objective)
	- [Container architecture and model representations](#Container-architecture-and-model-representations)
	- [Collaborative workspaces (eFMUs)](#Collaborative-workspaces-eFMUs)
	- [Workflow and tooling](#Workflow-and-tooling)
	- [Proof of the pudding](#Proof-of-the-pudding)
 2. [eFMI highlights](#eFMI-highlights)
 3. [Project organization and community](#Project-organization-and-community)

In a nutshell, eFMI can be depicted as a bridge between the modelling & simulation and the embedded software world; it can be summarized in three sentences:

> _"The eFMI Standard is an open standard for the step-wise, model-transformation-based development of advanced control functions suited for safety-critical and real time targets. Its container architecture defines the common ground for collaboration among the stake-holders and tooling along the various abstraction levels from high-level -- e.g., a-causal, equation-based physics -- modelling and simulation down to actual embedded code. The model representations it defines are interlinked for traceability and semi-automatic code generation and do not only capture functional, but also non-functional quality requirements like coding standards, static memory allocation, worst time execution and documentation, eventually enabling credible development within a standardized workspace."_ -- eFMI in three sentences.

# eFMI overview{id="eFMI-overview"}

### Objective{id="Objective"}

The main purpose of the _"[Modelica Association](https://modelica.org/) Project Functional Mock-up Interface for embedded systems"_ (MAP eFMI) is the development, standardization and promotion of the _eFMI Standard_. The _eFMI Standard_ is an open standard for step-wise development and validation of advanced control functions suited for safety-critical and real time targets. It enables the application of high-level abstraction and simulation models -- like a-causal physics models -- in embedded real-time and safety-critical software by providing a container architecture for the step-wise refinement of a first high-level algorithmic solution to an embedded implementation for some dedicated target environment.

### Container architecture and model representations{id="Container-architecture-and-model-representations"}

The _eFMI Standard_ can be thought of as a bridge closing the gap between the modelling and simulation world and the embedded software world. It defines a container architecture with various model representations to capture all activities of the required credible model transformation process:

- Behavior / reference results for testing (eFMI Behavioral Model containers).
- Target-independent algorithmic solution with guarantees on exception-free execution, error handling, worst time execution and memory requirements (eFMI Algorithm Code container) based on eFMI GALEC (***G***uarded ***A***lgorithmic ***L***anguage for ***E***mbedded ***C***ontrol).
- C implementations, tailored and optimized for the requirements of specific embedded execution environments (eFMI Production Code containers).
- Binary distributions and their build recipes, ready for embedded system integration (eFMI Binary Code containers).

### Collaborative workspaces (eFMUs){id="Collaborative-workspaces-eFMUs"}

Instances of the various eFMI container types -- each reflecting one aspect/step of the automatic transformation of some high-level model to an embedded solution -- are bundled in eFMUs (embedded Functional Mock-up Units). Each eFMU is one _shared/collaborative_ development workspace; shared hereby means that different stake-holders -- from simulation designers to embedded developers -- are working together using various eFMI tooling from different tool vendors to eventually implement the final embedded solution(s). The various containers of an eFMU reflect the development steps and intermediate artefacts that have been incrementally developed. Each used tool can be dedicated and shine on one abstraction and transformation level. The whole toolchain compatibility is ensured by the _eFMI Standard_ and its common means for cross-referencing and dependency tracking for traceability, hashing (checksums) for automatic stale-artefact analysis and copyright, licensing and description annotations for intellectual property protection and documentation.

### Workflow and tooling{id="Workflow-and-tooling"}

The general eFMI workflow is sketched by the following figure, demonstrating actual eFMI prototype tooling that has been developed in the [EMPHYSIS](https://itea4.org/project/emphysis.html) research project [which finished February 2021](../about#Project-history):

![eFMI-workflow](/media/introduction/eFMI-workflow.png)

Starting point of every eFMI-based development project is the generation (or manual development) of an algorithmic, sampled input-output-block in eFMI GALEC, a new real time and safety-critical domain suited imperative language for the definition of mathematical algorithms. Given a GALEC program in an eFMI Algorithm Code container generated by some simulation tooling, further model transformations along the various eFMI abstraction levels down to actual embedded code can be conducted with respective eFMI tooling provided by third party tool vendors assuming they support the targeted embedded execution environment and hardware architecture (target platform).

In above example, the source is a physics model in [Modelica](https://modelica.org/modelicalanguage.html) and the final target a BOSCH MDG1 embedded control unit (ECU); the individual, mostly automatized development steps are:

* Generation of an algorithmic GALEC program from an a-causal physics-equations model in Modelica (eFMI Algorithm Code container generated with, e.g., Amesim, Dymola or SimulationX).
* Design and generation of reference test scenarios from simulations of the physics model (eFMI Behavioral Model containers generated with, e.g., Dymola).
* Generation of production codes from the algorithmic GALEC solution (eFMI Production Code containers generated with, e.g., CATIA ESP, TargetLink oder SCODE-CONGRA).
* Generation of executable binary codes from production codes (eFMI Binary Code containers for, e.g., the [AUTOSAR Adaptive Platform](https://www.autosar.org/) generated with, e.g., AUTOSAR Builder).
* Static program analyses and testing of production and binary codes with, e.g., Astrée and TPT, on a concrete target platform, e.g., BOSCH MDG1.

### Proof of the pudding{id="Proof-of-the-pudding"}

A

# eFMI highlights{id="eFMI-highlights"}

Please note, that the first release of the _eFMI Standard_, version 1.0.0, [is still in development](../eFMI-Standard/candidate-drafts-of-next-release.md). It will comprise the following highlights:

* [Open](../eFMI-Standard/index.md), [freely available](../eFMI-Standard/current-stable-releases.md), community-developed standard under the umbrella of the non-profit [Modelica Association](https://modelica.org/).
* Driven by [open-source, research and industrial](project-organization-and-community.md##Project members) tool-vendors and users from the modelling & simulation to the safety-critical embedded software domains.
* Supporting [tools](../Tools/index.md) are first-class in their field of expertise, e.g., physics modeling (Dymola 2023), embedded development and rapid prototyping (TargetLink 2022 B), software- and Hardware-in-the-Loop (SiL, HiL) testing (TPT 19) etc.
* All features are rigorously tested in tool-vendor crosschecks based on a [substantial testsuite](https://github.com/modelica/efmi-testcases) of [Modelica](https://modelica.org/modelicalanguage.html) physics-models.
* Standardized workspace based on an open container architecture for cross-vendor tooling integration, covering most important aspects for the automatic transformation of high-level models to embedded solutions. Supported containers are:
  * **Behavioral Model:** Reference behavior design and testing.
  * **Algorithm Code:** Target-independent intermediate-representation (IR) of solution algorithm in eFMI GALEC (***G***uarded ***A***lgorithm ***L***anguage for ***E***mbedded ***C***ontrol), a new high-level imperative language with guarantees on exception-free execution, error handling, worst time execution and memory requirements.
  * **Production Code:** C code tailored for a target-platform (embedded execution environment) satisfying real-time and safety-critical programming standards.
  * **Binary Code:** Build recipes and binaries for target-architecture, ready for deployment.
  * Common -- i.e., across all container types provided -- meta-information like cross-referencing for dependency tracking, checksums for automatic stale-artefact analysis, generation dates, copyright and licensing, container descriptions etc.

# Project organization and community{id="Project-organization-and-community"}
