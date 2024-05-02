# PowerShell Container

Pretty simple: Runs `pwsh` in a Debian container. The `Dockerfile` has a `qc` user created so that it's not necessary to run everything as `root`.

Compile and run the container.

**NOTE**: For SELinux distributions, use the `:Z` appendix on the volume mount to make sure SELinux doesn't block you from using the mount.

```powershell
podman run -it --rm --user qc -v $(pwd):/home/qc/files:Z [name of your image]
```
