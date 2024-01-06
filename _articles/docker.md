---
layout: default
---
## Examples

### Ephemeral shell

Launch a shell in an ephemeral container, mounting the current directory of the host as the working directory

```
docker run --rm -it -v $(pwd):/ws -w /ws $IMAGE
```

A similar command for rootless `podman`

```
podman run --userns=keep-id --rm -it -v $(pwd):/ws -w /ws $IMAGE
```
