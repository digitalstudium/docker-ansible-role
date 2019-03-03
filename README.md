Role Name
=========

This role installs docker and docker-compose on Centos

Requirements
------------

Python installed on target host, Ansible 2.7 on managing host

Role Variables
--------------

Variable | Description | Default value
--- | --- | ---
`install_from_rpms` | If "yes", docker will be installed from .rpm | *no* 
`rpm_packages` | The list of .rpm urls from which docker and its dependencies will be iinstalled. | - https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-18.09.3-3.el7.x86_64.rpm
- https://download.docker.com/linux/centos/7/x86_64/stable/Packages/docker-ce-cli-18.09.3-3.el7.x86_64.rpm
- https://download.docker.com/linux/centos/7/x86_64/stable/Packages/containerd.io-1.2.4-3.1.el7.x86_64.rpm
`yum_packages` | The list of packages to install docker | - docker-ce
- docker-ce-cli
- containerd.io
`pre_packages` | The list of prerequisited packages | - yum-utils
- device-mapper-persistent-data
- lvm2

Example Playbook
----------------

```yaml
- hosts: scaleway
  roles:
    - docker-ansible-role
```

License
-------

BSD

Author Information
------------------

Costel Shootkin, costel@digitalstudium.com
