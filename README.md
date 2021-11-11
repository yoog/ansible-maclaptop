# ansible-maclaptop

Ansible roles for setting my mac laptop

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

## How to run

Run all roles
```bash
ansible-playbook setup.yml
```

Run specific roles with tags
```bash
ansible-playbook setup.yml -t <tag-names>
```
