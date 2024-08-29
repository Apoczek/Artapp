# Artapp

Wymagania:
- docker min 20.04
- docker compose v2

Start the dockers for local develop:\
`make start` 

Stop the dockers for local develop:\
`make stop`

Restart the dockers:\
`make restart`

Build images:\
`make build`

Go into backend container:\
`make bash`

Do laravel migrations:\
`make migrate`

Seeding the database:\
`make seed`

To make laravel link to storage:\
`make storage-link`

Deleting the database:\
`make clear-volume`

Install composer dependencies:\
`make install-vendor`

Install npm packages:\
`make npm-install`

Compile npm:\
`make npm-dev`

If there are issues with database go to database docker, login to mariadb and do as follows:

`CREATE DATABASE IF NOT EXISTS artapp_database;`\
`CREATE USER IF NOT EXISTS 'artur'@'%' IDENTIFIED BY 'secret';`\
`GRANT ALL PRIVILEGES ON artapp_database.* TO 'artur'@'%';`\
`FLUSH PRIVILEGES;`