# 🍪 A up-to-date Cookiecutter template for MLOps

---

Inspired by the [cookiecutter-data-science](https://github.com/drivendata/cookiecutter-data-science) template. This
template has been updated to better fit machine learning-based projects and is being used as the core template in
this [MLOps course](https://github.com/SkafteNicki/dtu_mlops).

## Requirements to use the template:

* Python 3.11
* Cookiecutter v2.4.0

## Start a new project

Start by creating a repository either using the Github GUI.
Afterwards on your local machine run

```bash
cookiecutter https://github.com/SkafteNicki/mlops_template
```

and input starting values for the project. When asked for the repository name when creating the template,
input the same name as when you created the repository. Note that when asked for the project name, you should input
a [valid Python package name](https://peps.python.org/pep-0008/#package-and-module-names). This means that the name 
should be all lowercase and only contain letters, numbers and underscores. The project name will be used as the name of 
the Python package. This will automatically be validated by the template.

To commit to the remote repository afterwards execute the following set of commands:

```bash
cd <repo_name>
git init
git add .
git commit -m "init cookiecutter project"
git remote add origin https://github.com/<username>/<repo_name>
git push origin main
```

## GitHub branch protection

It is recommended to protect the `main` branch of the repository.
To do this go to the repository settings, go to "Branches" and click "Add branch protection rule".
Type `main` as the branch name pattern and check the following boxes:
 - "Require a pull request before merging" to force changes to the `main` branch to go through PRs.
   - "Require approvals" this is optional, but can help to ensure that multiple people understand all code. It can also make progress more sluggish.
   - "Dismiss stale pull request approvals when new commits are pushed" if the above is checked, this should also be checked.
   - "Require approval of the most recent reviewable push" to avoid contributors approving their own PRs.
 - "Require status checks to pass before merging" force PR to pass CI before merging.
   - "Require branches to be up to date before merging".
   - Add any status checks you want. With this template we recommend adding `static_checks` as it runs Ruff and avoids non-unix line endings.
 - "Do not allow bypassing the above settings" force admins (like yourself) to also follow the rules.

## The stack

🐍 Python projects using `pyproject.toml` <img src="icons/python.svg" width="20" height="20">

🔥 Models in `pytorch` <img src="icons/pytorch.svg" width="20" height="20">

📦 Containerized using `docker` <img src="icons/docker.svg" width="20" height="20">

📄 Documentation in `mkdocs` <img src="icons/markdown.svg" width="20" height="20">

👕 Linting and formatting with `ruff` <img src="icons/ruff.svg" width="20" height="20">

✅ Checking using `pre-commit` <img src="icons/precommit.svg" width="20" height="20">

🛠️ CI with `Github actions` <img src="icons/githubactions.svg" width="20" height="20">
