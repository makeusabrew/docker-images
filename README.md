# Docker images

A collection of my public Docker images as hosted on the
[DOCKER index](https://index.docker.io/u/makeusabrew/)

## [makeusabrew/mongodb](https://index.docker.io/u/makeusabrew/mongodb/)

A MongoDB server built from 10gen's apt repository. Exposes port 27017,
mounts /data/db as a volume.

## [makeusabrew/redis](https://index.docker.io/u/makeusabrew/redis/)

A simple Redis server. Currently builds the latest 2.8.0
release candidate from source. Exposes port 6379, mounts /redis-data as
a volume.

## [makeusabrew/zeromq](https://index.docker.io/u/makeusabrew/zeromq/)

Installs ZeroMQ 3.2.4 on an Ubuntu 12.10 base. Doesn't have a CMD
or ENTRYPOINT as ZMQ is a daemonless process.
