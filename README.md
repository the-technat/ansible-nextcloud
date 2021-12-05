# ansible-hetzner-nextcloud

![build](https://img.shields.io/gitlab/pipeline-status/ansible_technat/ansible-hetzner-nextcloud?branch=develop)

Ansible Playbook to setup nextcloud on Debian Bullseye.

## Credits

This is my very first ansible playbook and its mostly copied from [https://github.com/ReinerNippes/nextcloud](https://github.com/ReinerNippes/nextcloud).  

## Philosophy about variables

Ansible has [a lot of places](https://docs.ansible.com/ansible/latest/user_guide/playbooks_variables.html) where you can set variables. For this playbook the following pattern exists:

- Most variables are defined within a role's `default/main.yml` file and are considered to be overriden by users.
- Variables set in role's `vars/main.yml` are considered constant and should not be overriden by users.
- We don't set variables in the `inventory` file as this is mostly generated dynamically

## Usage

### Create inventory

Edit the inventory and adjust the Username, SSH Port and Public Key accordingly.

Then run it like so:

```console
pip install -r requirements.txt
ansible-galaxy install -r requirements.yml
ansible-playbook nextcloud.yml -v 
```
