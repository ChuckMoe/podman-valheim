# Image
The image used was created by [lloesche](https://hub.docker.com/r/lloesche/valheim-server). For all variable descriptions, go there.

# Volumes
Change the volumes.hostPath.path to the directory where you want to save and access all the data available to Valheim. If you do not want or need direct access, you can instead use:

```yaml
volumes:
  - name: data
    persistentVolumeClaim:
          claimName: valheim-data
```

# Commands

Start Valheim
```bash
podman play kube --configmap=secrets.yaml pod.yaml
```

Stop Valheim
```bash
podman play kube --down pod.yaml
```

To update Valheim, aka. use the newest container, just stop and start again.
