# Installation

* Remove old venv if any: `rm -rf venv`
* Create virtual environment: `python3 -m venv venv`
* Activate virtual environment: `source venv/bin/activate`
* Check pip version: `pip --version`
* Install MkDocs: `pip install mkdocs-material`
* Create a new project: `mkdocs new [dir-name]`

# Testing your MkDocs web site locally

* `source venv/bin/activate` - Activate virtual env
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.