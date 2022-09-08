[![AWS 3.6 Build](https://github.com/pbenmoser4/github-actions-demo/actions/workflows/aws.yml/badge.svg)](https://github.com/pbenmoser4/github-actions-demo/actions/workflows/aws.yml)

# Overview
This is a fork from Noah Gift's [github actions demo](https://github.com/noahgift/github-actions-demo). 
# Getting Started
Before you do anything, you should create a virtual environment in your favorite cloud shell. From anywhere, create a `virtualenv` by executing

```python3 -m venv ~/.{your-env-name}```

and then activating that virtual environment by executing

```source ~/.{your-env-name}/bin/activate```

After executing the above code, your shell should add your environment name to the beginning of each command line.

# Forking and Cloning Locally
To run this code in your own cloud development environment, first fork the repo, and then clone it into your cloud shell. You may need to establish an auth handshake with github before doing this, if you haven't already.

To clone the repo in your cloud shell, run

```git clone https://github.com/pbenmoser4/github-actions-demo.git```

# Installing Dependencies and Testing Locally in the Cloud

To install dependencies, lint the code, and test it, run `make all` from the top-level `github-actions-demo` repository.

# Running Github Actions

There are already Github Actions files in this repository, but that doesn't mean that Github Actions is enabled in your forked repo. To get them up and running, click on the `Actions` button in your repo's top navigation bar, next to `Code` and `Pull Requests`. Github should notify you that there are actions files that aren't currently running. Tell Github that you know what you're doing, and to enable the actions files.

To get an idea of what's going on in the action files, navigate to [~/github-actions-demo/.github/workflows](https://github.com/pbenmoser4/github-actions-demo/tree/main/.github/workflows). Checking out `main.yml` will give you a general idea of what's going on, namely, when github senses a new `push` action on your repository, it will 1) set up Python 2) install dependencies using `make install` 3) lint the code using `make lint` and 4) test the code using `make test`, each action of which is defined in the `Makefile`. 

Now, every time you push new code to this repository, Github Actions will setup the code, install dependencies, lint it, and test it, so you can be sure that everything is running correctly!
