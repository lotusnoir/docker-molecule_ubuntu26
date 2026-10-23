# Docker Image with Ubuntu 26 base image

This repo was created in order to test ansible roles with molecule.

## Build it locally

### Build

  docker build -t ubuntu26img .

### Run

  docker run -d --name ubuntu26con \
  --privileged \
  --cgroupns=host \
  --volume=/sys/fs/cgroup:/sys/fs/cgroup:rw ubuntu26img

### Test

  docker exec ubuntu26con systemctl is-system-running --wait

### Explore

  docker exec -it ubuntu26con bash

## Use it from dockerhub

    https://hub.docker.com/repository/docker/lotusnoir/ansible_molecule_test_images:ubuntu26
