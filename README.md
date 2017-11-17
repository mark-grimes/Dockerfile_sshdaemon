# SSH daemon

Used for accessing files in other containers with the "--volumes-from" run option.
This started out from the example in the [docker guide for running ssh](https://docs.docker.com/engine/examples/running_ssh_service/);
but I couldn't find a public image of it so built it myself. Since then I've switched
to using an Alpine linux base image with dropbear, since it drops the image size from
250MB to less than 4.5MB.

The image is available at [markgrimes/sshdaemon](https://hub.docker.com/r/markgrimes/clientserver_build/)
