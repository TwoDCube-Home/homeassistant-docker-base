# Building

```shell
podman build . --build-arg BASHIO_VERSION=0.16.2 --build-arg TEMPIO_VERSION=2024.11.2 --build-arg S6_OVERLAY_VERSION=3.1.6.2 --build-arg BUILD_ARCH=amd64 --build-arg BUILD_FROM=registry.access.redhat.com/ubi9/ubi:9.5 -t ghcr.io/twodcube-home/homeassistant-docker-base:2025.02.0
```

# Home Assistant Base Images

These base images are designed as Docker base images for use with building Home Assistant containers and add-ons.
It is recommended to use these as a base for your own Home Assistant Add-ons.

Using these images as a base for other Docker projects is, however, not recommended.

The image include [S6-Overlay](https://github.com/just-containers/s6-overlay), [Bashio](https://github.com/hassio-addons/bashio) and [TempIO](https://github.com/home-assistant/tempio).

## Base images

We support version that are not EOL: https://alpinelinux.org/releases/

| Image | OS | Tags | latest |
|-------|----|------|--------|
| armhf-base | Alpine | 3.18, 3.19, 3.20, 3.21 | 3.21 |
| armv7-base | Alpine | 3.18, 3.19, 3.20, 3.21 | 3.21 |
| aarch64-base | Alpine | 3.18, 3.19, 3.20, 3.21 | 3.21 |
| amd64-base | Alpine | 3.18, 3.19, 3.20, 3.21 | 3.21 |
| i386-base | Alpine | 3.18, 3.19, 3.20, 3.21 | 3.21 |

### jemalloc

We support on our platforms jemalloc. On the application which you want to enable it, set as environment `LD_PRELOAD="/usr/local/lib/libjemalloc.so.2"` on your Dockerfile or before you start the application.

### Python images

We support the latest 3 release with the latest 3 Alpine version.

| Image | OS | Tags | latest |
|-------|----|------|--------|
| armhf-base-python | Alpine | 3.11, 3.12, 3.13, 3.11-alpine3.19, 3.11-alpine3.20, 3.11-alpine3.21, 3.12-alpine3.19, 3.12-alpine3.20, 3.12-alpine3.21, 3.13-alpine3.19, 3.13-alpine3.20, 3.13-alpine3.21 | 3.13-alpine3.21 |
| armv7-base-python | Alpine | 3.11, 3.12, 3.13, 3.11-alpine3.19, 3.11-alpine3.20, 3.11-alpine3.21, 3.12-alpine3.19, 3.12-alpine3.20, 3.12-alpine3.21, 3.13-alpine3.19, 3.13-alpine3.20, 3.13-alpine3.21 | 3.13-alpine3.21 |
| aarch64-base-python | Alpine | 3.11, 3.12, 3.13, 3.11-alpine3.19, 3.11-alpine3.20, 3.11-alpine3.21, 3.12-alpine3.19, 3.12-alpine3.20, 3.12-alpine3.21, 3.13-alpine3.19, 3.13-alpine3.20, 3.13-alpine3.21 | 3.13-alpine3.21 |
| amd64-base-python | Alpine | 3.11, 3.12, 3.13, 3.11-alpine3.19, 3.11-alpine3.20, 3.11-alpine3.21, 3.12-alpine3.19, 3.12-alpine3.20, 3.12-alpine3.21, 3.13-alpine3.19, 3.13-alpine3.20, 3.13-alpine3.21 | 3.13-alpine3.21 |
| i386-base-python | Alpine | 3.11, 3.12, 3.13, 3.11-alpine3.19, 3.11-alpine3.20, 3.11-alpine3.21, 3.12-alpine3.19, 3.12-alpine3.20, 3.12-alpine3.21, 3.13-alpine3.19, 3.13-alpine3.20, 3.13-alpine3.21 | 3.13-alpine3.21 |

## Others

### Debian images

**Note**: We prefer the Alpine based version because it's more IoT friendly. In some case, you need a glibc system like this.

| Image | OS | Tags | latest |
|-------|----|------|--------|
| armv7-base-debian | Debian | bullseye, bookworm | bookworm |
| armhf-base-debian | Debian | bullseye, bookworm | bookworm |
| aarch64-base-debian | Debian | bullseye, bookworm | bookworm |
| amd64-base-debian | Debian | bullseye, bookworm | bookworm |
| i386-base-debian | Debian | bullseye, bookworm | bookworm |

### Ubuntu images

**Note**: We prefer the alpine based version because it's more IoT friendly. In some case, you need a glibc system like this.

| Image | OS | Tags | latest |
|-------|----|------|--------|
| armv7-base-ubuntu | Ubuntu | 14.04, 16.04, 18.04 20.04 | 20.04 |
| aarch64-base-ubuntu | Ubuntu | 14.04, 16.04, 18.04 20.04 | 20.04 |
| amd64-base-ubuntu | Ubuntu | 14.04, 16.04, 18.04 20.04 | 20.04 |
| i386-base-ubuntu | Ubuntu | 14.04, 16.04, 18.04 | |

### Raspbian images

| Image | OS | Tags | latest |
|-------|----|------|--------|
| armhf-base-raspbian | Raspbian | bullseye, bookworm | bullseye |
