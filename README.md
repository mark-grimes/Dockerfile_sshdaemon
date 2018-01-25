# SSH daemon

Used for accessing files in other containers with the "--volumes-from" run option.
This started out from the example in the [docker guide for running ssh](https://docs.docker.com/engine/examples/running_ssh_service/);
but I couldn't find a public image of it so built it myself. Since then I've switched
to using an Alpine linux base image with dropbear, since it drops the image size from
250MB to less than 4.5MB.

The image is available at [markgrimes/sshdaemon](https://hub.docker.com/r/markgrimes/clientserver_build/)

## Supported Architectures

Supported architectures are:

* amd64 - from the markgrimes/sshdaemon:amd64 tag. This is built automatically by the Docker Hub servers.
* arm32v6 - from the markgrimes/sshdaemon:arm32v6 tag. This is built manually on a Raspberry Pi and pushed up to Docker Hub.

The latest tag (or no tag) is the multi-arch manifest, i.e. docker pull markgrimes/dnsmasq or
docker pull markgrimes/dnsmasq:latest will automatically select the correct image for your system.
This manifest tag is created by manually running [Phil Estes' manifest-tool](https://github.com/estesp/manifest-tool)
when the architecture tags change.
