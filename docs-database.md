# databases
Dockistry supports all databases via docker-compose, and this documentation explains some of our baseline data strategies for SPA reactive applications.

### attached containers
- generally speaking, all databases are volume mounted to the host or flocker/gluster/efs
- we use various CRUD API(s) that work with various DB(s) such as:
  * swagger
  * goat
  * php-crud
  * laravel eloquent
  * swift vapor
- databases are generally provided as attachment containers
- our general strategy is to always provide some sort of web-based admin
- we generate the passwords on the fly and insert them into docker-compose
- our baseline strategic data containers currently support
  * Mysql Innodb
  * Mariadb Innodb
  * Postgre 
  * Citus (Postgre sharded)
- we utilize boilerplate SQL for membership such as [membership.db](https://github.com/membership/membership.db)

### docker attachment containers
the following list is composed of private StackFork docker images we pre-compose for the purpose of attaching to strategies as baseline database layers. these are **not** performance-tuned currently, as we do performance tuning in prodstack-* only.

each of these is it's own repository and docker registry image for use with docker-compose
- postgre
  * postgre with [php-crud-api](https://github.com/mevdschee/php-crud-api)
  * citus with [php-crud-api](https://github.com/mevdschee/php-crud-api)
- mysql
  * mysql with [php-crud-api](https://github.com/mevdschee/php-crud-api)
  * mariadb with [php-crud-api](https://github.com/mevdschee/php-crud-api)
- eloquent
  * [generator for laravel](https://www.npmjs.com/package/generator-laravel)
- admins
  * phpmyadmin dockerhub
  
