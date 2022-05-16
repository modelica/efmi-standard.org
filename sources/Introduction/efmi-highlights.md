| [Introduction](../Introduction/index.md) | [News and events](.../News-and-events/index.md) | [_eFMI Standard_](../eFMI-Standard/index.md) | [Tools](../Tools/index.md) | [Resources](../Resources/index.md) | [FAQ](../FAQ/index.md) | [About](../About/index.md) |
| ---------------------------------------- | ----------------------------------------------- | ------------------------------------------ | -------------------------- | ---------------------------------- | ---------------------- | -------------------------- |

| [About eFMI](index.md) | [eFMI highlights](efmi-highlights.md) | [Project organization and community](project-organization-and-community.md) |
| ----------------------- | ----------------------- | ----------------------------------------------------------- |

# eFMI highlights

Please note, that the first release of the _eFMI Standard_, version 1.0.0, [is still in development](../eFMI-Standard/candidate-drafts-of-next-release.md). It will comprise the following highlights:

* [Open](../eFMI-Standard/index.md), [freely available](../eFMI-Standard/current-stable-releases.md), community-developed standard under the umbrella of the non-profit [Modelica Association](https://modelica.org/).
* Driven by [open-source, research and industrial](project-organization-and-community.md##Project members) tool-vendors and users from the modelling & simulation to the safety-critical embedded software domains.
  * E.g., [Dassault Sysèmes](https://www.3ds.com/), [Deutsche Zentrum für Luft- und Raumfahrt e. V.](https://www.dlr.de/), [dSPACE GmbH](https://www.dspace.com/), [Mercedes-Benz AG](https://www.mercedes-benz.com/), [Mitsubishi Electric Research Laboratories](https://www.merl.com/), [Modelon AB](https://www.modelon.com/), [Open Source Modelica Consortium](https://openmodelica.org/home/consortium), [Robert Bosch GmbH](https://www.bosch.com/) or [Siemens Digital Industries Software](https://www.sw.siemens.com/).
* Standardized workspace based on an open container architecture for cross-vendor tooling integration, covering most important aspects for the automatic transformation of high-level models to embedded solutions. Supported containers are:
  * **Behavioral Model:** Reference behavior design and testing.
  * **Algorithm Code:** Target-independent intermediate-representation (IR) of solution algorithm in eFMI GALEC (_**G**_uarded _**A**_lgorithm _**L**_anguage for _**E**_mbedded _**C**_ontrol), a new high-level imperative language with guarantees on exception-free execution, error handling, worst time execution and memory requirements.
  * **Production Code:** C code tailored for a target-platform (embedded execution environment) satisfying real-time and safety-critical programming standards.
  * **Binary Code:** Build recipes and binaries for target-architecture, ready for deployment.
  * Common -- i.e., across all container types provided -- meta-information like cross-referencing for dependency tracking, checksums for automatic stale-artefact analysis, generation dates, copyright and licensing, container descriptions etc.
* All features are rigorously tested in tool-vendor crosschecks based on a [substantial testsuite](https://github.com/modelica/efmi-testcases) of [Modelica](https://modelica.org/modelicalanguage.html) physics-models.
* Supporting [tools](../Tools/index.md) are first-class in their field of expertise, e.g., physics-modeling (Dymola 2023), embedded development and rapid prototyping (TargetLink 2022 B), software- and Hardware-in-the-Loop (SiL, HiL) testing (TPT 19) etc.
