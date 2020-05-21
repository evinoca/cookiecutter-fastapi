.PHONY: dev-local
.SILENT: 

IMAGE_NAME ?= {{ cookiecutter.registry_name }}/{{ cookiecutter.project }}
IMAGE_TAG ?= latest


dev-local:
	# FastApi will listen to localhost 8000 by default
	pipenv run uvicorn app.main:app --reload

build:
	 docker build -t ${IMAGE_NAME}:${IMAGE_TAG} .