help:
	@cat Makefile

DOCKER_FILE=Dockerfile

SRC?=$(shell pwd)
CONTAINER_SRC=/src

JUPITER_PORT=8888
CONTAINER_JUPITER_PORT=8888

IMAGE=yantonov/pytorch
CONTAINER_NAME?=$(shell echo "$(IMAGE)" | tr '/' '_')

build:
	docker build \
		-t $(IMAGE) \
		-f $(DOCKER_FILE) .

notebook:
	docker run \
			--hostname localhost \
			-i -t \
			-p $(JUPITER_PORT):$(CONTAINER_JUPITER_PORT) \
			-v "$(SRC):$(CONTAINER_SRC)" \
			--name "$(CONTAINER_NAME)" \
			--rm \
			"$(IMAGE)" \
			"jupyter notebook \
			--notebook-dir=$(CONTAINER_SRC) \
			--ip=0.0.0.0 \
			--port=$(CONTAINER_JUPITER_PORT) \
			--no-browser \
			--allow-root"

lab:
	docker run \
			--hostname localhost \
			-i -t \
			-p $(JUPITER_PORT):$(CONTAINER_JUPITER_PORT) \
			-v "$(SRC):$(CONTAINER_SRC)" \
			--name "$(CONTAINER_NAME)" \
			--rm \
			"$(IMAGE)" \
			"jupyter lab \
			--notebook-dir=$(CONTAINER_SRC) \
			--ip=0.0.0.0 \
			--port=$(CONTAINER_JUPITER_PORT) \
			--no-browser \
			--allow-root"

ssh:
	docker run --rm -t -i -v "$(SRC):$(CONTAINER_SRC)" "$(IMAGE)" bash

root:
	docker run --rm -u 0 -t -i -v "$(SRC):$(CONTAINER_SRC)" "$(IMAGE)" bash


stop:
	docker stop "$(CONTAINER_NAME)"

pull:
	docker pull "$(IMAGE)"

uninstall:
	docker image rm "$(IMAGE)"
