# InvenTree.github.io

This repository hosts the user documentation for [InvenTree](https://github.com/inventree/inventree), an open source inventory management system. 

To serve this documentation locally (e.g. for development), you will need to have Python 3 installed on your system.

## Setup

Run the following commands from the top-level project directory:

```
$ git clone -b mkdocs_material git@github.com:eeintech/InvenTree.github.io.git
$ cd InvenTree.github.io/
$ python3 -m venv env-inv-doc
$ source env-inv-doc/bin/activate
$ pip install -r requirements.txt
```

## Serve Locally

To serve the pages locally, run the command (from the top-level project directory)

```
$ mkdocs serve
``` 

## Edit Documentation Files

Once the server is running, it will monitor the documentation files for any changes, and update the served pages.

## Credits

This documentation makes use of the [mkdocs-material template](https://github.com/squidfunk/mkdocs-material)
