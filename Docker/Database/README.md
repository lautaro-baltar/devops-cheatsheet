# Dockerized Databases

In this section you can find a combination of Database and Database Interface based in docker-compose files, with this approach you can easily deploy both the Database and the GUI at the same time.

You can find more information abouth each service within the owner documentation, all of them listed bellow.

# Deployment

All of the services are deployed by just using:

    docker-compose -f [COMPOSE_FILE_PATH] up -d

# Services

## Mongo + Mongo-Express

Owner page and documentation
- https://hub.docker.com/_/mongo
- https://hub.docker.com/_/mongo-express

Once deployed you can access the Mongo-Express web Interface at: 

http://localhost:8081/

---

## MySQL + phpMyAdmin

Owner page and documentation
- https://hub.docker.com/_/mysql
- https://hub.docker.com/r/phpmyadmin/phpmyadmin/

Once deployed you can access the phpMyAdmin web Interface at: 

http://localhost:8080/

---

## Postgres + PgAdmin

Owner page and documentation
- https://hub.docker.com/_/postgres
- https://hub.docker.com/r/dpage/pgadmin4/

Once deployed you can access the PgAdmin web Interface at: 

http://localhost:8081/

---

## Redis + RedisCommander

Owner page and documentation
- https://hub.docker.com/_/redis
- https://hub.docker.com/r/rediscommander/redis-commander

Once deployed you can access the Redis Commander web Interface at: 

http://localhost:8081/

---

# Helpers

The Makefile simplifies some basic tasks:

### Mongo
- `make mongo up` deploys the `Mongo + MongoExpress` containers
- `make mongo stop` stops the `Mongo + MongoExpress` containers
- `make mongo down` stops and deletes the `Mongo + MongoExpress` containers

### MySQL
- `make mysql up` deploys the `MySQL + phpMyAdmin` containers
- `make mysql stop` stops the `MySQL + phpMyAdmin` containers
- `make mysql down` stops and deletes the `MySQL + phpMyAdmin` containers

### Postgres
- `make postgres up` deploys the `Postgres + PgAdmin` containers
- `make postgres stop` stops the `Postgres + PgAdmin` containers
- `make postgres down` stops and deletes the `Postgres + PgAdmin` containers

### Redis
- `make redis up` deploys the `Redis + RedisCommander` containers
- `make redis stop` stops the `Redis + RedisCommander` containers
- `make redis down` stops and deletes the `Redis + RedisCommander` containers

Execute `make` or `make help` from the Database directory to show all available tasks.