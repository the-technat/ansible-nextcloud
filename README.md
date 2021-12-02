# ansible-hetzner-nextcloud
![build](https://img.shields.io/gitlab/pipeline-status/ansible_technat/ansible-hetzner-nextcloud?branch=develop)

Ansible Playbook to setup nextcloud on Debian Bullseye.

## Credits

This is my very first ansible playbook and it highly copied from https://github.com/ReinerNippes/nextcloud. 


## Development

### Create inventory

Make sure the information to access the server is correct.

### Run locally

```console
ansible-galaxy install -r requirements.yml
ansible-playbook nextcloud.yml -v 
```
