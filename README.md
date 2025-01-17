# Git Commands Notes

This document provides notes on various Git commands, organized by scenarios encountered during past project development. It includes a subset of Git commands relevant to these scenarios, along with instructions for setting up and deploying documentation using MkDocs.

## Table of Contents

- [Git Commands Notes](#git-commands-notes)
  - [Table of Contents](#table-of-contents)
  - [Content Organization](#content-organization)
  - [Project and Deployment](#project-and-deployment)
    - [Installing MkDocs](#installing-mkdocs)
    - [Creating an MkDocs Project](#creating-an-mkdocs-project)
    - [Viewing Documentation Locally](#viewing-documentation-locally)
    - [Deploying to GitHub Pages](#deploying-to-github-pages)

## Content Organization

This document introduces git commands based on scenarios encountered during past project development, rather than by command functionality. Relevant commands are still summarized in the document and provided as links. 

Only a subset of git commands is provided in the summary table, based on the scenarios.

## Project and Deployment

This project uses MkDocs for documentation, so Python must be installed. The process is as follows:

### Installing MkDocs

If you have pip (package installer for Python) installed, you can run the following command to install MkDocs:

```bash
pip install mkdocs
```

### Creating an MkDocs Project

Once MkDocs is installed, you can use the `mkdocs` command to create a project, start a web server, and build the documentation site. The relevant MkDocs commands are as follows:

- `mkdocs new [dir-name]` - Create a new project
- `mkdocs serve` - Start a live-reloading documentation server
- `mkdocs build` - Build the documentation site
- `mkdocs -h` - Show help message

The following command was used to create this project:

```bash
mkdocs new .
```

### Viewing Documentation Locally

You can view the generated documentation locally by running the following command:

```bash
mkdocs serve
```

### Deploying to GitHub Pages

MkDocs provides a simple command to deploy your documentation to the `gh-pages` branch. Once you push the changes, you can see the deployment result on GitHub Pages.

```bash
mkdocs gh-deploy
```

After running `mkdocs gh-deploy`, you do not need to manually execute `git push` because this command automatically performs the following actions:

- Generates static site files: MkDocs will generate the static site content based on the `docs` directory and `mkdocs.yml` configuration file.
- Creates or updates the `gh-pages` branch: `mkdocs gh-deploy` will automatically switch to the `gh-pages` branch and place the static files in that branch.
- Automatically pushes to the remote repository: It will push the updated `gh-pages` branch to GitHub.
