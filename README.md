#Vagrant Symfony 2 Box setup

## Requirements
* [VirtualBox](https://www.virtualbox.org)
* [Vagrant](http://vagrantup.com)
* [vagrant-hostmanager](https://github.com/smdahlen/vagrant-hostmanager)
	* `vagrant plugin install vagrant-hostmanager`

## Installation
####This setup is based and tested with Ubuntu Precise 64 bit base box, with Vagrant 1.5.1 version

Clone this repository

    ```$ git clone https://github.com/josevillalobos/vagrant-symfony2-box.git```

* run vagrant (for the first time it should take up to 30-60 min)
    ```$ vagrant up```
    
* Web server is accessible with http://www.symfony-box.local (Host address can be changed in Vagrantfile)

* PhpMyAdmin is accessible with http://www.symfony-box.local/phpmyadmin

* Vagrant automatically setups database with this setup:

    * Username: root
    * Password: root
    * Database: symfony

## Installed components

* [Nginx](http://nginx.org/en/)
* [MySQL](http://www.mysql.com/)
* [PHP-FPM](http://php-fpm.org/)
* [PhpMyAdmin](http://www.phpmyadmin.net/home_page/index.php)
* [MongoDB](http://www.mongodb.org/)
* [Redis](http://redis.io/)
* [GiT](http://git-scm.com/)
* [Composer](http://getcomposer.org)
* [Vim](http://www.vim.org/)
* [PEAR](http://pear.php.net/)
* [cURL](http://curl.haxx.se/)
* [Node.js](http://nodejs.org/)
* [npm](https://npmjs.org/)
* [less](http://lesscss.org/)
* [OpenJDK](http://openjdk.java.net/)
* [sass](http://sass-lang.com/)
* [Compass](http://compass-style.org/)
* [Imagic](http://www.imagemagick.org/script/index.php)
* [Capistrano](https://github.com/capistrano/capistrano)
* [Capifony](http://capifony.org/)
* [phpqatools](http://phpqatools.org/)
* [memcached](http://memcached.org/)
* 

## SYMFONY2 + nginx CONF

For nginx not to overwrite Symfony2 errors just change this configuration in nginx configuration files:

-> proxy_params

proxy_buffer_size 128k;
proxy_buffers 4 256k;
proxy_busy_buffers_size 256k;

-> fastcgi_params

fastcgi_buffer_size 128k;
fastcgi_buffers 4 256k;
fastcgi_busy_buffers_size 256k;
