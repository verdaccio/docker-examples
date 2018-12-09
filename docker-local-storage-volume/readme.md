# Verdaccio and simple local storage

This example show a simple configuration `verdaccio` plus the default local storage with the minimum configuration required using `docker-compose`.

Contains

* conf: Configuration file and default user httpasswd
* storage: A published default package with 2 versions.

```bash
$> docker-compose up
```

## Login 

If you want to login into the Verdaccio instance created via these Docker Examples, please try:

Username: jpicado
Password: jpicado

## Running in Dokku

If you use the Dokku, a open-source alternative for Heroku, you can run this example using the following steps:

1. Create a new application `dokku apps:create verdaccio`
2. Pull the verdaccio image `docker pull verdaccio/verdaccio:4.x-next`
3. Tag the docker image for the app: `docker tag verdaccio/verdaccio:4.x-next dokku/verdaccio:v1`
4. Create the directories for persistent storage `mkdir -p /var/lib/dokku/data/storage/verdaccio/storage`, `mkdir -p /var/lib/dokku/data/storage/verdaccio/storage`
5. Mount the volumes: `dokku storage:mount verdaccio /var/lib/dokku/data/storage/verdaccio/storage:/verdaccio/storage` and `dokku storage:mount verdaccio /var/lib/dokku/data/storage/verdaccio/conf:/verdaccio/conf`
4. Deploy the docker image `dokku tags:deploy verdaccio v1`
5. Enjoy the application
