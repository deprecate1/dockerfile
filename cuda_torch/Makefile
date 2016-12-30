all: check build
	@echo "all success......"

check:
	nvidia-docker --version

build:
	docker build --tag cuda_torch:0.1 .

run:
	nvidia-docker run -it -v /data:/data --name cuda_torch cuda_torch:0.1 /bin/bash

exec:
	nvidia-docker exec -it cuda_torch /bin/bash

save:
	nvidia-docker save cuda_torch -o image_bak1.tar

load:
	nvidia-docker load            -i image_bak1.tar
