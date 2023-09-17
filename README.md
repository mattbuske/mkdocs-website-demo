# This is the source code for my website.
This project is versioned in a git repository, hosted on github, and I utilize Gitkraken as my GitUI. I also utilize github actions to incorporate CI/CD and to ease the process of delivery of my web content. The site [demo.mattbuske.com](https://demo.mattbuske.com) is pointed to an Azure Static Website where the compiled site is launched. The github repository is public.

## Tech Stack
I use a few different technologies to deploy this project:
- Windows 10 for OS
- Python (3.11) + MkDocs and Extensions (dependencies are in the requirements.txt file) for building the site
- VSCode for local development
- Git for versioning
- Gitkraken for git management
- Github for repository management
- Github actions for CI/CD
- Azure Static Websites (free) to host the final product

## Local Development
VSCode within a virtual python environment utilizing the following packages: 
- mkdocs==1.5.2
- mkdocs-material==9.3.1 
- mkdocs-material-extensions==1.1.1

These are pinned dependencies in a 'requirements.txt' file in the root of the project. The mkdocs.yml configuration file also resides in the root along with the standard 'docs' folder containing the markdown documents.

Development is performed via the `mkdocs serve` command and viewing it in a browser.

### Quick Start
*This assumes a Windows 10 Development environment!*
After cloning the repository (make sure to initialize all submodules!), run the following in VSCode via the powershell interface:

#### Create a python virtual environment
This will ensure a clean environment and no conflicts. The git repo also ignores the .venv folder and everything in it.
```POWERSHELL
py -m venv .venv
```

#### Activate the python virtual environment
```POWERSHELL
.venv/Scripts/activate.ps1
```

#### Upgrade pip
```POWERSHELL
py -m pip install --upgrade pip
```

#### Install Dependencies
```POWERSHELL
py -m pip install -r requirements.txt
```

#### Run MkDocs
```POWERSHELL
py -m mkdocs serve
```