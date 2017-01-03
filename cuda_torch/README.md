Torch7, CUDA8, CUDNN5.1 (Ubuntu 14.04)

================================================================

usage

	1. install nvidia driver, latest is NVIDIA-Linux-x86_64-375.26.run
	2. install nvidia docker, latest is nvidia-docker_1.0.0.rc.3-1_amd64.deb
	3. docker pull wjx0912/cuda_torch
	4. run container: nvidia-docker run -it -v /data:/data --name cuda_torch cuda_torch:latest /bin/bash

================================================================

source description


	the docker base on: wjx0912/cuda
	i have integrate latest cuda, cudnn, torch. before run docker, you only need nvidia-smi run success on host and container.

	run docker:
	nvidia-docker run -it -v /data:/data --name cuda_torch cuda_torch:latest /bin/bash
	
	open another terminal:
	nvidia-docker exec -it cuda_torch /bin/bash
