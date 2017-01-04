cuda8, cudnn5.1 from nvidia image
=========================
this container is base image, latest cuda and cudnn integrated.

buld on localhost: docker build --tag cuda_cudnn .

autobuild at hub.docker.com: [https://hub.docker.com/r/wjx0912/cuda_cudnn/]()

other image such as torch7 base on this image, you can get it: [https://hub.docker.com/r/wjx0912/cuda_torch/]()
