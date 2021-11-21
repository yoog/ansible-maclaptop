# ansible-maclaptop

Ansible roles for setting my mac laptop

## install ansible

NOTE: ansible 2.9 is used, hence hardcoding of the specific version!

```bash
pip3 install ansible==2.9.27
```

## Roles

### git

 * install or update to latest git
 * Add ~.ssh/config for tiq and personal keys
 * Create separate .gitconfigs for different directories

### ssh

 * Adds better ssh defaults to hosts in sshconfigs var 

### bash

 * sets bash as default terminal
 * create/use custom .bash_profile

### nvim

 * install neovim
 * creates custom init.vim config in ~/.config/nvim/
 * install vim-dim plugin/color scheme

### docker
 * install docker or upgrade if already installed  (via cask)
 * install font required for operator use
 * when installing fresh or upgrading be sure to start the Docker Desktop app to get the cli installed

### brew
 * install brew
 * NOTE: this requires running the playbook with -K

### terraform
 * install terraform 0.12.25 - this the version used on github runners

### helm
 * install the latest version of helm

### vscode
 * install the latest vscode via brew cask
 * note this won't update if already installed, update vscode from the app itself

### azurecli
 * install latest azure cli
 * updating can be done from the cli self "az upgrade" (note that this is in preview)

### go
 * install go
 * install goreleaser - <https://goreleaser.com/>

### awscli
 * install latest aws cli


## How to run

Run all roles
```bash
ansible-playbook setup.yml
```

Run specific roles with tags
```bash
ansible-playbook setup.yml -t <tag-names>
```

Run role with sudo pass
```bash
ansible-playbook setup.yml -t bash -K
```
