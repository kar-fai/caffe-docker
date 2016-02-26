# Caffe Docker

The following tags default to images based on [ubuntu:14.04](https://hub.docker.com/_/ubuntu/).
While GPU images is based on [nvidia/cuda:7.5-cudnn4-devel-ubuntu14.04](https://hub.docker.com/r/nvidia/cuda/)

Temporary not available for other distributions.

Check the tags reference for a given tag availability.

### CPU

Requirements : [docker-engine](https://docs.docker.com/engine/installation/)

* cpu-prerequisites [(ubuntu-14.04/cpu/prerequisites/Dockerfile)](ubuntu-14.04/cpu/prerequisites/Dockerfile)
* cpu-compilation [(ubuntu-14.04/cpu/compilation/Dockerfile)](ubuntu-14.04/cpu/compilation/Dockerfile)
* cpu-python [(ubuntu-14.04/cpu/python/Dockerfile)](ubuntu-14.04/cpu/python/Dockerfile)
* cpu-jupyter [(ubuntu-14.04/cpu/jupyter/Dockerfile)](ubuntu-14.04/cpu/jupyter/Dockerfile)

### GPU

Requirements : [nvidia-docker](https://github.com/NVIDIA/nvidia-docker)

* gpu-prerequisites [(ubuntu-14.04/gpu/prerequisites/Dockerfile)](ubuntu-14.04/gpu/prerequisites/Dockerfile)
* gpu-compilation [(ubuntu-14.04/gpu/compilation/Dockerfile)](ubuntu-14.04/gpu/compilation/Dockerfile)
* gpu-python [(ubuntu-14.04/gpu/python/Dockerfile)](ubuntu-14.04/gpu/python/Dockerfile)
* gpu-jupyter [(ubuntu-14.04/gpu/jupyter/Dockerfile)](ubuntu-14.04/gpu/jupyter/Dockerfile)
