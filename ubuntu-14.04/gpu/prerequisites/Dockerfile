FROM nvidia/cuda:7.5-cudnn4-devel-ubuntu14.04
MAINTAINER Siew Kar Fai <karfai0317@gmail.com>

RUN apt-get update && apt-get install -y \
    bc \
    git \
    wget \
    unzip \
    \
    libprotobuf-dev \
    libleveldb-dev \
    libsnappy-dev \
    libopencv-dev \
    libhdf5-serial-dev \
    protobuf-compiler \
    \
    libatlas-base-dev && \
    \
    apt-get install -y --no-install-recommends \
    libboost-all-dev && \
    \
    apt-get install -y \
    libgflags-dev \
    libgoogle-glog-dev \
    liblmdb-dev && \
    \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /tmp/*
