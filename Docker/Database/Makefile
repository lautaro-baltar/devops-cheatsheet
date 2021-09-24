.DEFAULT_GOAL := help

mongo-up: ## Deploys the Mongo + MongoExpress containers
	docker-compose -f Mongo_MongoExpress.yaml up -d
	docker-compose -f Mongo_MongoExpress.yaml ps
mongo-stop: ## Stops the Mongo + MongoExpress containers
	docker-compose -f Mongo_MongoExpress.yaml stop
mongo-down: ## Stops and Deletes the Mongo + MongoExpress containers
	docker-compose -f Mongo_MongoExpress.yaml down

mysql-up: ## Deploys the MySQL + phpMyAdmin containers
	docker-compose -f MySQL_phpMyAdmin.yaml up -d
	docker-compose -f MySQL_phpMyAdmin.yaml ps
mysql-stop: ## Stops the MySQL + phpMyAdmin containers
	docker-compose -f MySQL_phpMyAdmin.yaml stop
mysql-down: ## Stops and Deletes the MySQL + phpMyAdmin containers
	docker-compose -f MySQL_phpMyAdmin.yaml down

postgres-up: ## Deploys the Postgres + PgAdmin containers
	docker-compose -f Postgres_PgAdmin.yaml up -d
	docker-compose -f Postgres_PgAdmin.yaml ps
postgres-stop: ## Stops the Postgres + PgAdmin containers
	docker-compose -f Postgres_PgAdmin.yaml stop
postgres-down: ## Stops and Deletes the Postgres + PgAdmin containers
	docker-compose -f Postgres_PgAdmin.yaml down

redis-up: ## Deploys the Redis + Redis Commander containers
	docker-compose -f Redis-RedisCommander.yaml up -d
	docker-compose -f Redis-RedisCommander.yaml ps
redis-stop: ## Stops the Redis + Redis Commander containers
	docker-compose -f Redis-RedisCommander.yaml stop
redis-down: ## Stops and Deletes the Redis + Redis Commander containers
	docker-compose -f Redis-RedisCommander.yaml down

help:
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-16s\033[0m %s\n", $$1, $$2}'
