# Ansible Common

Common tools and user config for all of my servers, specifically those
created from an Ubuntu cloud-init template.

## Prerequisites

```
ansible
```

It is also assumed that there is a user named "karl" on the server,
which is the case for any servers created with my cloud-init template.

There also needs to be a ssh key named id_rsa_proxmox on the server,
and in the user's .ssh directory on the machine running
ansible-playbook.

## Usage

Update the inventory.ini as necessary.

Run the following to update all the servers:

```
ansible-playbook -i inventory.ini playbook.yml
# or, to limit the servers
ansible-playbook -i inventory.ini -l <server or group> playbook.yml
```
