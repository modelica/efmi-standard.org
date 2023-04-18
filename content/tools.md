---
title: Tools
contactFooter: true
---

![eFMI tools](/media/tools/eFMI-tools.png)

This pages gives a short overview of, mostly commercial, third party eFMI tooling. Tooling released by MAP eFMI can be found on the [Resources page](/resources/#map-efmi-published-tooling).

The overview classifies each tool w.r.t. its support for the different container types defined by the _eFMI Standard_; the following abbreviations are used: eFMI Behavioral Model (**BM**), eFMI Algorithm Code (**AC**), eFMI Production Code (**PC**) and eFMI Binary Code (**BC**). Tools are listed in alphabetic order:

| | |
| :---: | :--- |
| [![AUTOSAR Builder](/media/tools/AUTOSAR-Builder.png)](https://www.3ds.com/products-services/catia/products/autosar-builder/) | _**AUTOSAR Builder**_ by [_Dassault Systèmes_](https://www.3ds.com), **Since version:** 23x |
| | **General scope:** IDE for modeling, testing and validation of in-vehicle embedded systems for the [AUTOSAR](https://www.autosar.org/) Classic and Adapaptive Platforms, facilitating seamless integration with other AUTOSAR compliant tools based on the [AUTOSAR Tool Platform (Artop)](https://www.artop.org/). |
| | **BM:** Generate AUTOSAR test components for the test scenarios defined in BM containers. |
| | **PC:** Adapt any eFMI PC container for the AUTOSAR Adaptive Platform, yielding an AUTOSAR Adaptive Platform compliant component ready for deployment in AUTOSAR-based target environments. |
| | **BC:** Build binaries of AUTOSAR adapted PC containers for software-in-the-loop (SiL) tests. |
| | |
| [![CATIA ESP](/media/tools/CATIA-ESP.png)](TODO) | _**CATIA ESP**_ by [_Dassault Systèmes_](https://www.3ds.com), **Since version:** 3DEXPERIENCE 2023 |
| | **General scope:** Embedded source code producer (ESP) on the [3DEXPERIENCE® platform](https://www.3ds.com/3dexperience), providing high quality code generation facilities for various Dassault Systèmes tooling, for example, [Cameo Systems Modeler](https://www.3ds.com/products-services/catia/products/no-magic/cameo-systems-modeler/).
| | **General eFMI features:** Seamless integration with Dymola supported. |
| | **PC:** Export of C production code satisfying [MISRA C:2012](https://www.misra.org.uk/). |
| | **BC:** Generation of BC containers for desktop environments to support software-in-the-loop (SiL) applications. |
| | |
| [![Dymola](/media/tools/Dymola.png)](https://www.3ds.com/products-services/catia/products/dymola/) | _**Dymola**_ by [_Dassault Systèmes_](https://www.3ds.com), **Since version:** 2022x |
| | **General scope:** [Modelica](https://modelica.org/modelicalanguage.html) IDE for the acausal, equation-based modeling and simulation of complex multi-domain physics. |
| | **General eFMI features:** Seamless integration of [_eFMI Container Manager_](https://github.com/modelica/efmi-containermanager) and [_eFMI Compliance Checker_](https://github.com/modelica/efmi-compliancechecker) for checking generated eFMUs. |
| | **BM:** Clocked simulation of [Modelica](https://modelica.org/modelicalanguage.html) source models, but no BM container export yet. |
| | **AC:** Export of GALEC code and manifest for [Modelica](https://modelica.org/modelicalanguage.html) models. GALEC obfuscation support. Modelica source models with tables, events, reinitialization and mixed-systems of equations are supported. |
| | **PC:** Seamless integration of CATIA ESP for PC container generation, with software-in-the-loop (SiL) simulation in Dymola and [MISRA C:2012](https://www.misra.org.uk/) checks via [Cppcheck](https://cppcheck.sourceforge.io/). |
| | **BC:** Seamless integration of CATIA ESP for BC container generation and export of eFMU as black-box co-simulation [FMU](https://fmi-standard.org/). |
| | |
| [![TargetLink](/media/tools/TargetLink.png)](https://www.dspace.com/en/pub/home/products/sw/pcgs/targetlink.cfm) | _**TargetLink**_ by [_dSPACE_](https://www.dspace.com/), **Since version:** 22.1 |
| | **General scope:** Production code generator for highly efficient C code straight from MathWorks® [Simulink®](https://www.mathworks.com/products/simulink.html)/[Stateflow®](https://www.mathworks.com/products/stateflow.html) models, supporting early verification through built-in simulation and testing, certified for ISO 26262, ISO 25119 and IEC 61508, and with support for the [AUTOSAR](https://www.autosar.org/) Classic and Adaptive Platforms. |
| | **General eFMI features:** Seamless integration of eFMI technology in dSPACE rapid prototyping and hardware-in-the-loop (HiL) ecosystem.
| | **PC:** Export of C production code satisfying [MISRA C:2012](https://www.misra.org.uk/). |
| | |
| [![TPT](/media/tools/TPT.png)](https://piketec.com/tpt/) | _**TPT**_ by [_PikeTec_](https://piketec.com/), **Since version:** 19 |
| | **General scope:** IDE for testing ECU software and embedded control systems in all development phases such as model-in-the-loop (MiL testing), software-in-the-loop (SiL testing), processor-in-the-loop (PiL testing), hardware-in-the-loop (HiL testing), ECU testing and vehicle testing, supporting relevant safety standards, such as ISO 26262, and test assessment, reporting, management and requirements traceability. |
| | **BM:** Testing of BM containers in many well-known embedded execution environments. |
| | **PC:** On the fly build of the C sources of PC containers for testing. |

&nbsp;

There are a few tools with prototype support for eFMI, but not yet released; these are, in alphabetic order: [Astrée](https://www.absint.com/astree/index.htm), [AUTOSAR Builder](https://www.3ds.com/products-services/catia/products/autosar-builder/), [Simcenter Amesim](https://plm.sw.siemens.com/en-US/simcenter/systems-simulation/amesim/) and [SimulationX](https://www.esi-group.com/products/simulationx). If you are a user of these tools and are interested in eFMI, please push the respective developers to bring their prototypes to an official release.