# Welcome to Allfeat Documentation! 🚀

This README will explain how to build and start the documentation on a server. It does not elaborate on how to open ports for hosting.

The documentation is build using MkDocs, which turns .md files into HTML/CSS, and then builds and hosts it locally.

The actual documentation is located under `/docs`. After building, a build folder will appear, containing HTML and CSS information. Make sure to add it to your `.gitignore` (or to delete it before pushing)

## Getting Started 🚀

Ready to explore Allfeat's possibilities? Follow the steps below to get started:

### Install Allfeat and MkDocs

First, ensure you have the necessary tools.

#### Prerequisites

You'll need `pip` to install MkDocs and Allfeat.

```bash
# for apt
sudo apt install python3-pip
```

```bash
# for pacman
sudo pacman -S python-pip
```

For more information on installation and alternative package managers, refer to the [MkDocs documentation](https://www.mkdocs.org/getting-started/) or [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

#### Install MkDocs

```bash
pip install mkdocs
```

#### Install Plugins

Enhance your documentation experience by installing Material for MkDocs and MkDocs Minify Plugin.

```bash
pip install mkdocs-material mkdocs-minify-plugin
```

### Start a Local Server

Spin up a local server to preview your Allfeat documentation.

```bash
mkdocs serve
```

### Build Your Site

Build your site using:

```bash
mkdocs build
```

That's it! You're now equipped to dive into the world of Allfeat. Happy coding! 🎵🚀
