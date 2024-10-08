# Contributing and repository policy

This project welcomes contributions and suggestions. Please follow the guidelines below before opening new issues or pull requests.

## Contributor license agreement

Any pull requests or commits require you to agree to The _Modelica Association Contributor License Agreement_ (MA CLA) declaring that you have the right to, and actually do, grant us the rights to use your contribution. For details, visit https://github.com/modelica/ModelicaAssociationCLA.

When you submit a pull request, a bot will automatically determine whether you need to provide a MA CLA and decorate the pull request appropriately (e.g., status check, comment). Simply follow the instructions provided by the bot. You will only need to do this once.

## Reporting issues

Please check the available labels and use them. The label descriptions clarify the kind of issues that can be reported. _Every_ issue must be labeled with _one_ collated-to category label (`website`, `eFMI Standard`, `infrastructure`) denoting the artifacts and/or functionality of the repository the issue is about. The issue also _must_ be categorized if it is a general question, enhancement request or an actual bug (`question`, `enhancement` and `bug` labels). The `documentation` label is optional and used to denote that the issue is about the documentation of its collated-to category. The `invalid` label is used to denote issues that already exists, doesn't seem right or won't be worked on.

The `eFMI Standard` label is used to denote issues of publically released stable and candidate-draft _eFMI Standard_ versions. It can be used by the public -- i.e., individuals and organizations that are not part of the [Modelica Association Project eFMI](https://www.efmi-standard.org/about/) -- to report issues or feature requests they found in publicly released _eFMI Standard_ versions. If you report any standard issues, please denote the troublesome version of the standard first in the issue title, e.g., _"eFMI Standard 1.0.0 Alpha 4: The links in Chapter Foo-Bar are broken"_. And don't forget to add a categorization as explained in the previous paragraph (`bug`, `ehancement` or `question` label). We will provide feedback if we consider your issue worthwhile and tranferred it to the non-public _eFMI Standard_ development repository or not.

## Branch protection and commits/pull requests

The main branch (`main`) of the repository is protected. All work must be done on separate branches, with pull requests to merge your new contributions into `main`. Respective pull requests must be reviewed by at least one code owner of the changed artifacts. Please cf. the `CODEOWNERS` file for who to add as reviewer to your pull request.
