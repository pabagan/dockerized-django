# Dockerized Django
Built using Oficial images with some Docker-Compose
* [Python](https://hub.docker.com/_/python/).
* [Postgres](https://hub.docker.com/_/postgres/).

## Scaffold
```bash
├── <appSelectedName>       # App scaffold created by Django startproject
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── docker-compose.yml      # Docker compose
├── Dockerfile              # Docker to configure Python 3
├── LICENSE.md
├── manage.py               # file created by Django startproject
├── README.md
└── requirements.txt        # python dependencies
```

## Create an APP
Need to delete `/<appSelectedName>` and `manage.py` if already exist. Then at project root run:

```bash
# run ./.sh/create-new.sh <projectName>
docker-compose run web django-admin.py startproject <xxxName> .
```

Or run the bash included in `/.sh` folder. From root would be a:

```bash
./.sh/create-new.sh demoApp
```

## Run Docker
* Run `docker-compose up` (needs [Docker Compose](https://docs.docker.com/compose/) installed).

## Once running
* Go to your [http://0.0.0.0:8000/](http://0.0.0.0:8000/) to see dJango App.

## Requirements
* [Docker Engine](https://docs.docker.com/installation/).
* [Docker Compose](https://docs.docker.com/compose/).
* [Docker Machine](https://docs.docker.com/machine/) (Mac and Windows only).
