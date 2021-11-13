# ansible-maclaptop

Ansible roles for setting my mac laptop

## install ansible

NOTE: ansible 2.9 is used in prod hence hardcoding of the specific version!

```bash
pip3 install ansible==2.9.27
```

## Roles

### git

 * Add ~.ssh/config for tiq and personal keys
 * Create separate .gitconfigs for different directories

### ssh

 * Adds better ssh defaults to hosts in sshconfigs var 

### bash

 * sets bash as default terminal
 * creates .bash_profile based on template

### nvim

 * install neovim
 * creates custom init.vim config in ~/.config/nvim/

### docker
 * install docker desktop (via cask)

### brew
 * install brew
 * NOTE: this requires running the playbook with -K

### terraform
 * install terraform (12.25)

## How to run

Run all roles
```bash
ansible-playbook setup.yml
```

Run specific roles with tags
```bash
ansible-playbook setup.yml -t <tag-names>
```
