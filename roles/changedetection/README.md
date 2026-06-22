# changedetection

## Example playbook

```yaml
- hosts: my-server
  roles:
    - eriol.pod.changedetection
```

## Browser support

Browser support is enabled by default using changedetection.io's recommended
sockpuppetbrowser sidecar. Disable it with:

```yaml
changedetection_browser: false
```

When enabled, the app is configured with `PLAYWRIGHT_DRIVER_URL` pointing at the
browser container in the same Podman pod. You may still need to enable
Playwright/Chrome fetching in changedetection.io settings or per watch.
