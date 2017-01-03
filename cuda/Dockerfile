FROM nvidia/cuda:8.0-devel
LABEL maintainer "yongjian <weiqi5@qq.com>"

#ADD apt/tsinghua.edu.cn.sources.list    /etc/apt/sources.list
#ADD apt/aliyun.sources.list             /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -y curl
RUN apt-get install -y git
RUN rm -rf /var/lib/apt/lists/*

ENV CUDNN_VERSION 5
LABEL com.nvidia.cudnn.version="5"

RUN CUDNN_DOWNLOAD_SUM=a87cb2df2e5e7cc0a05e266734e679ee1a2fadad6f06af82a76ed81a23b102c8 && \
    curl -fsSL http://developer.download.nvidia.com/compute/redist/cudnn/v5.1/cudnn-8.0-linux-x64-v5.1.tgz -O && \
    echo "$CUDNN_DOWNLOAD_SUM  cudnn-8.0-linux-x64-v5.1.tgz" | sha256sum -c --strict - && \
    tar -xzf cudnn-8.0-linux-x64-v5.1.tgz -C /usr/local && \
    rm cudnn-8.0-linux-x64-v5.1.tgz && \
    ldconfig

#ADD cudnn-8.0-linux-x64-v5.1.tgz /usr/local
#RUN ldconfig

RUN git clone https://github.com/torch/distro.git ~/torch --recursive
RUN cd ~/torch && bash install-deps

RUN git clone https://github.com/facebookresearch/darkforestGo.git ~/darforest --recursive
