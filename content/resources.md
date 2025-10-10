---
title: Resources
contactFooter: true
---

![Modern warehouse with pallet rack storage system, © 2010, Axisadman, Attribution-ShareAlike 3.0 Unported (CC BY-SA 3.0)](/media/resources/modern-warehouse-with-pallet-rack-storage-system.png)

This page provides the by MAP eFMI published material: the _eFMI Standard_, selected recommended documentation and introductory material (overview papers, teaser videos, tutorials, etc), project organization documents (bylaws, application guidelines and forms, etc), and _eFMI Standard_ accompanying resources like crosscheck test cases and example eFMUs. Scientific publications are listed separately on the [Publications page](/publications/). For an overview of third party eFMI tooling, please consult the [Tools page](/tools/).

The resources provided on this page can be categorized in:

{{< toc >}}

## _eFMI Standard_ releases

**Most recent stable release**

There exists no current stable release yet. The first release will be the upcoming _eFMI Standard 1.0.0_; in the meantime, please see the current candidate-drafts.

**Current candidate-drafts**

The next major upcoming _eFMI Standard_ release is version 1.0.0; below are the candidate-drafts for it. Please see [the release cycle](/standard/#release-cycle-and-versioning) for details about the release schedule and for an estimation of maturity of candidate-drafts.

 - _eFMI Standard 1.0.0 Beta 1 (2024-07-02)_:
   - [_eFMI Standard 1.0.0 Beta 1_ (zip)](/media/resources/eFMI-Standard-1.0.0-Beta-1.zip)
 - _eFMI Standard 1.0.0 Alpha 4 (2021-02-22)_:
   - [_eFMI Standard 1.0.0 Alpha 4_ (zip)](/media/resources/eFMI-Standard-1.0.0-Alpha-4.zip)
   - [Specification text with change-marks to previous draft (PDF)](/media/resources/eFMI-Standard-1.0.0-Alpha-4-specification-text-changemarks.pdf)

**Previous stable releases**

There are no previous stable releases yet. We are still in the process of finishing the first official release; please see the current candidate-drafts.

## MAP eFMI published tooling

MAP eFMI provides a set of open source tools and libraries to foster the eFMI ecosystem. For tooling, including commercial tools, that are not MAP eFMI published, please see the [Tools page](/tools/). For final release distributions of MAP eFMI published tooling, please check each individual tool's repository; note that we apply a unique [versioning scheme](/standard/#versioning-scheme) such that every tool version can be mapped to the _eFMI Standard_ it supports and vice-versa. The tools published by MAP eFMI are:

 - [eFMI crosscheck test cases](https://github.com/modelica/efmi-testcases/releases): The official eFMI test cases for demonstrating and evaluating eFMI tooling. 
 - [eFMI Container Manager](https://github.com/modelica/efmi-containermanager/releases): A tool for creating, checking, reading and modifying eFMUs and their individual containers.
 - [eFMI Compliance Checker](https://github.com/modelica/efmi-compliancechecker/releases): A tool for checking eFMUs for conformance with the _eFMI Standard_. 

## Project organization

**Bylaws and membership application**

 - [MAP eFMI bylaws (PDF)](/media/resources/MAP-eFMI-bylaws.pdf)
 - [Membership application guidelines and form (PDF)](/media/resources/MAP-eFMI-application.pdf)
 - [Modelica Association Contributor License Agreement (MA CLA) (PDF)](/media/resources/Modelica-Association-CLA.pdf)

**Annual project reports at Modelica Association assembly meetings**

 - [Annual project report 2024 (PDF)](/media/resources/MAP-eFMI-annual-project-report-2024.pdf)
 - [Annual project report 2023 (PDF)](/media/resources/MAP-eFMI-annual-project-report-2023.pdf)
 - [Annual project report 2022 (PDF)](/media/resources/MAP-eFMI-annual-project-report-2022.pdf)
 - [Annual project report 2021 (PDF)](/media/resources/MAP-eFMI-annual-project-report-2021.pdf)

## Recommended documentation and introductory material{id="Recommended-documentation-and-introductory-material"}

### Teasers and overview material

 - [eFMI overview paper (PDF)](/media/resources/Modelica-Conference-2021-paper.pdf) at the [14th International Modelica Conference](https://2021.international.conference.modelica.org/):
   - A comprehensive and highly recommended introductory overview paper about eFMI technology and the _eFMI Standard_.
 - [eFMI motivation and objectives teaser (mp4)](/media/resources/eFMI-Explained-in-4-Minutes.mp4):
   - A 3:20-minutes video summarizing the application domain, motivation and objectives of the _eFMI Standard_. 
 - [eFMI vs. FMI lineup (mp4)](/media/resources/eFMI-vs-FMI.mp4):
   - A 3:32-minutes summary of the relation of eFMI compared to FMI, highlighting the need for another standard.
 - [eFMI® scope and delimitation (PDF)](/media/resources/eFMI-scope-and-delimitation.pdf)
   - Classification of eFMI w.r.t. related standards and ecosystems in the (physics) simulation and embedded software domain, highlighting its focus on (1) embedded software _development_, (2) single function-level design not composition & distributed-deployment and (3) non-functional quality criteria. The unique language design characteristics of eFMI GALEC are used to exemplify the focal point of eFMI: bringing acausal physics simulation to the safety-critical and hard real-time world all the way down to actual target hardware and their ecosystems.

### eFMI® tutorials

**eFMI® tutorial 2025**

A comprehensive eFMI tutorial has been presented at the [16th International Modelica & FMI Conference](https://modelica.org/events/modelica2025/), 8th of September 2025, Lucerne, Switzerland. The tutorial demonstrates the current state-of-the-art of available eFMI tooling in 5 parts (cf. [agenda slides (PDF)](/media/resources/eFMI-Tutorial-2025-Agenda.pdf)), including an eFMI overview, motivating example, hands-on, advanced examples and industry use-case:

 - **Part 1 -- eFMI® motivation and overview:** High-level overview of the _eFMI Standard_ and workflow from acausal physics models in Modelica® down to embedded target code. ([recording (mp4)](/media/resources/eFMI-Tutorial-2025-Part-1.mp4), [slides (PDF)](/media/resources/eFMI-Tutorial-2025-Part-1.pdf))
 - **Part 2 -- Running use-case introduction:** Comprehensible Modelica® example demonstrating the advantages and beauty of eFMI. The use-case is an electric vehicle drivetrain torque controller to reduce drivetrain vibrations, using a simple inverse model of the elastic drivetrain (virtual sensor) to feed -- and thereby improve the behavior of -- a off-the-shelf PI controller from the Modelica Standard Library. ([recording (mp4)](/media/resources/eFMI-Tutorial-2025-Part-2.mp4), [slides (PDF)](/media/resources/eFMI-Tutorial-2025-Part-2.pdf))
 - **Part 3 -- Hands-on in Dymola and Software Production Engineering:** Hands-on experience in [Dymola](https://www.dymola.com/) (Dassault Systèmes) and [Software Production Engineering](https://my.3dexperience.3ds.com/welcome/compass-world/3dexperience-industries/transportation-and-mobility/smart-safe-and-connected/embedded-software-engineering/systems-software-production-engineer) (Dassault Systèmes) to generate an eFMU for the example of Part 2. Besides final software-in-the-loop (SiL) and recalibration tests, the generated eFMU and its various intermediate model representations are investigated, focusing on the non-functional quality criteria satisfied by the generated solution, like traceability between eFMU containers, MISRA C:2023 compliance of generated production code and other code quality criteria like static memory allocation and error handling. Also, tooling to import eFMI production code in [Simulink®](https://www.mathworks.com/products/simulink.html) (The MathWorks, Inc.) as C Function blocks or to export production code as [Arduino®](https://www.arduino.cc/) sketch is presented. ([recording (mp4)](/media/resources/eFMI-Tutorial-2025-Part-3.mp4), [slides (PDF)](/media/resources/eFMI-Tutorial-2025-Part-3.pdf))
 - **Part 4 -- Advanced demonstrators:** Two advanced examples demonstrating how eFMI can help with the development of advanced hard real-time model-predictive control in safety-critical embedded environments. The first example is a battery management system (BMS) where the battery cell model is used as virtual sensor to predict the cell core tempurate, such that power requests can be limited to avoid battery damage due to overheating. The second example is a quarter car vehicle model (QVM), that is a hybrid physics and neural networks (NN) model -- a so called physics-enhanced neural ordinary differential equations system (PeN-ODE) -- with the unknown non-linear physics of the suspension incorporated by NN surrogate models that are well integrated with known physics of the QVM. ([recording (mp4)](/media/resources/eFMI-Tutorial-2025-Part-4.mp4), [slides (PDF)](/media/resources/eFMI-Tutorial-2025-Part-4.pdf), [battery management system life-demo at Dassault Systèmes booth (mp4)](/media/resources/eFMI-Tutorial-2025-Part-4-BMS-demo.mp4))
 - **Part 5 -- Industry case-study:** Industry use-case for the eFMI based development of a thermal management system (TMS) for a fuel cell electric vehicle (FCEV). ([recording (mp4)](/media/resources/eFMI-Tutorial-2025-Part-5.mp4), [slides (PDF)](/media/resources/eFMI-Tutorial-2025-Part-5.pdf))

**eFMI® tutorial 2023**

A comprehensive eFMI tutorial has been presented at the [15th International Modelica Conference](https://2023.international.conference.modelica.org/), 9th of October 2023, Aachen, Germany. The tutorial starts with a general eFMI motivation and overview, proceeds with a running example motivating eFMI, a hands-on to generate eFMUs for the running example with a step-by-step guide in [Dymola](https://www.dymola.com/) (Dassault Systèmes) and [Software Production Engineering](https://my.3dexperience.3ds.com/welcome/compass-world/3dexperience-industries/transportation-and-mobility/smart-safe-and-connected/embedded-software-engineering/systems-software-production-engineer) (Dassault Systèmes), followed by a live presentation of [TargetLink](https://www.dspace.com/en/pub/home/products/sw/pcgs/targetlink.cfm#180_25805) (dSPACE GmbH) support for eFMI production code generation and system integration in [Simulink®](https://www.mathworks.com/products/simulink.html) (The MathWorks, Inc.) and other dedicated embedded target environments -- including harware-in-the-loop simulation and binary code statistics for the running example -- and finally finishes with a short summary of further eFMI tooling, like [TPT](https://piketec.com/tpt/) (PikeTec GmbH) and [AUTOSAR Builder](https://www.3ds.com/products-services/catia/products/autosar-builder/) (Dassault Systèmes):

 - eFMI® Tutorial Agenda
 ([slides (PDF)](/media/resources/eFMI-Tutorial-2023-Agenda.pdf))
 - Part 1: eFMI® motivation and overview
 ([recording (mp4)](/media/resources/eFMI-Tutorial-2023-Part-1.mp4), [slides (PDF)](/media/resources/eFMI-Tutorial-2023-Part-1.pdf))
 - Part 2: Running use-case introduction
 ([recording (mp4)](/media/resources/eFMI-Tutorial-2023-Part-2.mp4), [slides (PDF)](/media/resources/eFMI-Tutorial-2023-Part-2.pdf))
 - Part 3: Hands on demonstration in Dymola and Software Production Engineering (former name _CATIA ESP_)
 ([recording (mp4)](/media/resources/eFMI-Tutorial-2023-Part-3.mp4), [slides (PDF)](/media/resources/eFMI-Tutorial-2023-Part-3.pdf))
 - Part 4: Live demonstration in TargetLink
 ([recording (mp4)](/media/resources/eFMI-Tutorial-2023-Part-4.mp4), [slides (PDF)](/media/resources/eFMI-Tutorial-2023-Part-4.pdf))
 - Part 5: Short presentation of further tooling
 ([recording (mp4)](/media/resources/eFMI-Tutorial-2023-Part-5.mp4), [slides (PDF)](/media/resources/eFMI-Tutorial-2023-Part-5.pdf))

### Use-cases and industrial applications

 - [ITEA 3 EMPHYSIS industrial demonstrator report (PDF)](/media/resources/emphysis-public-demonstrator-summary.pdf):
   - The final report summarizing the industrial demonstrators developed in the [ITEA 3 Call 2](https://itea4.org/) project [EMPHYSIS](https://itea4.org/project/emphysis.html) (see the [About page](/about/#project-history) for details about the relationship of MAP eFMI with EMPHYSIS). The report explains the used eFMI tooling and tool interactions, the performance assessment conducted to compare eFMI with state-of-the-art embedded software development, the test suite and unit tests to validate eFMI tooling compatibility (crosschecks) and the varying actual industrial demonstrators and their challenges and eFMI-based solution.

## Example eFMUs

### Drivetrain torque controller with eFMI 1.0.0 Alpha 4

 - [eFMU (zip)](/media/resources/M04-example-eFMU-for-eFMI-1-0-0-Alpha-4.zip)

Example eFMU with Algorithm Code, Production Code, Binary Code and Behavioral Model containers for a drivetrain torque controller. The example and its original [Modelica](https://modelica.org/modelicalanguage.html) model defining the physics of the drivetrain (the plant model) are test case M04 of the [eFMI crosscheck test cases](https://github.com/modelica/efmi-testcases). The embedded controller developed in the eFMU is an approximated inverse model of the drivetrain plant model combined with a simple PI controller. The respective Modelica models of the test setup and controller are:

![M04-torque-controller](/media/resources/M04-example-scenario.png)

The example eFMU provides the following eFMI containers, each generated by varying eFMI tooling:

 - A Behavioral Model container providing two test scenarios and the original Modelica model defining the controller subject to embedded code generation.
 - An Algorithm Code container providing GALEC code -- i.e., an algorithmic, causal solution -- for the controller; it has been generated using [Dymola](https://www.dymola.com/) (Dassault Systèmes).
 - Four Production Code containers for the Algorithm Code container, generated using two different tools: [Software Production Engineering](https://my.3dexperience.3ds.com/welcome/compass-world/3dexperience-industries/transportation-and-mobility/smart-safe-and-connected/embedded-software-engineering/systems-software-production-engineer) (former name _CATIA ESP_) (Dassault Systèmes) and [TargetLink](https://www.dspace.com/en/pub/home/products/sw/pcgs/targetlink.cfm#180_25805) (dSPACE GmbH). With each tool two production codes are generated, a 32-Bit and a 64-Bit floating point precision version. All 4 production codes pass [MISRA C:2012](https://www.misra.org.uk/) checks with [Cppcheck 2.10](https://cppcheck.sourceforge.io/).
 - A Binary Code container for the 32-Bit floating point precision production code of _Software Production Engineering_, targeting Windows x86 and generated using _Software Production Engineering_.

[TPT](https://piketec.com/tpt/) (PikeTec GmbH) has been used to validate each production code against the scenarios of the Behavioral Model container. The respective test results are stored in `TestResult` folders of their respective Production Code containers. Minor differences due to floating point precision are visible by the TPT tests; still all 32-Bit compared to 64-Bit floating point precision results are within the tolerances of the test scenarios defined in the Behavioral Model container's manifest.

The final content of the collaboratively developed eFMU is:

![M04-torque-controller](/media/resources/M04-example-eFMU-content.png)

Note that manifests link dependent containers for traceability. Production code manifests, for example, link back to the Algorithm Code container they implement by means of `ManifestReference` and individual `ForeignVariableReference` for each block-variable of the original GALEC code. eFMU consistency between dependent artefacts is ensured by means of SHA-1 checksums. For example, the GALEC code of an Algorithm Code container is listed as `File` element with a mandatory checksum; likewise, the `ManifestReference` of a Production Code container's manifest lists the checksum of the respective Algorithm Code container manifest it implements.

The `schemas` folder contains the XSD Schemas for all manifests as defined in the _eFMI Standard_ 1.0.0. The `__content.xml` of the eFMU's root directory lists all containers of the eFMU; it is the unique entry point for reading and working with the eFMU. 
