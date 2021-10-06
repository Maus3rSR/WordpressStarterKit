# Wordpress StartKit

> Author [Kevin Unfricht](https://www.linkedin.com/in/kevinunfricht/)

## Purpose

Launch Wordpress project in minute with a basic structure. It use [WpPackagist](https://wpackagist.org/) for plugins and themes

## Requirements

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/) if not shipped within

## Configuration

- Copy `.env.sample` to `.env` and configure its variables
- Copy `local.yml.sample` to `local.yml` and configure this docker-compose file to fit your needs. _NB: This file is an override of `base.yml`_

## Launch

> **Note:** If you have `composer` installed, you will launch scripts by using `composer` cli command. If you don't, you'll need `php` installed to launch with the `composer.phar` file with `php composer.phar` command

- Install plugins dependencies by using `composer install-deps` or `php composer.phar install-deps-php` comand
- Launch containers by using `composer docker` or `php composer.phar docker` command

**And voilà!**

> **Note:** `install-deps` will add a few usefull plugins that will fit basic needs. Its personal choices, you can of course install what you'll need/want

> **Note:** There are some few docker commands available inside compose scripts:
> - `docker` up services in daemon mode _(in background)_
> - `docker-nodaemon` launch services
> - `docker-down` down services
> - `docker-down-volumes` down services and removes volumes, or just remove volumes if already downed
> 
> If for any reason you need to access one of your container, use `docker exec -it container_name /bin/bash` command