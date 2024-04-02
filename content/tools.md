---
title: Tools
contactFooter: true
---

![eFMI tools](/media/tools/eFMI-tools.png)

This pages gives a short overview of, mostly commercial, third party eFMI tooling. Tooling released by MAP eFMI can be found on the [Resources page](/resources/#map-efmi-published-tooling).

The overview classifies each tool w.r.t. its support for the different container types defined by the _eFMI Standard_; the following abbreviations are used: eFMI Behavioral Model (**BM**), eFMI Algorithm Code (**AC**), eFMI Production Code (**PC**) and eFMI Binary Code (**BC**). Tools are listed in alphabetic order (third party marks and brands are the property of their respective holders):

| | |
| :---: | :--- |
| [![AUTOSAR Builder](/media/tools/AUTOSAR-Builder.png)](https://www.3ds.com/products-services/catia/products/autosar-builder/) | [_**AUTOSAR Builder**_](https://www.3ds.com/products-services/catia/products/autosar-builder/) by [_Dassault Systèmes_](https://www.3ds.com), **Since version:** 23x |
| | **General scope:** IDE for modeling, testing and validation of in-vehicle embedded systems for the [AUTOSAR](https://www.autosar.org/) Classic and Adaptive Platforms, facilitating seamless integration with other AUTOSAR compliant tools based on the [AUTOSAR Tool Platform (Artop)](https://www.artop.org/). |
| | **BM:** Generate AUTOSAR test components for the test scenarios defined in BM containers. |
| | **PC:** Adapt any eFMI PC container for the AUTOSAR Adaptive Platform, yielding an AUTOSAR Adaptive Platform compliant component ready for deployment in AUTOSAR-based target environments. |
| | **BC:** Build binaries of AUTOSAR adapted PC containers for software-in-the-loop (SiL) tests. |
| | |
| [![Dymola](/media/tools/Dymola.png)](https://www.dymola.com/) | [_**Dymola**_](https://www.dymola.com/) by [_Dassault Systèmes_](https://www.3ds.com), **Since version:** 2023 |
| | **General scope:** [Modelica](https://modelica.org/modelicalanguage.html) IDE for the acausal, equation-based modeling and simulation of complex multi-domain physics. |
| | **General eFMI features:** Seamless integration of [_eFMI Container Manager_](https://github.com/modelica/efmi-containermanager) and [_eFMI Compliance Checker_](https://github.com/modelica/efmi-compliancechecker) for checking generated eFMUs. |
| | **BM:** Definition of test scenarios including tolerances, derived form existing continuous and clocked [Modelica](https://modelica.org/modelicalanguage.html) experiments, and generation of respective BM containers. Support for regression testing BM containers and software-in-the-loop (SiL) testing of Software Production Engineering generated PC containers. |
| | **AC:** Generation of GALEC code and manifest for [Modelica](https://modelica.org/modelicalanguage.html) models. GALEC obfuscation support. Modelica source models with tables, events, reinitialization and mixed-systems of equations are supported. |
| | **PC:** Seamless integration of Software Production Engineering for PC container generation, with SiL simulation in Dymola and [MISRA C:2012](https://www.misra.org.uk/) checks via [Cppcheck](https://cppcheck.sourceforge.io/). |
| | **BC:** Seamless integration of Software Production Engineering for BC container generation and export of eFMU as black-box co-simulation [FMU](https://fmi-standard.org/). |
| | |
| [![Software Production Engineering](/media/tools/Software-Production-Engineering.png)](https://my.3dexperience.3ds.com/welcome/compass-world/3dexperience-industries/transportation-and-mobility/smart-safe-and-connected/embedded-software-engineering/systems-software-production-engineer) | [_**Software Production Engineering**_](https://my.3dexperience.3ds.com/welcome/compass-world/3dexperience-industries/transportation-and-mobility/smart-safe-and-connected/embedded-software-engineering/systems-software-production-engineer) (former name _CATIA ESP_) by [_Dassault Systèmes_](https://www.3ds.com), **Since version:** 3DEXPERIENCE 2024x FD02 |
| | **General scope:** Production code generator on the [3DEXPERIENCE® platform](https://www.3ds.com/3dexperience), providing high quality code generation facilities for various target platforms, including the [AUTOSAR](https://www.autosar.org/) Classic and Adaptive Platforms.
| | **General eFMI features:** Seamless integration with Dymola supported. |
| | **PC:** Generation of C production code satisfying [MISRA C:2012](https://www.misra.org.uk/) from GALEC code in AC. |
| | **BC:** Generation of BC containers for desktop environments to support software-in-the-loop (SiL) applications. |
| | |
| [![TargetLink](/media/tools/TargetLink.png)](https://www.dspace.com/en/pub/home/products/sw/pcgs/targetlink.cfm) | [_**TargetLink**_](https://www.dspace.com/en/pub/home/products/sw/pcgs/targetlink.cfm) by [_dSPACE_](https://www.dspace.com/), **Since version:** 22.1 |
| | **General scope:** Production code generator for highly efficient C code straight from MathWorks® [Simulink®](https://www.mathworks.com/products/simulink.html)/[Stateflow®](https://www.mathworks.com/products/stateflow.html) models, supporting early verification through built-in simulation and testing, certified for ISO 26262, ISO 25119 and IEC 61508, and with support for the [AUTOSAR](https://www.autosar.org/) Classic and Adaptive Platforms. |
| | **General eFMI features:** Usage of eFMI technology in dSPACE TargetLink ecosystem and vice-versa.
| | **PC:** Generation of C production code satisfying [MISRA C:2012](https://www.misra.org.uk/) from GALEC code in AC. |
| | |
| [![TPT](/media/tools/TPT.png)](https://piketec.com/tpt/) | [_**TPT**_](https://piketec.com/tpt/) by [_PikeTec_](https://piketec.com/), **Since version:** 19 |
| | **General scope:** IDE for testing ECU software and embedded control systems in all development phases such as model-in-the-loop (MiL testing), software-in-the-loop (SiL testing), processor-in-the-loop (PiL testing), hardware-in-the-loop (HiL testing), ECU testing and vehicle testing, supporting relevant safety standards, such as ISO 26262, and test assessment, reporting, management and requirements traceability. |
| | **BM:** Testing of BM containers in many well-known embedded execution environments. |
| | **PC:** On the fly build of the C sources of PC containers for testing. |

&nbsp;

There are a few tools with prototype support for eFMI, but not yet released; these are, in alphabetic order: [Astrée](https://www.absint.com/astree/index.htm), [AUTOSAR Builder](https://www.3ds.com/products-services/catia/products/autosar-builder/), [Simcenter Amesim](https://plm.sw.siemens.com/en-US/simcenter/systems-simulation/amesim/) and [SimulationX](https://www.esi-group.com/products/simulationx). If you are a user of these tools and are interested in eFMI, please push the respective developers to bring their prototypes to an official release.