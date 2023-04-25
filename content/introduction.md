---
title: Introduction
contactFooter: true
---

![eFMI-physics-simulation-to-embedded-systems-bridge](/media/introduction/eFMI-bridge.png)

This page gives an overview of the general objectives and concepts of eFMI, its highlights and our project organization. Information about the project members and history can be found on the [About page](/about/). The topics covered in the following are:
 
{{< toc >}}

## eFMI Overview

In a nutshell, eFMI can be depicted as a bridge between the modeling & simulation and the embedded software world; it can be summarized in three sentences:

> _"The eFMI Standard is an open standard for the stepwise, model-transformation-based development of advanced control functions suited for safety-critical and real time targets. Its container architecture defines the common ground for collaboration among the stake-holders and toolchains along the various abstraction levels from high-level modeling and simulation – e.g., acausal, equation-based physics in Modelica – down to actual embedded code. The model representations it defines are interlinked for traceability and semi-automatic code generation and do not only capture functional, but also non-functional quality requirements like coding standards, static memory allocation, worst time execution, and documentation, enabling credible development within a standardized workspace."_ -- eFMI in three sentences.

### Objective

The main purpose of the _"[Modelica Association](https://modelica.org/) Project Functional Mock-up Interface for embedded systems"_ (MAP eFMI) is the development, standardization, and promotion of the _eFMI Standard_. The _eFMI Standard_ is an open standard for stepwise development and validation of advanced control functions suited for safety-critical and real time targets. It enables the application of high-level abstraction and simulation models -- like acausal physics models -- in embedded real-time and safety-critical software by providing a container architecture for the stepwise refinement of a first high-level algorithmic solution to an embedded implementation for some dedicated target environment.

### Container architecture and model representations

The _eFMI Standard_ can be thought of as a bridge closing the gap between the modeling and simulation world and the embedded software world. It defines a container architecture with various model representations to capture all activities of the required credible model transformation process:

- Behavior / reference results for testing (eFMI Behavioral Model containers).
- Target-independent algorithmic solution with guarantees on exception-free execution, error handling, worst time execution, and memory requirements (eFMI Algorithm Code container) based on eFMI GALEC (***G***uarded ***A***lgorithmic ***L***anguage for ***E***mbedded ***C***ontrol).
- C implementations tailored and optimized for the requirements of specific embedded execution environments (eFMI Production Code containers).
- Binary distributions and their build recipes, ready for embedded system integration (eFMI Binary Code containers).

### Collaborative workspaces (eFMUs)

Instances of the various eFMI container types -- each reflecting one aspect/step of the automatic transformation of some high-level model to an embedded solution -- are bundled in eFMUs (embedded Functional Mock-up Units). Each eFMU is one _shared/collaborative_ development workspace; shared hereby means that different stakeholders -- from simulation designers to embedded developers -- are working together using various eFMI tooling from different tool vendors in a seamless toolchain to eventually implement the final embedded solution(s). The various containers of an eFMU reflect the development steps and intermediate artefacts that have been incrementally developed. Each used tool can be dedicated and prove itself on one abstraction and transformation level. The whole toolchain compatibility is ensured by the _eFMI Standard_ and its common means for cross-referencing and dependency tracking for traceability, hashing (checksums) for automatic stale-artefact analysis and copyright, licensing and description annotations for intellectual property protection and documentation.

### Workflow and toolchain

