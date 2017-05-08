# Dockerized Django Restful API

This repo contains all the basics to build a Dockerized Djano Resful API

## Set up

#### Build the djangoapi docker image :
`docker build -t djangoapi .`

#### Run app services
`docker-compose up`

#### Stop app services
`docker stop $(docker ps -a -q)`

#### Create django superuser
`docker-compose run web /code/manage.py createsuperuser`

#### Migrate database
`docker-compose run web /code/manage.py migrate`

#### Run app services again
`docker-compose up`

Django api is now ready to perform (in development env)

## Docker Images

### djangoapi

_Dockerfile_ contains the instructions for building a django app containing psycopg2 and Django Rest Framework

## Docker compose

The _docker-compose.yml_ file contains the structure of the different services of the app (postgresql and djangoapi).
