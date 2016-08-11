# live-dist-builder

Example: How to build an USB live distro within a docker container. Based on Debian Jessie.

## What is this?

This was made as an example on how to build your own USB live distribution within a Docker container, so your build environment just depends on docker, bash and an Internet connection.

## Does it work?

Yes.

It's just an example though. A working example. And a boilerplate for you to hack around with yourself.

## How to use it?

Run the `./run.sh` bash script. When finished, there will be an `usb.img`, which is the USB image file.

Grab the code and build something cool! This example just builds a very thin Debian Jessie.

You probably should begin at row 99 in `run.sh`, installing and fixing stuff that you need for your own Live USB Linux Distribution.

## Why is so much happening in `run.sh`, and not more being built from the `Dockerfile`?

It is not possible to use `debootstrap` from the `Dockerfile`, since there is no privileged mode during docker build. Read more about it in this [open isseue](https://github.com/docker/docker/issues/1916).
