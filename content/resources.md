---
title: Resources
contactFooter: true
---

This page provides _selected_ MAP eFMI publications, most importantly the _eFMI Standard_, but also accompanying documents like example eFMUs, introductory presentations, overview papers, project reports and forms etc. For an overview of 3rd party eFMI tooling, please consult the [Tools page](/tools/). The publications of MAP eFMI can be categorized in:

{{< toc >}}
 
## _eFMI Standard_ releases

**Most recent stable release**

There exists no current stable release yet. The first release will be the upcoming _eFMI Standard 1.0.0_; please cf. its current candidate-drafts.

**Current candidate-drafts**

The next major upcoming _eFMI Standard_ release is version 1.0.0; below are the candidate-drafts for it. Please cf. [the release cycle](/standard/#Release-cycle-and-versioning) for details about the release schedule and for an estimation of maturity of candidate-drafts.

 - _eFMI Standard 1.0.0 Alpha 4 (2021-02-22)_:
   - [_eFMI Standard 1.0.0 Alpha 4_ (zip)](/media/resources/eFMI-Standard-1.0.0-Alpha-4.zip)
   - [Specification text with change-marks to previous draft (PDF)](/media/resources/eFMI-Standard-1.0.0-Alpha-4-specification-text-changemarks.pdf)

**Previous stable releases**

There are no previous stable releases yet. We are still in the process of finishing the first official release; please cf. the current candidate-drafts.

## MAP eFMI published tooling

MAP eFMI provides a set of open source tools and libraries to foster the eFMI ecosystem. For not by MAP eFMI released tooling, including commercial tools, please cf. the [Tools page](/tools/). For final release distributions of MAP eFMI published tooling, please check each individual tool's repository; note, that we apply a unique [versioning scheme](/standard/#Versioning-scheme) such that every tool version can be mapped to the _eFMI Standard_ it supports and vice-versa. The tools published by MAP eFMI are:

 - [eFMI crosscheck test cases](https://github.com/modelica/efmi-testcases/releases): Official eFMI test cases for demonstrating and evaluating eFMI tooling. 
 - [eFMI Container Manager](https://github.com/modelica/efmi-containermanager/releases): Tool for creating, checking, reading and modifying eFMUs and their individual containers.
 - [eFMI Compliance Checker](https://github.com/modelica/efmi-compliancechecker/releases): Tool for checking eFMUs for conformance with the _eFMI Standard_. 

## Project organization

 - [MAP eFMI bylaws (PDF)](/media/resources/MAP-eFMI-bylaws.pdf)
 - [Membership application guidelines and form (PDF)](/media/resources/MAP-eFMI-application.pdf)
 - [Modelica Association Contributor License Agreement (MA CLA) (PDF)](/media/resources/Modelica-Association-CLA.pdf)

**Annual project reports at Modelica Association assembly meetings**

 - [Annual project report 2021](/media/resources/MAP-eFMI-annual-project-report-2021.pdf)
 
## Recommended documentation and introductory material{id="Recommended-documentation-and-introductory-material"}

**Overview and introduction**

 - [eFMI motivation and objectives teaser (mp4)](/media/resources/eFMI-Explained-in-4-Minutes.mp4):
   - 3:20-minutes video summarizing the application domain, motivation and objectives of the _eFMI Standard_. 
 - [eFMI overview paper (PDF)](https://doi.org/10.3384/ecp2118157) at the [14th International Modelica Conference](https://2021.international.conference.modelica.org/):
   - Comprehensive and highly recommended introductory overview paper about eFMI technology and the _eFMI Standard_.
 - [eFMI overview presentation (mp4)](/media/resources/Modelica-Conference-2021-MAP-eFMI.mp4) at the "FMI Industrial User Meeting" at the [14th International Modelica Conference](https://2021.international.conference.modelica.org/):
   - Video explaining how eFMI fits into the standards ecosystem of the [Modelica Association](https://modelica.org/) -- in particular compared to the [FMI Standard](https://fmi-standard.org) -- how eFMI containers look like and how the development of embedded solutions from high-level physics models is fostered by the eFMI workflow and accompanying existing tooling. A short overview of the MAP eFMI and its [development process and release cycle](/standard/) conclude the presentation.
 - [eFMI vs. FMI comparison (mp4)](/media/resources/eFMI-vs-FMI.mp4):
   - 3:26-minutes summary of the relation of eFMI compared to FMI, highlighting the need for another standard. 
 
**Use-cases and industrial applications**

 - [ITEA 3 EMPHYSIS industrial demonstrator report (PDF)](/media/resources/emphysis-public-demonstrator-summary.pdf):
   - Final report summarizing the industrial demonstrators developed in the [ITEA 3 Call 2](https://itea4.org/) project [EMPHYSIS](https://itea4.org/project/emphysis.html) (cf. the [About page](/about/#Project-history) for details about the relationship of MAP eFMI with EMPHYSIS). The report explains the used eFMI tooling and tool interactions, the performance assessement conducted to compare eFMI with state of the art embedded software development, the testsuite and unit tests to validate eFMI tooling compatibility (crosschecks) and the varying actual industrial demonstrators and their challenges and eFMI-based solution. 

## Example eFMUs

### Drivetrain torque controller with eFMI 1.0.0 Alpha 4

 - [eFMU (zip)](/media/resources/M04-example-eFMU-for-eFMI-1-0-0-Alpha-4.zip)

Example eFMU with Algorithm Code, Production Code, Binary Code and Behavioral Model containers for a drivetrain torque controller. The example and its original [Modelica](https://modelica.org/modelicalanguage.html) model defining the physics of the drivetrain (the plant model) are test case M04 of the [eFMI crosscheck test cases](https://github.com/modelica/efmi-testcases). The embedded controller developed in the eFMU is an approximated inverse model of the drivetrain plant model combined with a simple PI controller. The respective Modelica models of the test setup and controller are:

![M04-torque-controller](/media/resources/M04-example-scenario.png)

The example eFMU provides the following eFMI containers, each generated by varying eFMI tooling:

 - A Behavioral Model container providing two test scenarios and the original Modelica model defining the controller subject to embedded code generation.
 - An Algorithm Code container providing GALEC code -- i.e., an algorithmic, causal solution -- for the controller; it has been generated using [Dymola](https://www.3ds.com/products-services/catia/products/dymola/) (Dassault Systèmes).
 - 6 Production Code containers for the Algorithm Code container, generated using three different tools: _CATIA ESP_ (Dassault Systèmes), [TargetLink](https://www.dspace.com/en/pub/home/products/sw/pcgs/targetlink.cfm#180_25805) (dSPACE GmbH) and _SCODE-CONGRA_ (ETAS GmbH). With each tool two production codes are generated, a 32 Bit and a 64 Bit floating point precision version. All 6 production codes pass [MISRA C:2012](https://www.misra.org.uk/) checks with [Cppcheck 2.10](https://cppcheck.sourceforge.io/).
 - A Binary Code container for the 32 Bit production code of _CATIA ESP_, targeting Windows x86 and generated using _CATIA ESP_ (Dassault Systèmes).

[TPT](https://piketec.com/tpt/) (PikeTec GmbH) has been used to validate each production code against the scenarios of the Behavioral Model container. The respective test results are stored in `TestResult` folders of their respective Production Code containers. Minor differences due to floating point precision are visible by the TPT tests; still all 32 Bit compared to 64 Bit floating point precision results are within the tolerances of the test scenarios defined in the Behavioral Model container's manifest.

The final content of the collaboratively developed eFMU is:

![M04-torque-controller](/media/resources/M04-example-eFMU-content.png)

Note, that manifests link dependent containers for traceability. Production code manifests, for example, link back to the Algorithm Code container they implement by means of `ManifestReference` and individual `ForeignVariableReference` for each block-variable of the original GALEC code. eFMU consistency between dependent artefacts is ensured by means of SHA-1 checksums. For example, the GALEC code of an Algorithm Code container is listed as `File` element with a mandatory checksum; likewise, the `ManifestReference` of a Production Code container's manifest lists the checksum of the respective Algorithm Code container manifest it implements.

The `schemas` folder contains the XSD Schemas for all manifests as defined in the _eFMI Standard_ 1.0.0. The `__content.xml` of the eFMU's root directory lists all containers of the eFMU; it is the unique entry point for reading and working with the eFMU. 
