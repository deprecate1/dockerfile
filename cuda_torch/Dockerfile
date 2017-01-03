FROM wjx0912/cuda_cudnn:latest
LABEL maintainer "yongjian <weiqi5@qq.com>"

RUN cd ~/torch      && ./install.sh -b

ENV PATH=/root/torch/install/bin/:$PATH
RUN luarocks install class
RUN luarocks install image
RUN luarocks install tds
RUN luarocks install cudnn
RUN luarocks install torchnet

RUN cd ~/darforest  && sh ./compile.sh
RUN mkdir -p ~/darkforest/models
RUN cp ~/darkforest.data/df_models/* ~/darkforest/models/

RUN echo "for test nvidia driver,    please run command: nvidia-smi"
RUN echo "for test cuda/cudnn/torch, please run command: th -lcutorch -e 'cutorch.test()'"
