Torch7, CUDA8, CUDNN5.1 (Ubuntu 14.04)

usage
================================================================
	1. install nvidia driver, latest version >= NVIDIA-Linux-x86_64-375.26.run
	2. install nvidia docker, latest version >= nvidia-docker_1.0.0.rc.3-1_amd64.deb
	3. docker pull wjx0912/cuda_torch
	4. run container: nvidia-docker run -it -v /data:/data --name cuda_torch cuda_torch:latest /bin/bash
	5. open another terminal: nvidia-docker exec -it cuda_torch /bin/bash
	6. before run cuda/cudnn/torch, you need run nvidia-smi *SUCCESS* on container.

source description
================================================================
	I've contacted docker support team, and according to their response, 
	the current limits on Automated Builds are:

	- 2 hours
	- 2 GB RAM
	- 1 CPU
	- 30 GB Disk Space

	So, for larger builds you have to either break them into several Automated Builds connected by FROM 
	statements and Repository Links, or build them locally on your machine and push them to the repository.

	buld on localhost: docker build --tag cuda_torch .
