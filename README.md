# eniak_de

## Installation

- run `sphinx-quickstart` - say yes here:
```
You have two options for placing the build directory for Sphinx output.
Either, you use a directory "_build" within the root path, or you separate
"source" and "build" directories within the root path.
> Separate source and build directories (y/n) [n]: 

```

- delete make.bat - we do not work with windows
- config git with `git config pull.rebase true`
- install https://sphinx-rtd-theme.readthedocs.io/en/latest/
- install https://myst-nb.readthedocs.io/en/latest/
  - add it to extensions
  - turn off notebook building: `jupyter_execute_notebooks = "off"`
- turn off `prev_next_buttons`
```
html_theme_options = {
    "prev_next_buttons_location": None,
}
```
