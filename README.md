
# Docker Image with Ubuntu 26 base image

This repo was created in order to test ansible roles with molecule.

## Build it locally

  docker build - < Dockerfile

## Use it from dockerhub

    https://hub.docker.com/repository/docker/lotusnoir/ansible_molecule_test_images:ubuntu26

## Run locally

    docker pull lotusnoir/ansible_molecule_test_images:ubuntu26
    docker run -d --privileged --volume=/sys/fs/cgroup:/sys/fs/cgroup:ro lotusnoir/ansible_molecule_test_images:ubuntu26
    docker ps -a
    ocker exec -t DOCKER_ID /bin/bash
