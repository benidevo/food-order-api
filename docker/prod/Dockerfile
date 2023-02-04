FROM python:3.10-slim-bullseye

WORKDIR /app

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN apt-get update
RUN apt-get -y --no-install-recommends install netcat build-essential cargo libpq-dev

RUN pip install --upgrade pip
COPY ./requirements ./requirements
RUN pip install -r ./requirements/prod.txt

COPY . .

CMD ["sh", "/app/docker/entrypoint.sh"]
