# Substance IO

A minimal publishing solution based on Pandoc Markdown and Substance.

## Installation

### Prerequisites

- Node.js >=0.10.x
- Pandoc >= 1.12.02 (for Markdown cross-compiling)

### Install

Substance.IO comes as a ready-to-use NPM module:

    $ sudo npm install -g substance-io


### Development Environment

For development we use a setup based on our Screwdriver command line utility. It's just a little helper that makes dealing with our many modules easier.

    $ git clone https://github.com/substance/screwdriver.git
    $ cd screwdriver
    $ sudo python setup.py install

Clone the io repo.

    $ git clone https://github.com/substance/io.git

Run the update command, which pulls in all the sub-modules and dependencies.

    $ cd io
    $ substance --update

Finally start the server and point your browser to `http://localhost:5000`.

    $ substance <path-to-library-folder>


## Managing collections and documents

Documents are managed by convention in a directory structure having folders for collections
and subfolders for documents. For example:

    mylibrary/substance                    # collection folder
    mylibrary/substance/index.json         # collection metadata
    mylibrary/substance/about              # document folder
    mylibrary/substance/about/index.json   # document metadata
    mylibrary/substance/about/content.md   # source markdown


This would define a library with one collection with id `substance` having one document with id `about`.
