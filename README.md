# clab-dind

A Docker-in-Docker (DinD) image with Containerlab pre-installed. This image is designed to run Containerlab topologies within a Docker container, providing an isolated environment for network simulations.

## Features

- Containerlab pre-installed
- Bash completion for Containerlab

## Usage

### Pull

```bash
docker ghcr.io/flosch62/clab-dind:latest
```

### Running the Container

To run the container:
```bash
docker run -it --privileged --cgroupns=host ghcr.io/flosch62/clab-dind:latest
```

This command:
- Starts an interactive container (-it)
- Grants extended privileges to the container (--privileged), necessary for running Docker inside Docker
- Uses the host's cgroup namespace (--cgroupns=host), which is required for proper functioning of Docker inside the container

### Using Containerlab

Once inside the container, you can use Containerlab as you normally would. For example:
```bash
containerlab deploy -t your_topology.yml
```

## Automated Builds

This image is automatically built and pushed to GitHub Container Registry whenever a new version of Containerlab is released. The current Containerlab version in the latest image is:

CONTAINERLAB_VERSION="0.57.4"