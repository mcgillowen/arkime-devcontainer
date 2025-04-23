# Arkime Dev Containers

This repo contains the Containerfile's for building Dev Containers that can be used during Arkime development.

Currently there is only a Dev Container for Ubuntu 22.04, more should come in the future.

To use the devcontainer copy the `devcontainer.json` file into either `.devcontainer.json` or `.devcontainer/devcontainer.json`
in the root of the Arkime workspace and if you are using VS Code and have the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) installed, it should ask you if you wish to reopen the current folder in the Dev Container.

For more information refer to the [Dev Containers documentation](https://code.visualstudio.com/docs/devcontainers/containers).

## Extras

If you are using `podman` as container runner, then I recommend using the `podman-devcontainer-wrapper` since it configures `podman` to run with the `docker` format instead of `oci`, it does it by setting the `BUILDAH_FORMAT` environment variable to `docker`.
This is required since the devcontainer CLI uses `SHELL` instructions when executing devcontainers which the OCI format does not support.