# Stamp Backend

Backend Docker environment for the digital stamp card service.

## Setup
Before proceeding, you should clone the [API server](https://github.com/jumakall/stamp-api) to the ``images/php/app`` directory and follow the API server's setup instructions.

### Bring the environment up
The environment can be set up automatically with Docker Compose, just run ``docker-compose up -d``. Docker Compose will automatically bind port 80 on your local machine to the correct container. After you've ran the database migrations, you should now be able to make requests to ``http://localhost``.

### Bring the environment down
Destroy the environment with ``docker-compose down``. This will remove all related containers and networks. Docker Compose automatically mounts a few directories on your local machine to the containers, so all the changes will be persisted.
