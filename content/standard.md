---
title: Standard
---

[//]: # "# _eFMI Standard_: Licensing, release cycle and release schedule"

This page gives a short overview of the development process of the _eFMI Standard_, its licensing, release cycle, backwards compatibility and issue system. The actual _eFMI Standard_ can be found on the [Resources page](/resources/). The topics covered in the following are:
 1. [eFMI Standard releases and licensing](#eFMI-Standard-releases-and-licensing)
 2. [Release cycle and versioning](#Release-cycle-and-versioning)
    - [General release organization](#General-release-organization)
	- [Schedule of individual releases](#Schedule-of-individual-releases)
	- [Versioning scheme](#Versioning-scheme)
 3. [Backwards compatibility](#Backwards-compatibility)
 4. [Reporting specification issues and new feature requests](#Reporting-specification-issues-and-new-feature-requests)

# eFMI Standard releases and licensing{id="eFMI-Standard-releases-and-licensing"}

The _eFMI Standard_ is a freely available, open, cross-community and cross-vendor developed standard.

There is not _the_ _eFMI Standard_ but many separate, self-contained, but incrementally-developed improvements, i.e., versions, of it. If it comes to releases of the _eFMI Standard_, we distinguish the [most recent stable, candidate-draft and previous stable](/resources/#eFMI-Standard-releases) versions. Each _eFMI Standard_ version consists of the actual specification text _and_ accompanying software artefacts the specification text refers to and leverages on for defining how valid eFMUs must look like and what their meaning is. Such accompanying software artefacts are for example the [XML Schema Definitions (XSD)](https://www.w3schools.com/xml/schema_intro.asp) for eFMU container manifests; they are distributed under [3-Clause BSD License](https://opensource.org/licenses/BSD-3-Clause). The actual specification text of each version is distributed under [CC BY-SA 4.0 License (Creative Commons Attribution-ShareAlike 4.0 International Public License)](https://creativecommons.org/licenses/by-sa/4.0/) as browsable single-page [HTML5](https://www.w3schools.com/html/) and as a printer-suited [Portable Document Format (PDF)](https://en.wikipedia.org/wiki/PDF) document. It is important to understand, that any version of the _eFMI Standard_ is the combination of both, actual specification text _and_ accompanying software artefacts the specification text refers to for defining valid eFMUs and their meaning; just the specification text without the referenced software artefacts is incomplete. All releases of the _eFMI Standard_ are therefore distributed as [Zip-archives](https://en.wikipedia.org/wiki/ZIP_(file_format)) including both, specification text and accompanying software artefacts. _eFMI Standard_ releases therefore ship with two licenses.

All other -- i.e., _not_ part of any _eFMI Standard_ version -- software artefacts and tooling provided by the MAP eFMI are released in coordination with _eFMI Standard_ releases (for details about the coordinated release of _eFMI Standard_ and tooling cf. [the release cycle](#Release-cycle-and-versioning)). Such support artefacts and tooling are released under [3-Clause BSD License](https://opensource.org/licenses/BSD-3-Clause). Examples for such support artefacts and tooling are example eFMUs for the varying _eFMI Standard_ versions, the [_eFMI Container Manager_](https://github.com/modelica/efmi-containermanager), [_eFMI Compliance Checker_](https://github.com/modelica/efmi-compliancechecker) and [eFMI crosscheck test cases](https://github.com/modelica/efmi-testcases).

_eFMI Standard_ releases and supporting artefacts and tooling are published on the [Resources page](/resources/).

# Release cycle and versioning{id="Release-cycle-and-versioning"}

## General release organization{id="General-release-organization"}

We are currently in the second year of our release cycle. The latest candidate-draft is the _eFMI Standard 1.0.0 Alpha 4_.

We aim to release a new major eFMI version (i.e., _eFMI Standard_ and related tooling) about every 2 years; that is our release cycle. In the first year new features are collected and defined, i.e., we design the:

* what, why, limitations, test scenarios, prototype implementations *and*…
* …feasibility study that a specification can achieve completeness of rules that can be reasonably implemented -- _"somebody tries to put it into rules and plays the evil guy trying to break these"_.

In the 2nd year, the proposed and accepted features are cleaned up; no new features are accepted and _"if in doubt, accepted features are cut"_; this comprises:

* Writing the actual specification.
* Cleanup and prepare release of MAP eFMI toolings and libraries.
* Tool vendors cleanup their prototype implementations used in crosschecks to be ready for release.
* Features not crosschecked by [official MAP eFMI tests](https://github.com/modelica/efmi-testcases) or failing crosschecks are cut.

We avoid minor standard versions. Such are *only* for bug-fixes. We are rigorous to make sure everything works before we release a major version; hence there should be no need for bug-fixing (although our [versioning scheme](#Versioning-scheme) still allows such in case of emergency). To that end major releases are only ready if, and only if, all features are tested in tooling crosschecks.

This means, that _eFMI Standard_ releases and tooling releases are coordinated (which is reflected in our [versioning scheme](#Versioning-scheme)). After all, the eFMI technology is not useful if users have no access to a working _toolchain_ from high-level a-causal modeling and simulation to target-specific embedded code.

## Schedule of individual releases{id="Schedule-of-individual-releases"}

First candidate-drafts of a new _eFMI Standard_ version are earliest released in the second year of development. Typically there are an _Alpha 1_, _Alpha 2_, _Beta 1_, _Beta 2_ and finally _Voting Candidate_ draft versions of the currently developed standard before its final release, roughly evenly spread out within the second year.

The _Alpha_ versions are likely incomplete with open _"to do"_ sections. The _Beta_ versions are complete, but with edges and corners that are to be polished. The _Voting Candidate_ is polished and as far as we know the final version. We only expect typo and minor language improvements as feedback for a _Voting Candidate_; otherwise this is the candidate we will push in the [Modelica Association](https://modelica.org/) for public release approval.

## Versioning scheme{id="Versioning-scheme"}

All artefacts released by MAP eFMI -- e.g., the eFMI specification text, XML Schema Definitions for container manifests, example eFMUs, the [_eFMI Container Manager_](https://github.com/modelica/efmi-containermanager), [_eFMI Compliance Checker_](https://github.com/modelica/efmi-compliancechecker) and [eFMI crosscheck test cases](https://github.com/modelica/efmi-testcases) -- use a certain versioning scheme consisting of three digits of the form `MAJOR.MINOR.PATCH`. In principle the scheme follows [Semantic Versioning 2.0.0](https://semver.org/), with the following additional restrictions:

* All artefacts of a _eFMI Standard_ must have the very same version. This means for example, that the versions of the XML Schema Definitions for eFMI container manifests (the XSD files / software artefacts) are aligned with the version of the eFMI specification text that uses this very definitions.
* If there is ever a need for a new `MINOR` _eFMI Standard_ version (hence a pure bug-fix release of the standard according to the [general release organization](#General-release-organization)), all artefacts and tooling must provide new releases (incorporating any fix as needed of course), increasing their `MINOR` digit respectively. I.e., the `MINOR` digit denotes consecutive bug-fix releases of the _eFMI Standard_ and the tooling for it.
* The `PATCH` digit is only used by artefacts and tooling for some _eFMI Standard_, but never _eFMI Standards_ (their `PATCH` digit always is 0). This means, that pure tooling bug-fix releases, for the very same _eFMI Standard_ version, is denoted by increasing `PATCH` digits of the version of the respective tooling.

**Example:** _A eFMI Container Manager 1.1.3 release is the third release of the tool for the eFMI Standard 1.1.0, which was a bug-fix release for the eFMI Standard 1.0.0, whereas a eFMI Container Manager 2.0.0 release is the first tooling release for a completely new major eFMI Standard release._

We like to stress that `MINOR` _eFMI Standard_ version changes are pure bug-fix releases as explained in the [general release organization](#General-release-organization)! This means, no new features are added in such. For that reason it is valid to just talk about, e.g., _eFMI 1_ vs. _eFMI 2_ etc when denoting the features and general tooling of some eFMI technology space.

# Backwards compatibility{id="Backwards-compatibility"}

Our target domain -- embedded, safety critical, real time software -- is strict, in fact ridiculous strict, when it comes to documenting, archiving, certifying and sticking to the defined tooling versions throughout the whole development cycle of an embedded project. Changing tooling in the middle of embedded development projects comes with _severe_ requirements on documentation, auditing and certification. In fact, it is not likely to be required because the used tooling is typically extensively tested, or even certified, before being deployed. It is very unlikely that a show-stopper tooling-bug is encountered, which means that one is typically much better of to work around minor tooling-bugs than going through the hassle to document and recertify a tool change.

Considering that the eFMI technology requires a toolchain, we can safely assume that once picked, an embedded software development project sticks with the given _eFMI Standard_ until project end. Hence, we do not have to take care of backwards compatibility from the perspective of the _eFMI Standard_. A standard for embedded development is rather better off by rigorously fixing shortcomings and cleaning up the specification instead of using second quality solutions to also take care of backwards compatibility.

MAP eFMI therefore reserves the right of -- and in fact very likely will introduce -- backwards compatibility breaking _eFMI Standard_ changes from one `MAJOR` version to the next. Embedded developers can switch to new eFMI tooling at the beginning of their next project (which can in fact be to port a released version of an existing project to a newer _eFMI Standard_ as part of its next release -- a task that should not be underestimated).

# Reporting specification issues and new feature requests{id="Reporting-specification-issues-and-new-feature-requests"}

You can report any specification issues you found via the [GitHub issue tracker](https://github.com/modelica/efmi-standard.org/issues). Before opening any new issues, please consult the [contributing and repository policy](https://github.com/modelica/efmi-standard.org/blob/main/CONTRIBUTING.md) first. If you create a new issue, please use the label `eFMI Standard` and denote the troublesome version of the standard first in the issue title, e.g., _"eFMI 1.0.0 Alpha 4: The links in Chapter Foo-Bar are broken"_. Further, use the `bug` label for real specification bugs, the `enhancement` label for general new feature requests and the `question` label for general discussions.
