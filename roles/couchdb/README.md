# couchdb

CouchDB container managed with rootless Podman quadlet.

The role starts CouchDB bound to `127.0.0.1:5984` by default. It creates
`{{ couchdb_dir }}/couchdb.env` for the official CouchDB image bootstrap
credentials.

## Example playbook

```yaml
- hosts: my-server
  roles:
    - eriol.pod.couchdb
```

Override the default credentials:

```yaml
couchdb_admin_user: myuser
couchdb_admin_password: changeme
```

## Verify access

Check CouchDB with the configured admin credentials:

```shell
curl -u myuser:changeme http://127.0.0.1:5984/_up
```
