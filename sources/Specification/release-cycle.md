| [Introduction](../Introduction/index.md) | [News and events](.../News-and-events/index.md) | [Specification](../Specification/index.md) | [Tools](../Tools/index.md) | [Resources](../Resources/index.md) | [FAQ](../FAQ/index.md) | [About](../About/index.md) |
| ---------------------------------------- | ----------------------------------------------- | ------------------------------------------ | -------------------------- | ---------------------------------- | ---------------------- | -------------------------- |

| [Overview](index.md) | [Release cycle, eFMI versioning and backwards compatibility](release-cycle.md) | [Reporting specification issues and new feature proposals](reporting-specification-issues-and-new-feature-proposals.md) | [Current stable releases](current-stable-releases.md) | [Candidate-drafts of next release](candidate-drafts-of-next-release.md) | [Old stable releases](old-stable-releases.md) |
| ----------------------- | ----------------------------------------------------------- | ------------------------------------------------------------ | ----------------------------------------------------- | ------------------------------------------------------------ | --------------------------------------------- |

# Release cycle, eFMI versioning and backwards compatibility

## Overview

We are currently in the second year of development. The latest candidate-draft is the _eFMI Standard 1.0.0 Alpha 4_. We expect the _Voting Candidate_ about the first quarter of 2023.

We aim to release a new major eFMI Standard version about every 2 years. In the first year new features are collected and defined, i.e.,

* What, why, limitations, test scenarios, prototype implementations *and*…
* …feasibility study that a specification can achieve completeness of rules that can be reasonably implemented -- _"somebody tries to put it into rules and plays the evil guy trying to break these"_.

In the 2nd year, the proposed and accepted features are cleaned up; no new features are accepted and _"if in doubt, accepted features are cut"_; this comprises:

* Actual specification in standard.
* Cleanup and prepare release of MAP eFMI toolings/libraries.
* Tool vendors cleanup their prototype implementations used in crosschecks to be ready for release.
* Features not crosschecked or with failing crosschecks are cut.

We avoid minor standard versions. Such are *only* for bug-fixes. We are rigorous to make sure everything works before we release a major version; hence there should be less to no need for bug-fixing. To that end major releases are only ready if, and only if, all features are tested in tooling crosschecks. This means, that eFMI Standard releases and tooling releases are coordinated. After all, the eFMI technology is not useful of users have no access to a working toolchain from high-level a-causal modeling and simulation to target-specific embedded code.

## Release cycle

First candidate-drafts of a new eFMI Standard version are earliest released in the second year of development. Typically there are an _Alpha 1_, _Alpha 2_, _Beta 1_, _Beta 2_ and finally _Voting Candidate_ draft versions of the currently developed standard before its final release, roughly evenly spread out within the second year.

The _Alpha_ versions are likely incomplete with open TODO sections. The _Beta_ versions are complete, but with edges and corners that are to be polished. The _Voting Candidate_ is polished and as far as we know the final version. We only expect typo and minor language improvements as feedback; otherwise this is the candidate we will push in the Modelica Association for public release approval.

## eFMI versioning

All artefacts released by MAP eFMI -- e.g., the eFMI specification, XML Schemas for container manifests, example eFMUs, the [_eFMI Container Manager_](https://github.com/modelica/efmi-containermanager), [_eFMI Compliance Checker_](https://github.com/modelica/efmi-compliancechecker) and [eFMI crosscheck test cases](https://github.com/modelica/efmi-testcases) -- use a certain versioning scheme consisting of three digits of the form `MAJOR.MINOR.PATCH`. In principle the scheme follows [Semantic Versioning 2.0.0](https://semver.org/), with the following additional restrictions:

* For the eFMI specification, the `MAJOR` digit is the eFMI Standard version it is specifying.
* If there is ever a need for a new `MINOR` eFMI specification version, all artefacts and tooling must provide new releases (incorporating any fix as needed of course), increasing their `MINOR` digit respectively. I.e., the `MINOR` digit denotes consecutive bug-fix releases of artefacts/tools incorporating fixes as defined by the respective eFMI specification.
* The `PATCH` digit is only used by artefacts and tooling, not the eFMI specification.

E.g., a _eFMI Container Manager_ release 1.1.3 is the third release of the tool for the first eFMI Standard as defined by the eFMI specification version 1.1.0.

## eFMI backwards compatibility

Our target domain -- embedded, safety critical, real time software -- is strict, in fact ridiculous strict, when it comes to documenting, archiving and sticking to the defined tooling versions throughout the whole development cycle of an embedded project. Changing tooling in the middle of embedded development projects comes with _severe_ requirements on documentation and certification. In fact, it is not likely to be required because the used tooling is typically extensively tested, or even certified, before being deployed. It is very unlikely that a show-stopper bug is encountered, which means that one is much better of to work around minor bugs than going through the hassle to document and recertify a tool change.

Considering that the eFMI technology requires a tool chain, we can safely assume that once picked, an embedded software development project sticks with the given eFMI Standard until the project end. Hence, we do not have to take care of backwards compatibility from the perspective of the eFMI Standard. In our domain, one is rather better off by rigorously fixing shortcomings and cleaning up the specification instead of taking care of backwards compatible second quality solutions.

MAP eFMI therefore reserves the right of -- and in fact very likely will introduce -- backwards compatibility breaking eFMI Standard changes from one `MAJOR` version to the next. Embedded developers can switch to new eFMI tooling at the beginning of their next project (which can in fact be to port a released version of an existing project to the new eFMI Standard as part of its next release -- a task that should not be underestimated).
