# Redis Slave Dockerfile

This Dockerfile is based off: https://github.com/docker-library/redis/tree/7dec62fe6de187165dce3f771efa57ce4e5d7a32/3.0/alpine

We are not using a base image currently as we need to base of alpine:edge
due to an issue with using `search` in `/etc/resolv.conf`.

See: https://github.com/gliderlabs/docker-alpine/issues/8 for more info.

The `redis.conf` file is simply has the `slaveof` directive changed.
