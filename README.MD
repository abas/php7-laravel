# Docker Laravel PHP7

## Basic Usage
cloning this repo
```
    # clone this repository
    $ git clone https://github.com/abas/php7-laravel.git
    $ cd php7-laravel
```

> Building Images

this step will be take some time, on other hand you can brew the coffea or snack something :>
```bash
    $ docker build -f Dockerfile -t your_dockerhub_username/images_name:tagname .
    # example
    $ docker build -f Dockerfile -t kankuu/php7-laravel .
```
this step will created new images called kankuu/php7-laravel, also you can check that images with `docker images | grep php7-laravel`


> Image Usage

if everything is done, you can run the container by single line like bellow
```bash
    $ docker run -d --name container_name -v /path/to/laravel/project:/var/www --net local_network -w /var/www kankuu/php7-laravel
    
    # to check is that container already running you can type
    $ docker ps -a | grep container_name
    
    # if status of container is [Exited] trying to check log
    $ docker logs container_name
```
or you can make `docker-compose` file like i was created. 

**<Kankuu>** dont be hesitate to make an __`Issue`__ or __`Pull Request`__ :>