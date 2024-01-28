# General info

## Python and packages

### Create a virtual environment

In root, create environment
- `python -m venv venv` on Windows or `python3 -m venv venv` on Unix
If errors occure, try to install `pip install virtualenv`

Activate environment
- `venv\Scripts\activate` on Windows or `source venv/bin/activate` on Unix

Deactivate environment
- `deactivate`

Virtual environment is excluded in `.gitignore`

Install required packages to your virutal env
- `pip install -r requirements.txt`

If installing, add the packages to `requirements.txt` by hand or
- `pip freeze > requirements.txt`


### Development

Format code with black
- `black <file_name>`

Prefer functions rather than static variables.
Functions are more readable if they contain docstrings.
