# asdf Installation Playbook

This repository contains an Ansible playbook for automating the installation of several packages and tools including [asdf](https://asdf-vm.com/#/), a CLI tool that can manage multiple language runtime versions on a per-project basis. The playbook is configured to work on localhost and is designed for macOS systems.

## Contents

1. `asdf.yml` - The Ansible playbook that automates the installation process.

## Prerequisites

You need to have [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) installed on your system to use this playbook.

## Usage

To execute the playbook, navigate to the directory containing the playbook file (`asdf.yml`) and run the following command in your terminal:

```bash
ansible-playbook asdf.yml
```

This command starts the Ansible playbook, which will automate the installation process. Please ensure that you have the necessary administrative privileges to install software on your system.

## What does the playbook do?

1. Checks if Homebrew is installed and installs it if it is not already present on the system.

2. Uses Homebrew to install several packages, including `coreutils`, `curl`, `git`, `openssl`, `readline`, `sqlite3`, `xz`, `zlib`, and `tcl-tk`.

3. Clones the `asdf` repository into the `~/.asdf` directory.

4. Appends the line `. "$HOME/.asdf/asdf.sh"` to the `~/.zsh` file.

5. Sources `asdf.sh` and adds Python as a plugin to `asdf`.

6. Installs Python version 3.10.10 and sets it as the global Python version using `asdf`.
