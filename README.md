# Docker-compose for Drupal 8 Development

## Dependencies

* [Docker](https://www.docker.com/)
* [Docker Compose](https://docs.docker.com/compose/install/)

## How it works

### Download this repo

With git clone or download button

### Copy drupal code into www folder

If you want one specific version (example with 8.3.2) :

`git clone --branch 8.3.2 http://git.drupal.org/project/drupal.git www`

If you yant the latest version :

`git clone http://git.drupal.org/project/drupal.git www`

**INFO** : If the version is 8.4.0-dev the drupal console doesn't work

### Start the containers

For the first time, create the containers :

`docker-compose up -d`

If you have already created the containers you must to start the containers :

`docker-compose start`

### Install Drupal 8 vendors with composer

`docker-compose exec web composer install -o`

After that you can visit http://localhost

### Install Drupal 8 by using Drupal console

`docker-compose exec web drupal init`

`docker-compose exec web drupal site:install --db-host=mysql --db-name=drupal8 --db-user=root --db-pass=root`

### Access to PhpMyAdmin

Visit http://localhost:8080
