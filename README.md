# Playbooks

```
     _              _ _     _
    / \   _ __  ___(_) |__ | | ___
   / _ \ | '_ \/ __| | '_ \| |/ _ \
  / ___ \| | | \__ \ | |_) | |  __/
 /_/   \_\_| |_|___/_|_.__/|_|\___|
```

These are my ansible playbooks :). Here be dragons. Some are copied / forked from other locations


## Notes

All can be provisioned by simply adding your host to:

```sh
vim hosts

[all]
host1
```

### ssh-provision

**OS:** Any

Creates a user / provisions a group of servers and copies over your local SSH public key.

```sh
cd ssh-provision
cp hosts.sample hosts
ansible-playbook site.yaml -i hosts --extra-vars="create_user=USERYOUWANTTOCREATE"
```


### docker

**OS:** Debian 9

Creates a Docker host

```sh
cd docker
cp hosts.sample hosts
ansible-playbook site.yaml -i hosts
```

### libvirt

**OS:** Debian 9

Creates a KVM host

```sh
cd libvirt
cp hosts.sample hosts
ansible-playbook site.yaml -i hosts
```
