# rshanhluf16.github.io
## About

This repository contains my Quarto website for DSCI 521. The site includes computational blog posts written in both Python and R, with reproducible environments managed using `uv` and `renv`.

## Prerequisites

To build this website locally, you need:

- Quarto
- Python 3.14
- uv
- R 4.6.1
## Build Instructions

Clone the repository and move into the project directory:

```bash
git clone https://github.com/rshanhluf16/rshanhluf16.github.io.git
cd rshanhluf16.github.io
```

Restore the Python environment from the committed `uv.lock` file:

```bash
uv sync
```

Restore the R environment from the committed `renv.lock` file:

```bash
R -e 'renv::restore()'
```

Render the complete Quarto website:

```bash
uv run quarto render
```
## Viewing the Website

The rendered website is written to the `docs/` directory.

To preview the website locally, run:

```bash
uv run quarto preview
```

The published website is available at:

https://rshanhluf16.github.io

## Data Sources

The Python computational post uses the Iris dataset provided by scikit-learn:

https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_iris.html

The R computational post uses the built-in `mtcars` dataset from R:

https://stat.ethz.ch/R-manual/R-devel/library/datasets/html/mtcars.html

Both datasets are available through the installed software/packages, so the computational posts do not require downloading separate data files during rendering.