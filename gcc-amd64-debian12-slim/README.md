# gcc amd64 Container

Meant to be ran interactively as a tool container. Basic tools to compile 64-bit C programs are included. 

**NOTE**: For SELinux distributions, use the `:z` appending on the volume mount to make sure SELinux doesn't block writes to the mount.

```bash
podman run -it --rm -v $(pwd):[workdir here]:z [name of the image]
```
