# clab-dind

```bash
docker build -t clab-dind . 
```

```bash
docker run -it --privileged --cgroupns=host clab-dind
```

- Grants extended privileges to the container (--privileged), necessary for running Docker inside Docker
- Uses the host's cgroup namespace (--cgroupns=host), which is required for proper functioning of Docker inside the container
