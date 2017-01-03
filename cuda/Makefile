all: check build
	@echo "all success......"

check:
	nvidia-docker --version

build:
	docker build --tag cuda:0.1 .

commit:
	docker commit -a "yongjian <weiqi5@qq.com>" -m "add cudnn" cuda cuda:0.2

run:
	nvidia-docker run -it -v /data:/data --name cuda cuda:0.1 /bin/bash

exec:
	nvidia-docker exec -it cuda /bin/bash

save:
	nvidia-docker save cuda -o image_bak1.tar

load:
	nvidia-docker load            -i image_bak1.tar
