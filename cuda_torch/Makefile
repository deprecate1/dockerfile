all: check build
	@echo "all success......"

check:
	nvidia-docker --version

build:
	docker build --tag cuda_torch .

commit:
	docker commit -a "yongjian <weiqi5@qq.com>" -m "add cudnn, torch, darkforest" cuda_torch cuda_torch

run:
	nvidia-docker run -it -v /data:/data --name cuda_torch wjx0912/cuda_torch /bin/bash

exec:
	nvidia-docker exec -it cuda_torch /bin/bash

save:
	nvidia-docker save cuda_torch -o image_bak1.tar

load:
	nvidia-docker load            -i image_bak1.tar
