Ansible role: Helm
==================

Install Helm for Kubernetes.

Role Variables
--------------

```
ENTRY POINT: main - Install Helm for Kubernetes

OPTIONS (= is mandatory):

- helm_apt_key_fingerprint
        The apt key fingerprint for the helm repo
        [Default: (null)]
        type: str
```

Installation
------------

This role can either be installed manually with the ansible-galaxy CLI tool:

    ansible-galaxy install git+https://github.com/wandansible/helm,main,wandansible.helm
     
Or, by adding the following to `requirements.yml`:

    - name: wandansible.helm
      src: https://github.com/wandansible/helm

Roles listed in `requirements.yml` can be installed with the following ansible-galaxy command:

    ansible-galaxy install -r requirements.yml

Example Playbook
----------------

    - hosts: kubernetes_hosts
      roles:
         - role: wandansible.helm
           become: true
