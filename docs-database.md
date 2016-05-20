## t.o.c.
- [dockistry home](https://github.com/forktheweb/dockistry)
- [why use dockistry?](https://github.com/forktheweb/dockistry/blob/master/docs-why.use.this.md)
- [what do we mean by fullstack strategy?](https://github.com/forktheweb/dockistry#what-is-a-fullstack-strategy)
- [author info](https://labs.stackfork.com:2003/dockistry-contributors/cho)
- [preface to dockistry](https://github.com/forktheweb/dockistry/blob/master/docs-preface.md) 
- [videos](https://github.com/forktheweb/dockistry/blob/master/docs-videos.md) of ***some*** functionality
- [changelog](https://github.com/forktheweb/dockistry/blob/master/changelog.md)
- [roadmap](https://github.com/forktheweb/dockistry/blob/master/roadmap.md)

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
- databases and webservers are easy to swap in and out
- our general strategy is to always provide some sort of web-based admin for the database
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
  
## other components
   * master registry [categories](https://labs.stackfork.com:2003/explore/groups) | [activity]()
   * [all components](https://github.com/forktheweb/dockistry/blob/master/docs-componentry.md)
   * [frameworks](https://github.com/forktheweb/dockistry/blob/master/docs-frameworks.md) 
   * [supported languages](https://github.com/forktheweb/dockistry/blob/master/docs-languages.md)
   * developer [CLI(s)](https://github.com/forktheweb/dockistry/blob/master/dockistry-cli.md) | [experimental CLI(s)](https://github.com/forktheweb/dockistry/blob/master/docs-experimental-cli.md)
   * [infrastructure](https://github.com/forktheweb/dockistry/blob/master/docs-infrastructure-packages.md) for setting up a hosting cluster on AWS/Google clouds
   * [databases & stores](https://github.com/forktheweb/dockistry/blob/master/docs-database.md)

## t.o.c.
- [dockistry home](https://github.com/forktheweb/dockistry)
- [why use dockistry?](https://github.com/forktheweb/dockistry/blob/master/docs-why.use.this.md)
- [what do we mean by fullstack strategy?](https://github.com/forktheweb/dockistry#what-is-a-fullstack-strategy)
- [author info](https://labs.stackfork.com:2003/dockistry-contributors/cho)
- [preface to dockistry](https://github.com/forktheweb/dockistry/blob/master/docs-preface.md) 
- [videos](https://github.com/forktheweb/dockistry/blob/master/docs-videos.md) of ***some*** functionality
- [changelog](https://github.com/forktheweb/dockistry/blob/master/changelog.md)
- [roadmap](https://github.com/forktheweb/dockistry/blob/master/roadmap.md)
