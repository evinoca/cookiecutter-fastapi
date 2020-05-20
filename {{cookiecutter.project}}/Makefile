.PHONY: dev-local
.SILENT: 

IMAGE_TAG ?= latest

dev-local:
	pipenv run uvicorn app.main:app --reload

build:
	docker build . -t docker build . --file Dockerfile --tag {{ cookiecutter.registry_name }}/{{ cookiecutter.project }}:${IMAGE_TAG}