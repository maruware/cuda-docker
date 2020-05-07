FROM maruware/cuda:10.2-base-ubuntu20.04

ENV NCCL_VERSION 2.5.6

RUN apt-get update && apt-get install -y --no-install-recommends \
    cuda-libraries-$CUDA_PKG_VERSION \
cuda-nvtx-$CUDA_PKG_VERSION \
libcublas10=10.2.2.89-1 \
libnccl2=$NCCL_VERSION-1+cuda10.2 && \
    apt-mark hold libnccl2 && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
