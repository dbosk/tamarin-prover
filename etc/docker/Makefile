.PHONY: all docker-image
all: docker-image

DOCKER_ID_USER?=dbosk
DOCKER_IMAGE?=tamarin-prover

docker-image: Dockerfile
	docker build -t ${DOCKER_IMAGE} .


.PHONY: docker-push
docker-push: docker-image
	docker tag ${DOCKER_IMAGE} ${DOCKER_ID_USER}/${DOCKER_IMAGE}
	docker push ${DOCKER_ID_USER}/${DOCKER_IMAGE}


.PHONY: distclean
distclean:
	docker image rm ${DOCKER_IMAGE}
	docker image rm ${DOCKER_ID_USER}/${DOCKER_IMAGE}

.PHONY: clean
clean:
	true

