PROJECT_NAME = artapp

DC = docker compose
EXEC_BACKEND = $(DC) exec backend
EXEC_PHP = $(EXEC_BACKEND) php
EXEC_COMPOSER = $(EXEC_BACKEND) composer
EXEC_NPM = $(EXEC_BACKEND) npm


start:
	$(DC) up -d

stop:
	$(DC) down

restart:
	$(DC) restart

build:
	$(DC) build

bash:
	$(EXEC_BACKEND) bash

migrate:
	$(EXEC_PHP) artisan migrate --force

seed:
	$(EXEC_PHP) artisan db:seed --force

storage-link:
	$(EXEC_PHP) artisan storage:link

clear-volume:
	$(DC) down -v

install-vendor:
	$(EXEC_COMPOSER) install

npm-install:
	$(EXEC_NPM) install

npm-dev:
	$(EXEC_NPM) run dev

setup: build start install-vendor npm-install npm-dev migrate seed