FROM wjx0912/cuda_cudnn:latest
LABEL maintainer "yongjian <weiqi5@qq.com>"


RUN cd ~/torch && ./install.sh -b
RUN cd ~/darforest && sh ./compile.sh

RUN echo "for test nvidia driver,    please run command: nvidia-smi"
RUN echo "for test cuda/cudnn/torch, please run command: th -lcutorch -e 'cutorch.test()'"
