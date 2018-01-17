# Playbooks

```
     _              _ _     _
    / \   _ __  ___(_) |__ | | ___
   / _ \ | '_ \/ __| | '_ \| |/ _ \
  / ___ \| | | \__ \ | |_) | |  __/
 /_/   \_\_| |_|___/_|_.__/|_|\___|
```

These are my ansible playbooks :). Here be dragons.

### kubeadm-ansible

Debian / Ubuntu / CentOS

Fork of: https://github.com/kairen/kubeadm-ansible/ with some of my modifications (get it to work on Debian 9)

```sh
cd kubeadm-ansible

# Edit as necessary
vim inventory
vim group_vars/all.yaml
ansible-playbook site.yaml -i inventory
```

### ssh-provision


Creates a user / provisions a group of servers and copies over your local SSH public key.

```sh
cd ssh-provision
ansible-playbook site.yaml -i inventory --extra-vars="create_user=USERYOUWANTTOCREATE"
```


### docker

Debian / Ubuntu only

Creates a Docker host

```sh
cd docker
ansible-playbook site.yaml -i inventory
```

### libvirt

Debian 9 only

Creates a KVM host with the user `libvirt`. This copies over your local public SSH key for access.

```sh
cd libvirt
ansible-playbook site.yaml -i inventory
G:w```
