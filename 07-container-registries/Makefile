.PHONY: build
build:
	docker build --tag my-scratch-image1:1 .

# Have to authenticate to dockerhub and create repo first:
# https://docs.docker.com/engine/reference/commandline/login/
.PHONY: push-dockerhub
push-dockerhub:
	docker tag my-scratch-image1:1 ishehroz/my-scratch-image1 # defaults to latest
	docker push ishehroz/my-scratch-image1

	docker tag my-scratch-image1:1 ishehroz/my-scratch-image1:abc-123
	docker push ishehroz/my-scratch-image1:abc-123

# Have to authenticate to ghcr.io first
# https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-to-the-container-registry
.PHONY: push-github-packages
push-github-packages:
	docker tag my-scratch-image1:1 ghcr.io/mshehrozjamshaid/my-scratch-image1 # defaults to latest
	docker push ghcr.io/mshehrozjamshaid/my-scratch-image1

	docker tag my-scratch-image ghcr.io/mshehrozjamshaid/my-scratch-image1:abc-123 # defaults to latest
	docker push ghcr.io/mshehrozjamshaid/my-scratch-image1:abc-123
