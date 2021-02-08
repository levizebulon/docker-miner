ARG BASE_CONTAINER=levizebulon/base-miner
FROM $BASE_CONTAINER

# 切换到tmp目录
WORKDIR /tmp

ENV ETHMINER_ADDRESS="https://github.com/ethereum-mining/ethminer/releases/download/v0.18.0/ethminer-0.18.0-cuda-9-linux-x86_64.tar.gz" \
    ETHMINER_NAME="ethminer-0.18.0-cuda-9-linux-x86_64.tar.gz"

# Using the ethminer released to download ethminer
RUN wget -q "${ETHMINER_ADDRESS}" \
 && tar xzf "${ETHMINER_NAME}" -C /usr/local --owner root --group root --no-same-owner \
 && rm "${ETHMINER_NAME}" 

WORKDIR /root

