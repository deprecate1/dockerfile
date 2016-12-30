description

	1. install nvidia driver, latest is NVIDIA-Linux-x86_64-375.26.run
	2. install nvidia docker, latest is nvidia-docker_1.0.0.rc.3-1_amd64.deb
	3. docker pull wjx0912/cuda_torch
	4. run container: nvidia-docker run -it -v /data:/data --name cuda_torch cuda_torch:latest /bin/bash