The general eFMI workflow is sketched by the following figure, demonstrating an actual eFMI prototype toolchain that has been developed in the [EMPHYSIS](https://itea4.org/project/emphysis.html) research project, [which finished in February 2021](../about#project-history) (third party marks and brands are the property of their respective holders):

![eFMI-workflow](/media/introduction/eFMI-workflow.png)

The starting point of every eFMI-based development project is the generation (or manual development) of an algorithmic, sampled input-output-block in eFMI GALEC, a new real time and safety-critical domain suited imperative language for the definition of mathematical algorithms. Given a GALEC program in an eFMI Algorithm Code container generated by some simulation tooling, further model transformations along the various eFMI abstraction levels down to actual embedded code can be conducted with a respective eFMI toolchain provided by third party tool vendors assuming they support the targeted embedded execution environment and hardware architecture (target platform).

In the above example, the source is a physics model in [Modelica](https://modelica.org/modelicalanguage.html) and the final target a BOSCH MDG1 embedded control unit (ECU); the individual, mostly automatized development steps are:

* Generation of an algorithmic GALEC program from an acausal physics-equations model in Modelica (eFMI Algorithm Code container generated with, e.g., [CATIA DBM](https://my.3dexperience.3ds.com/welcome/compass-world/rootroles/dynamic-systems-engineer), [Simcenter Amesim](https://plm.sw.siemens.com/en-US/simcenter/systems-simulation/amesim/), [Dymola](https://dymola.com/) or [SimulationX](https://www.esi-group.com/products/simulationx)).
* Design and generation of reference test scenarios from simulations of the physics model (eFMI Behavioral Model containers generated with, e.g., [Dymola](https://dymola.com/)).
* Generation of production codes from the algorithmic GALEC solution (eFMI Production Code containers generated with, e.g., CATIA ESP or [TargetLink](https://www.dspace.com/en/pub/home/products/sw/pcgs/targetlink.cfm)).
* Generation of executable binary codes from production codes (eFMI Binary Code containers for, e.g., the [AUTOSAR Adaptive Platform](https://www.autosar.org/) generated with, e.g., [AUTOSAR Builder](https://www.3ds.com/products-services/catia/products/autosar-builder/)).
* Static program analyses and testing of production and binary codes with, e.g., [Astrée](https://www.absint.com/astree/index.htm) and [TPT](https://piketec.com/tpt/), on a concrete target platform, e.g., BOSCH MDG1.

### Proof of the pudding

The eFMI workflow presented in the previous section has been extensively tested using a prototype toolchain and industry-driven demonstrators developed throughout the [EMPHYSIS](https://itea4.org/project/emphysis.html) research project [from which MAP eFMI originates](../about#project-history). This experience is the _"proof of the pudding"_; consider the following results, speaking for themselves.

**Comprehensive examples:**

 - 11 industry-driven demonstrators, summarized in the [ITEA 3 EMPHYSIS industrial demonstrator report (PDF)](/media/resources/emphysis-public-demonstrator-summary.pdf). For example:
   - Semi-active damping controller with nonlinear inverse model and nonlinear Kalman filter (see [paper](https://www.mdpi.com/2076-0825/10/11/301))
   - Transmission model of whole drivetrain as virtual sensor
   - Dual-clutch transmission diagnosis virtual sensor
   - Powertrain vibration reduction controller
   - Advanced emergency braking system controller
 - An [open source Modelica library](https://github.com/modelica/efmi-testcases) with 22 test cases with ~40 real time simulation configurations
 - Requiring support for:
   - Inverse model or feedback linearization based control
   - Explicit and implicit fixed-step integration schemes
   - Solving linear equation systems
   - Mixed system of equations with mutually-dependent control-conditionals and physics
   - Event-based re-initialization of continuous states
   - Runtime tuning of tunable parameters
   - 1D and 2D interpolation of tables
   - Guaranteed error handling
   - Guaranteed saturation of control states, in- and outputs

**eFMI prototype support in established toolchain:**

 - eFMI prototype-extensions in 9 well-established commercial tools; 13 tool prototypes in total
 - Support for the whole eFMI workflow (Algorithm Code, Production Code, Binary Code and Behavioral Model containers)
 - Fifty well-tested workflow paths between various tools from different companies
 
**Uncompromising assessment:**

 - An assessment of eFMI vs. state-of-the-art hand-crafted embedded solutions, confirming (see [article](https://doi.org/10.4271/2021-26-0048)):
    - A productivity gain of ~90%
    - A speed-up in runtime of ~25-40%

**EMPHYSIS won the [ITEA Award of Excellence 2021](https://itea4.org/press-release/press-release-emphysis-the-missing-link-between-digital-simulation-and-embedded-software.html), honored with a _Special Vice-chairman award_ title for being one of the highest scored ITEA projects to date!**

![EMPHYSIS-ITEA-Award-of-Excellence](/media/about/EMPHYSIS-ITEA-Award-of-Excellence.png)

In the end, eFMI is easier to show than to describe. The magic is in the toolchain; the _eFMI Standard_ is not the user experience, but coordinates tool development and integration. As a user you can just enjoy a seamless toolchain from modeling to embedded implementation. Contact us for a demonstration of, for example, a toolchain from a [Modelica](https://modelica.org/modelicalanguage.html) physics-model of the [eFMI crosscheck test cases](https://github.com/modelica/efmi-testcases) 🡆 Modelica tool with support for eFMI GALEC code generation 🡆 Production code generator 🡆 to an [AUTOSAR Adaptive Platform](https://www.autosar.org/standards/adaptive-platform) component.

## eFMI highlights

Please note, that the first official release of the _eFMI Standard_, version 1.0.0, [is still in development](/resources/#_efmi-standard_-releases). It will comprise the following highlights:

* [Open, freely available](/standard/#_efmi-standard_-releases-and-licensing), community-developed standard under the umbrella of the non-profit [Modelica Association](https://modelica.org/).
* Driven by [open-source, research and industrial](/about/#map-efmi-members) tool-vendors and users from the modeling & simulation to the safety-critical embedded software domains.
* Supporting [tools](/tools/) are first-class in their field of expertise, e.g., physics modeling ([Dymola](https://dymola.com/)), embedded development and rapid prototyping ([TargetLink](https://www.dspace.com/en/pub/home/products/sw/pcgs/targetlink.cfm)), software- and Hardware-in-the-Loop (SiL, HiL) testing ([TPT](https://piketec.com/tpt/)) etc.
* All features are rigorously tested in tool-vendor crosschecks based on a [substantial test suite](https://github.com/modelica/efmi-testcases) of [Modelica](https://modelica.org/modelicalanguage.html) physics-models.
* Standardized workspace based on an open container architecture for cross-vendor toolchains, covering most important aspects for the automatic transformation of high-level models to embedded solutions. Supported containers are:
  * **Behavioral Model:** Reference behavior design and testing.
  * **Algorithm Code:** Target-independent intermediate-representation (IR) of solution algorithm in eFMI GALEC (***G***uarded ***A***lgorithm ***L***anguage for ***E***mbedded ***C***ontrol), a new high-level imperative language with guarantees on exception-free execution, error handling, worst time execution and memory requirements.
  * **Production Code:** C code tailored for a target-platform (embedded execution environment) satisfying real-time and safety-critical programming standards.
  * **Binary Code:** Build recipes and binaries for target-architecture, ready for deployment.
  * Common -- i.e., across all container types provided -- meta-information like cross-referencing for dependency tracking, checksums for automatic stale-artefact analysis, generation dates, copyright and licensing, container descriptions etc.

## Project organization and community

Development of the _eFMI Standard_ is organized as a [Modelica Association Project (MAP)](https://modelica.org/projects.html) under the roof of the [Modelica Association](https://modelica.org/). You can find an overview of the project objectives and members on the [About page](/about/#map-efmi-members) and the project bylaws and application forms on the [Resources page](/resources/#project-organization).

We follow a well-defined release-cycle and versioning scheme described on the [Standard page](/standard/#release-cycle-and-versioning). There, also details on how to report issues of the _eFMI Standard_ [can be found](/standard/#reporting-specification-issues-and-new-feature-requests). Note, that the currently in development _eFMI Standard_ version -- except [deliberately released candidate-drafts](/resources/#_efmi-standard_-releases) -- is not public, as is the specification repository; you have to be a project member to get access to our private repositories and an official saying in standardization decisions.

If you have any open questions, do not hesitate to write us on efmi-info@googlegroups.com.

And finally yet importantly, all material distributed by MAP eFMI, including on this website, [is open source](/about/#legal-information); please feel free to reuse it for explaining and promoting eFMI.