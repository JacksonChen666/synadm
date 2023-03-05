<!-- TODO: find the keyword TODO through out the document, and resolve that -->
# Contributing guidelines and guide

Thanks for your consideration <!-- TODO: replace word as it doesn't sound right
--> to contribute to the synadm project! This document aims to be a contribution
guidelines document, while also guiding those who need more help. <!-- TODO:
reword since i kinda don't like the wording with "need more help" -->

Table of Contents:
- TODO
- TODO
- TODO
- TODO
- TODO
- TODOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOO

# Guidelines

TODO

- A dedicated issue is not required for any Pull Request.
- Code should be formatted according to [PEP8][] (check with [flake8])
- The length of a line for code is maximum 79 characters.

[PEP8]:TODO

# Ways to contribute to synadm

Even if you're not do not have the technical knowledge, you can still help
contributing to the `synadm` project. We still accept technical contributions
(code, etc.).

## Non-technical contribution suggestions

- Help improving the documentation: The documentation could be sometimes be in
  rough shape, in need of corrections on spelling, wording, grammar, etc.
- TODO: implementation status checks updates

## Technical contribution suggestions

- Implement a [synapse admin API](TODO) endpoint missing in `synadm`
- Review the [open issues](TODO) and considering open a Pull Request for it if
  there isn't one already for the issue

# Technical things to be aware about

The `synadm` project uses the python `Click` library for it's command line
interface. TODO: expand

# Setup your development environment

TODO

- Click the fork button on the [JOJ0/synadm](TODO) repository
- Run the following commands:
  ```
  git clone git@github.com:TODO/synadm TODOTODOTODOTODOTODOTODOTODO
  cd synadm TODO
  python3 -m venv env
  source env/bin/activate TODO: other shells, reactivation, deactivation, pointer to docs?
  pip3 install -e .
  pip3 install flake8 TODO: make that dev dependency? TODO: document that requirement
  ```

# Maintainers' guidelines

TODO

- In case the `dev` branch is being used as part of a PR, the dev branch should
  not be touch except for things related to that PR.
- Branches do not have to be created in the maintainer's fork and should <!--
  TODO: discuss clarification --> be created on the main repository
- TODO: PR owners or something
 
## Release process

TODO

## For contributors interested in collaborating

TODO
