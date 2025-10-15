# Jupyter-Python Template


## Setup


### UV Installation

Install UV through any of the methods described in the
[official documentation][UV Installation Documentation].


### VSCode Extensions

Install the recommended VSCode extensions of this repository (they appear in
recommendations when opening up the extensions menu on the left sidebar).


### UV Setup

Execute the following command: `uv sync`, to download all the necessary
dependencies to execute the project and recompile the modules.


### Kernel Selection

When opening a Jupyter notebook, select the "Python Environments" option and
select the one that belongs to this workspace.


## Coding

First of all, create a new folder under `src/`, there can go either Jupyter
notebooks or Python packages.


### Python


#### Packages

To write a Python package, inside the newly made folder create a `__init__.py`
file as its entrypoint.


#### Modules

As many `.py` files as needed can be created under the newly made folder. They
can be imported from the `__init__.py` file to belong to the package.


## Jupyter Notebooks


### Creation

Jupyter notebooks can directly be added under the newly made folder. It is
recommended to keep only one notebook per folder.


### Importing Modules

Modules located on the same folder can be directly imported with
`import module`, and packages from anywhere in the workspace can be imported
after an `uv sync` with `import package`.


## Modifications


### Project


#### Scripts

To add a script to the project, add a script name and a path to a function in
the `[project.scripts]` table from the `pyproject.toml` file and a launch task
written in the `.vscode/launch.json` launch configuration. The script name
should be in kebab-case, whereas all the rest should be in snake_case.


#### Name and Description

To modify the description of the project, change the value of the
`[project.name]` and the `[project.description]` keys in the `pyproject.toml`
file, respectively.


#### Author/s

To modify the author of the project, change the value of the `[project.authors]`
key in the `pyproject.toml` file.


### Python Linting-Formatting

The Python linter-formatter used is Ruff, and can be configured in the
`ruff.toml` file (excluded out of view but existing in the folder) or the
`pyproject.toml` file, as explained in the
[official documentation][Ruff Settings Documentation]. In any case, if any
[rules or set of rules][Ruff Rules Documentation] are to be disabled, they can
be added to the ignore array.



[Ruff Rules Documentation]: https://docs.astral.sh/ruff/rules/
[Ruff Settings Documentation]: https://docs.astral.sh/ruff/settings/
[UV Installation Documentation]: https://docs.astral.sh/uv/getting-started/installation/
