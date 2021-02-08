# Ubuntu 16.04
# nvidia/cuda:9.0-base
# https://hub.docker.com/layers/nvidia/cuda/9.0-base/images/sha256-4f7ca42225b5779e5e05cdee23431d633fbce12f12a8b9fb51bbb6bc0040c670?context=explore 
# OS/ARCH: linux/amd64
ARG BASE_CONTAINER=nvidia/cuda:9.0-base
FROM $BASE_CONTAINER

LABEL maintainer="Docker Miner <levizebulon@gmail.com>"

# Fix DL4006
SHELL ["/bin/bash", "-o", "pipefail", "-c"]


# 切换到root用户
USER root

# Install all OS dependencies for notebook server that starts but lacks all
# features (e.g., download as all possible file formats)
ENV DEBIAN_FRONTEND noninteractive
# 安装必要软件
RUN apt-get clean \
 && apt-get update --fix-missing || true \
 && apt-get install -yq --no-install-recommends \
    wget \
    vim \
 && apt-get clean && rm -rf /var/lib/apt/lists/*
