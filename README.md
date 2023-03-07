# Repository overview

This repository contains the sources of the [efmi-standard.org website](https://efmi-standard.org) and is the central location for feature requests, suggestions and bug reports.

The issue tracker of the repository is also used by the public (i.e., not MAP eFMI members) to report any issue of _eFMI Standard_ releases they found. Please consult the [contributing guidelines](CONTRIBUTING.md) and [overview of the _eFMI Standard_](https://efmi-standard.org/standard/) before reporting any issues.

## Building the website locally

The [efmi-standard.org website](https://efmi-standard.org) is build using the [HUGO framework](https://gohugo.io/), an open-source static website generator. To build it locally:

 1. Clone the [website's git repository](https://github.com/modelica/efmi-standard.org).
 2. Initialize and update all git submodules via `git submodule update --init --recursive` from the repository root.
 3. Install the [HUGO extended version](https://gohugo.io/installation/) for your platform. In the following steps we assume Microsoft Windows, but the concpets are likewise for other platforms.
 4. Make sure that _HUGO_ is available from your command line (e.g., adding it to your path as required).
 5. Switch to the website repository as current working directory.
 6. You can now build and provide the website locally via `hugo serve`. Read the command line output; it provides you the address from which the local build is available. Typically it is something like `http://localhost:1313/`. Load that address in your browser. You can edit the site live; _HUGO_ will automatically detect changes and rebuild.

## Contributing, security and repository policies

Please consult the [contributing guidelines](CONTRIBUTING.md) for details on how to report issues and contribute to the repository.

For security issues, please consult the [security guidelines](SECURITY.md).

General MAP eFMI repository setup and configuration policies are summarized in the [MAP eFMI repository policies](https://github.com/modelica/efmi-organization/wiki/Repositories#public-repository-policies) (only relevant for repository administrators and therefor private webpage).