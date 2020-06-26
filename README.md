# CookieCutter Python Package Template

A [cookiecutter](https://cookiecutter.readthedocs.io/en/1.7.2/README.html) template for Python packages.

## Requirements
- Cookiecutter
- Setuptools

```
pip install setuptools cookiecutter
```
---

## Usage

1. #### Generate Your Package
   ```
   cookiecutter gh:nogoodusername/cookiecutter-pypackage-template
   ```

   You will asked to fill in below details:

   `author_name`: Main Author of the library (Used in setup.py, LICENSE, README.md)   
   `author_email`: Contact email of the author (Used in setup.py, LICENSE, README.md)      
   `package_name`: Name of the python package. Please only enter [a qualified python package name](https://www.python.org/dev/peps/pep-0008/#package-and-module-names). (Used in setup.py, README.md)   
   `package_version`: Release version (Used in setup.cfg)   
   `package_description`: One line description of the library (Used in README and setup.py)   
   `package_url`: Git Repo URL of the library.   

2. #### Add a Git Repo
   Create a new repo for `package_name` in Github or your preferred Git repository hosting site. 

   You will find a folder named [`package_name`]. Move into the folder, and setup your git repo there.

   ```
   cd [package_name]
   git init .
   git add .
   git commit -m "Initial commit"
   git remote add origin git@[your-package-repo]
   git push -u origin master
   ```

3. #### Install Dev Requirements
   Install Dev Requirements using `pip`

   ```
    pip install -r requirements_dev.txt
   ```

4. #### Add your package code and start developing
   You are good to go, you can add your to the package and start developing.
---

## Releasing The Package

### Version Management
This template uses [bump2version](https://github.com/c4urself/bump2version)- Pre-configured version bumping with a single command

Please read [Semantic Versioning 2.0.0](http://semver.org/) before bumping versions.


### Changelog
Changelogs are maintained using [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) format.

### Publishing the package
This template does not include a publish mechanism. Implement your own publishing mechanism and update the Makefile:deploy function.
