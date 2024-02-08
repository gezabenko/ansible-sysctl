Ansible - sysctl
=========

Manage sysctl settings

Requirements
------------

NA

Role Variables
--------------

Implemented all parameters and associated defaults, but not set. Just the `name` parameter is necessary.
```yaml
sysctl_default__sysctl_set: true
sysctl_default__sysctl_file: "/etc/sysctl.d/99-local.conf"
sysctl__all:
  - name: vm.swappiness
    value: 10
    reload: true
sysct__gateways:
  - name: net.ipv4.ip_forward
    value: 1
```

> And see `default/main.yml` file.

Dependencies
------------

- [ansible.posix.sysctl](https://docs.ansible.com/ansible/latest/collections/ansible/posix/sysctl_module.html)

Example Playbook
----------------

```yaml
 - hosts: servers
   roles:
     - { role: ansible-sysctl, tags: [ sysctl ] }
```

License
-------

GPLv3
