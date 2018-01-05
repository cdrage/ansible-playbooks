# Playbooks

These are my ansible playbooks :)

```sh
ansible-playbook playbook.yaml -u user -K -i hosts.yaml
```

__docker-debian9-host:__

Creates a Docker host with the user `docker`. This copies over your local public SSH key for access.

__libvirt-debian9-host:__

Creates a KVM host with the user `libvirt`. This copies over your local public SSH key for access.

__k8s-debian9-host:__

Creates a k8s host with the user `k8s`. This copies over your local public SSH key for access.

This is intended for use with `kubeadm`.
