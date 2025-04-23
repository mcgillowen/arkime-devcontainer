# Arkime Dev Containers

This repo contains the Containerfile's for building Dev Containers that can be used during Arkime development.

Currently there is only a Dev Container for Ubuntu 22.04, more should come in the future.

## Extras

If you are using `podman` as container runner, then I recommend using the `podman-devcontainer-wrapper` since it configures `podman` to run with the `docker` format instead of `oci`, it does it by setting the `BUILDAH_FORMAT` environment variable to `docker`.
This is required since the devcontainer CLI uses `SHELL` instructions when executing devcontainers which the OCI format does not support.