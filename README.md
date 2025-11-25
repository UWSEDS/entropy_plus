![](https://github.com/UWSEDS/entropy_plus/actions/workflows/testsuite.yaml/badge.svg?branch=main)

# entropy_plus
An example for continuous integration

This is based on the [entropy](https://github.com/UWSEDS/entropy) example, but it adds continuous integration.

We are using GitHub actions for our continuous integration. GitHub actions looks
for workflow files, which are yaml files that specify what to run on the GitHub
action runner. The workflow files **must** be placed in the `.github/workflows/`
folder and must have a `.yaml` or `.yml` extension for GitHub actions to find them.

In our action, we first set up our conda environment using the `environment.yaml`
file in our repo and then call `pytest` to run our tests. We also use the pytest-cov
plugin to report our test coverage.

Note:
GitHub actions are disabled by default on forks.