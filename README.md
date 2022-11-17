# Sports-facilities proposal system

## Project setup

Run the docker container

`docker-compose up -d`

Install required packages

`docker-compose composer install`

Setup settings and services for development.
```
cp web/sites/default/_development.services.local.yml web/sites/default/services.local.yml
cp web/sites/default/_development.settings.local.php web/sites/default/settings.local.php
```

Setup site
```
docker-compose exec phpfpm vendor/bin/drush --yes site:install minimal --existing-config
```

Import drupal configuration

`docker-compose vendor/bin/drush config-import`

Export drupal configuration

`docker-compose vendor/bin/drush config-export`

## Sub theme

Sub-theme located in:

web/themes/sportsfaciliteter
