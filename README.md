# DDS team manual

Team manual for the Defence Digital Service (DDS) in the UK Ministry of Defence.

# Making changes to the manual

## Pre-requisites

This manual uses a documentation and static site generator called [docnado](https://heinventions.github.io/docnado-site/example-site/w/home.html). To get started, you need to have installed: 

- Python 3

You may wish to have a virtual environment setup for the rest. To do so, run:

`python3 -m venv <virtual-environment-name>`

Then, activate the environment, using:

`source <virtual-environment-name>/bin/activate`

Finally, install all of the requirements for this project, by running:

`pip install -r requirements.txt`

## Using Docnado to make changes

Docnado uses standard markdown. 

For general reference, please visit the [Docnado docs](https://heinventions.github.io/docnado-site/example-site/w/documents/callouts.html) website. This includes some nice extra style options, like [how to add "info" text](https://heinventions.github.io/docnado-site/example-site/w/documents/callouts.html).

### Editing a page

Just edit the relevant `.md` file.

### Adding a page

All pages must live in the `docs` folder and must be a `.md` file-type. All you have to do, therefore, is add a `<filename>.md` file to the relevant sub-directory of `docs` to add a page.

For formatting and navigation-listing purposes, you'll also need to include some metadata at the top of the `.md` file. You can copy and paste this as a minimum:

```
title:      <page title - this appears at the top of the page in big letters>
desc:       <a short description of the page. This appears beneath the title at the top of the page>
date:       <yyyy/mm/dd format - the date on which you made the change you're making>
version:    <0.1.0 for example. Please use semantic versioning>
template:   document
nav:        Directory > Subdirectory > Page name [the directory and page name should be as you want it to appear in the sidebar]
percent:    100
authors:    team@digital.mod.uk
```

### Adding a directory

To add a directory, just `mkdir` within the `docs` directory. However, this will not automatically appear in the sidebar. To do this, you must refer to the subdirectory in the `nav` metadata tag, as above.

### Previewing a change locally

To preview a change, ensure your local virtual environment is activated, then just run `docnado`. This will run a local server on localhost:5000, which you can visit in your browser.

### Deploying a change

Changes will be continuously deployed, so you don't need to do anything apart from raising a PR. 
