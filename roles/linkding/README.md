# linkding

## Example playbook

```yaml
- hosts: my-server
  roles:
    - eriol.pod.linkding
```

## Create the first user

```shell
podman exec -ti linkding ./manage.py createsuperuser --username=eriol
```
