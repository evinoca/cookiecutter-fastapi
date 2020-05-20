FROM python:slim

WORKDIR /services/{{ cookiecutter.project }}

COPY Pipfile Pipfile.lock ./

RUN pip install pipenv && \
    pipenv install --system

COPY . .

USER www-data
EXPOSE 8000

CMD ["uvicorn", "app.main:app", "--reload"]