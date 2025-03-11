# Documentation for `cortex` 🧠
This repo contains a `jupyter-book` with documentation for [`cortex`](https://github.com/prescient-design/cortex).

### Building the documentation
Create a virtual environment with `uv` or a conda environment with `mamba`. Install requirements with
```bash
uv pip install -r requirements.in
``` 

or from `requirements.in` and run `publish.sh`.

To render notebook output, install [`cortex`](https://github.com/prescient-design/cortex).

To build and view the docs locally
```bash
jupyter-book build docs
open docs/_build/html/index.html
```

and when changes are ready, publish with
```bash
ghp-import -n -p -f docs/_build/html
```

### Writing docs
Protip: load the part of the `cortex` codebase that you're writing docs for into LLM project context and prompt to generate markdown and .py files. Then use `jupytext` to convert from code to executable ipynb.
```bash
jupytext --to notebook myfile.py
```
In VSCode, select the .venv as the kernel.

### Acknowledgements
Thanks to [Miguel González Duque](https://github.com/miguelgondu) and the `poli` [documentation](https://machinelearninglifescience.github.io/poli-docs/) for inspiration!