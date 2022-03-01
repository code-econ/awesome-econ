# Awesome Econ [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

Curated list of links related to coding in economics. We will try to list links to class content, notebooks, replication codes, libraries and data sources. We are just starting this so bare with us and please send us suggestions!

## Coding Resources

  - [RISE](https://rise.readthedocs.io) Jupyter slideshow extension
  - [Google Collab](https://colab.research.google.com/) online Jupyter notebooks with GPU support
  - [Atom](https://atom.io/) text editor
    - Interactive coding with [hydrogen](https://atom.io/packages/hydrogen)
    - Julia support with [IJulia](https://github.com/JuliaLang/IJulia.jl) and [language-julia](https://atom.io/packages/language-julia)
    - R support with [IRkernel](https://irkernel.github.io/installation/) and [language-r](https://atom.io/packages/language-r)
  - [VS code](https://code.visualstudio.com/) open source text editor by Microsoft.
    - I find that using the notebook in the browser is better than the notebook inside VScode

## Maintaining environments

This is the first required piece. The following resources help with portability of your code. 

 - [conda](https://docs.conda.io/en/latest/) is a the goto package manager for data-science. It supports all platform, and provides binaries so you don't need tool chains installed. It also doesn't require admin right on the machine. It supports all languages like julia, R, go, rust and of course python
  - [conda-build](https://docs.conda.io/projects/conda-build/en/latest/) allows to port a conda environment prepared on one machine to another.   
  - [mamba](https://github.com/mamba-org/mamba) is a drop-in replacement for conda that is faster.
- [Nix](https://nixos.org/download.html) is a manage it all manager. It requires admin rights.

Container approach: think of these as thin virtual machine. This is the easier to port as long as the host machine has the ability to run containers. 

- [docker](https://www.docker.com/) is an industry standard for portable code. 
- [singularity](https://sylabs.io/singularity) is probably where academia will converge. 

Some language specific package and environment managers:

 - [julia](https://pkgdocs.julialang.org/v1.2/environments/) natively supports environment. It's really great. It can be hard however to relocate an environment.
 - [pdm](https://pdm.fming.dev/) is a recent python enivronment manager, compared to the king of the gender `npm`
 - [peotry](https://python-poetry.org/) is a very friendly python environment manager. Makes is easy to upload package to pip

## DataFrames

 - Julia
   - [DataFrames.jl](https://github.com/JuliaData/DataFrames.jl) main pacakge to handle dataframes in Julia
   - [DataFramesMeta.jl](https://github.com/JuliaData/DataFramesMeta.jl) handy additional functions
   - [Chain.jl](https://github.com/jkrumbiegel/Chain.jl) piping, recommmned to use with the above
- Python
  - [Pandas](https://pandas.pydata.org/) de facto dataframe for python
  - [Method chaining](https://towardsdatascience.com/using-pandas-method-chaining-to-improve-code-readability-d8517c5626ac#:~:text=Method%20chaining%20is%20a%20programmatic,variables%20at%20each%20intermediate%20step.) to improve readability
  - [Modin](https://modin.readthedocs.io/en/latest/) dropin replacement for large datasets
 - R
   - [data.table](https://cran.r-project.org/web/packages/data.table/vignettes/datatable-intro.html) fast dataframe for R

## Deep Learning & auto-diff programming

- Pytorch
  - [Installation](https://pytorch.org/get-started/locally/) with or without GPU support
  - [Quickstart](https://pytorch.org/tutorials/beginner/basics/intro.html) to learn the basics
- [JAX](https://github.com/google/jax)
- Keras
  - Getting started in [Python](https://keras.io/getting_started/intro_to_keras_for_researchers/) and [R](https://tensorflow.rstudio.com/installation/)
- [Flux.l](https://fluxml.ai/Flux.jl/stable/) in julia

## Machine Learning

 - [scikit-learn](https://scikit-learn.org/stable/) in Python
 - [mlr3](https://mlr3.mlr-org.com/) in R

## Probabilistic programing

 - [Pyro](https://pyro.ai/) for python
 - [Turing.jl](https://turing.ml/stable/) for julia

## Academic Websites

- [GitHub Pages](https://pages.github.com/) to host a private website
- [Jekyll](https://jekyllrb.com/) for building pages from HTML/CSS

## Slides in html
 
- [reveal.js](https://revealjs.com/) is the most mature but also older. 
- [mdx-deck](https://github.com/jxnblk/mdx-deck) based on react and MDX (markdown)
- [spectacle](https://formidable.com/open-source/spectacle/) also react
- [slidev](https://github.com/slidevjs/slidev) is based on vue.js and vite.js. This is the best html framework to write academic presentation. It supporst math, annotations, code highlights and the list goes on and on. Because it is built on vite, the slides get updated almost instantly whenever you change the source. It's amazing!

## Pipelines

 - [Make](https://www.gnu.org/software/make/manual/make.html), the classic
 - [nextflow](https://www.nextflow.io/) 
 - [doit](https://pydoit.org/) 
 - [snakemake](https://snakemake.readthedocs.io/en/stable/) 
 - [luigi](https://github.com/spotify/luigi), [airflow](https://airflow.apache.org/) and [prefect](https://www.prefect.io/) are great but not clearly adapted to scientific work

## Rerpoducibility, versioning and provenance

 - [Verdant](https://marybethkery.com/Verdant/) keeps a history of all changes to a notebook
 - [nbdime](https://nbdime.readthedocs.io/en/latest/) nicely compare versions of a notebook
 - [dvc](https://dvc.org/) versioning for large files and more, inside git

## Notebooks

 - [Jupytext](https://github.com/mwouts/jupytext) seamless sync between text based files and notebook format (json)
