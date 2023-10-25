[![Project generated with PyScaffold](https://img.shields.io/badge/-PyScaffold-005CA0?logo=pyscaffold)](https://pyscaffold.org/)
<!-- These are examples of badges you might also want to add to your README. Update the URLs accordingly.
[![Built Status](https://api.cirrus-ci.com/github/<USER>/deep-learn-tutorial.svg?branch=main)](https://cirrus-ci.com/github/<USER>/deep-learn-tutorial)
[![ReadTheDocs](https://readthedocs.org/projects/deep-learn-tutorial/badge/?version=latest)](https://deep-learn-tutorial.readthedocs.io/en/stable/)
[![Coveralls](https://img.shields.io/coveralls/github/<USER>/deep-learn-tutorial/main.svg)](https://coveralls.io/r/<USER>/deep-learn-tutorial)
[![PyPI-Server](https://img.shields.io/pypi/v/deep-learn-tutorial.svg)](https://pypi.org/project/deep-learn-tutorial/)
[![Conda-Forge](https://img.shields.io/conda/vn/conda-forge/deep-learn-tutorial.svg)](https://anaconda.org/conda-forge/deep-learn-tutorial)
[![Monthly Downloads](https://pepy.tech/badge/deep-learn-tutorial/month)](https://pepy.tech/project/deep-learn-tutorial)
[![Twitter](https://img.shields.io/twitter/url/http/shields.io.svg?style=social&label=Twitter)](https://twitter.com/deep-learn-tutorial)
-->

# deep-learn-tutorial

> Quick tutorial on deep learning for Introduction to Data Science

A longer description of your project goes here...

## Installation

In order to set up the necessary environment:

1. create a local environment stored in `.env` with the help of [conda]:
   ```
   conda config --set channel_priority strict
   ```
   ```
   conda env create -f environment.lock.yml -p ./.env
   ```

   > Note: the following command assumes you left channel_priority as its default
   ```
   conda config --set channel_priority flexible
   ```
2. activate the new environment with:
   ```
   conda activate -p ./.env
   ```

Then take a look in the `notebooks` folders.

## Dependency Management & Reproducibility

> Note: I left this here for students to see how to properly utilize [conda], but it is not necessary for the tutorial.

1. Always keep your abstract (unpinned) dependencies updated in `environment.yml` and eventually in `setup.cfg` if you want to ship and install your package via `pip` later on.
2. Create concrete dependencies as `environment.lock.yml` for the exact reproduction of your
   environment with:
   ```bash
   conda env export -p ./.env -f environment.lock.yml
   ```
   For multi-OS development, consider using `--no-builds` during the export.
3. Update your current environment with respect to a new `environment.lock.yml` using:
   ```bash
   conda env update -p ./.env -f environment.lock.yml --prune
   ```
## Project Organization

```
├── LICENSE.txt             <- License as chosen on the command-line.
├── README.md               <- The top-level README for developers.
├── configs                 <- Directory for configurations of model & application.
├── data
│   ├── external            <- Data from third party sources.
│   ├── interim             <- Intermediate data that has been transformed.
│   ├── processed           <- The final, canonical data sets for modeling.
│   └── raw                 <- The original, immutable data dump.
├── environment.yml         <- The conda environment file for reproducibility.
├── environment.lock.yml    <- The _pinned_ conda environment file for emergencies.
├── models                  <- Trained and serialized models, model predictions,
│                              or model summaries.
├── notebooks               <- Jupyter notebooks. Naming convention is a number (for
│                              ordering), the creator's initials and a description,
│                              e.g. `1.0-fw-initial-data-exploration`.
├── pyproject.toml          <- Build configuration. Don't change! Use `pip install -e .`
│                              to install for development.
├── references              <- Data dictionaries, manuals, and all other materials.
├── reports                 <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures             <- Generated plots and figures for reports.
├── setup.cfg               <- Declarative configuration of your project.
└── src
    └── deep_learn_tutorial <- Actual Python package where the main functionality goes.
```

<!-- pyscaffold-notes -->

## Note

This project has been set up using [PyScaffold] 4.5 and the [dsproject extension] 0.7.2.

[conda]: https://docs.conda.io/
[pre-commit]: https://pre-commit.com/
[Jupyter]: https://jupyter.org/
[nbstripout]: https://github.com/kynan/nbstripout
[Google style]: http://google.github.io/styleguide/pyguide.html#38-comments-and-docstrings
[PyScaffold]: https://pyscaffold.org/
[dsproject extension]: https://github.com/pyscaffold/pyscaffoldext-dsproject
