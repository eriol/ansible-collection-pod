# Ansible collection - eriol.pod

Ansible collection to manage services with podman.

## Installation

Create a `requirements.yml` with the following content:

```yaml
---
collections:
  - name: https://noa.mornie.org/eriol/ansible-collection-pod
    type: git
    version: 0.1.0
```

and then, using ansible >= 2.10, run:

```
ansible-galaxy collection install -r requirements.yml
```
