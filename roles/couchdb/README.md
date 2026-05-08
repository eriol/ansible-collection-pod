# couchdb

CouchDB container managed with rootless Podman quadlet.

The role starts CouchDB bound to `127.0.0.1:5984` by default.

## Example playbook

```yaml
- hosts: my-server
  roles:
    - eriol.pod.couchdb
```

## Create an admin user

By default CouchDB starts without an admin account. Create one after the
service is running:

```shell
curl -X PUT http://127.0.0.1:5984/_node/_local/_config/admins/myuser \
  -H "Content-Type: application/json" \
  -d '"mypassword"'
```

Verify authentication:

```shell
curl -u myuser:mypassword http://127.0.0.1:5984/_up
```
