# General info

## GIT
### Using feature branches:
Feature branches are very useful when collaborating.<br>Creating a separate branch from the _main_ branch allows multiple people to work on the project simultaniously. Changes are pushed to that feature branch and reviewed by others.<br>When changes are merged into the _main_ branch, other collaborators can _rebase_ their own local branch with those changes.
### Creating a feature branch
Terminal in main branch:<br>
Get the latest Main.
- `git pull`
- `git checkout -b "branch_name"` Feature branches are often named as `"feature/feature-name-here"`
Add changes and commit:
- `git add .` "." adds all modified files
- `git commit -m "commit message here"`
Push changes to remote feature branch:
- `git push -u origin HEAD` This sets upstream to the remote in the same process (HEAD is current branch)
After merging the feature branch you can leave the branch by:
- `git checkout main`

### Rebasing
When main has changed during development:
Commit or stash changes, exit to main with `git checkout main`<br>
Pull changes and rebase to your branch with following commands:<br>
`git pull`, `git checkout your-feature-branch`, `git rebase main`<br>
Resolve conflicts and continue with `git rebase --continue`

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
