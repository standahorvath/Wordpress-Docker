# Wordpress-Docker
Wordpress CMS in docker container for simple and easy development

This repository is to complement the article on how to run wordpress on docker.

**Article can be found here:** [standa.tonakodi.cz/knowledge/local-wordpress-development-harness-the-power-of-docker-containers](https://standa.tonakodi.cz/knowledge/local-wordpress-development-harness-the-power-of-docker-containers)

## Requirements
- Docker

## How to run
- Clone this repository
- Run `docker-compose up -d`

## Config .env file
- docker/dev/.env

## How to access
- Wordpress: http://localhost
- PhpMyAdmin: http://localhost:8282
- MySQL: localhost:3306
  
## How to stop
- Run `docker-compose down`

