FROM nvidia/cuda:7.5-cudnn4-devel-ubuntu14.04
MAINTAINER Siew Kar Fai <karfai0317@gmail.com>

# Reference: Ubuntu Installation - http://caffe.berkeleyvision.org/install_apt.html

RUN apt-get update && apt-get install -y \
# Essential command-line interface
    bc \
    git \
    wget \
    unzip \
    \
# General dependencies
    libprotobuf-dev \
    libleveldb-dev \
    libsnappy-dev \
    libopencv-dev \
    libhdf5-serial-dev \
    protobuf-compiler \
    \
# BLAS: ATLAS
    libatlas-base-dev \
    \
# Remaining dependencies
    libgflags-dev \
    libgoogle-glog-dev \
    liblmdb-dev && \
    \
# Boost C++ libraries
    apt-get install -y --no-install-recommends \
    libboost-all-dev && \
    \
# Clean up
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /tmp/*
