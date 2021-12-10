# wp-headless-docker

Simple docker env, for local development.

# About build:

* composer (insert plugins for headless cms)
* docker-compose hold all wp and db files localy on your host mashine
* example 'env/files' config for wp and db services

# How start 

Before run you should install docker on your PC [how install docker](https://docs.docker.com/get-docker/)

Or checkout docker already installed, just run in terminal and you get docker version info

docker -v


So if you solve docker install problems you can run this build in your ide or terminal:

docker-compose up -d


And now checkout in browser:

[PhpMyAdmin](http://localhost:8081)

[Wodpress Installation](http://localhost:8080)

> MariaDB, you should wait few seconds, after run command. Before wordpress installation checkout db with PhpMyAdmin.


---
P.S. Notes

How unlock permission for local files of worpdress run this as root

sudo chown -R [user-name]:www-data /path/to/your/local/folder

> Add full permission for your user, use command as root (sudo).
> -R flag (recursive run).
> Warning it breaks workflow as admin in cms. 


sudo chown -R www-data /path/to/your/local/folder

> This will return all back, use command as root (sudo). 
> -R flag (recursive run).
> But for better permission config use All-in-One-WP-Security-and-Firewall plugin, and yeah it includes in composer.json