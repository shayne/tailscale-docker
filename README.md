# Automated Tailscale Docker Build

![Docker Image Version (tag latest semver)](https://img.shields.io/docker/v/shaynesweeney/tailscale/latest)
![Check Tailscale latest release](https://github.com/shayne/tailscale-docker/workflows/Check%20Tailscale%20latest%20release/badge.svg)
![Build Tailscale Docker image](https://github.com/shayne/tailscale-docker/workflows/Build%20Tailscale%20Docker%20image/badge.svg)

This repo, upon official release, automatically builds the a Tailscale Docker image from the official [tailscale/tailscale](https://github.com/tailscale/tailscale) repository. Automation is done via GitHub [workflows in this repo](https://github.com/shayne/tailscale-docker/tree/main/.github/workflows).

`docker pull shaynesweeney/tailscale`

<hr />

Proceed with Caution [[source]](https://github.com/tailscale/tailscale/blob/main/Dockerfile)

>```
> ############################################################################
> #
> # WARNING: Tailscale is not yet officially supported in Docker,
> # Kubernetes, etc.
> #
> # It might work, but we don't regularly test it, and it's not as polished as
> # our currently supported platforms. This is provided for people who know
> # how Tailscale works and what they're doing.
> #
> # Our tracking bug for officially support container use cases is:
> #    https://github.com/tailscale/tailscale/issues/504
> #
> # Also, see the various bugs tagged "containers":
> #    https://github.com/tailscale/tailscale/labels/containers
> #
> ############################################################################
> ```

Usage [[source]](https://github.com/tailscale/tailscale/blob/main/Dockerfile)
>```
> # This Dockerfile includes all the tailscale binaries.
> #
> # To build the Dockerfile:
> #
> #     $ docker build -t tailscale:tailscale .
> #
> # To run the tailscaled agent:
> #
> #     $ docker run -d --name=tailscaled -v /var/lib:/var/lib -v /dev/net/tun:/dev/net/tun --network=host --privileged tailscale:tailscale tailscaled
> #
> # To then log in:
> #
> #     $ docker exec tailscaled tailscale up
> #
> # To see status:
> #
> #     $ docker exec tailscaled tailscale status
> ```
