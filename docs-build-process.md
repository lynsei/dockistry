## t.o.c.
- [dockistry home](https://github.com/forktheweb/dockistry)
- [why use dockistry?](https://github.com/forktheweb/dockistry/blob/master/docs-why.use.this.md)
- [what do we mean by fullstack strategy?](https://github.com/forktheweb/dockistry#what-is-a-fullstack-strategy)
- [author info](https://labs.stackfork.com:2003/dockistry-contributors/cho)
- [preface to dockistry](https://github.com/forktheweb/dockistry/blob/master/docs-preface.md) 
- [videos](https://github.com/forktheweb/dockistry/blob/master/docs-videos.md) of ***some*** functionality
- [changelog](https://github.com/forktheweb/dockistry/blob/master/changelog.md)
- [roadmap](https://github.com/forktheweb/dockistry/blob/master/roadmap.md)

## production builds
Our production CLI tools allow you to create Amazon AWS instances and install any of our fullstack strategies by configuring their options.
The following is the "order of operations" for how stacks are installed in production:

- sets up the git location for installing (or pass it with --gitpath)
- fetches specified repo (local/master)
- reads the following files:
    * dockistry-compose.yml - specific rules for the cli to follow
    * docker-compose.yml - docker composition 2.0
    * rancher-compose.yml - cluster setup info
- upon reading the rules, the CLI will execute the creation of the docker-compose using the install path
- volume paths not specified will prompt the user for those
- containers are brought online, as is the cluster via Rancher
- once containers are online the system executes commands based on the dockistry-compose.yml rules
   * npm installation commands
   * jspm commands
   * yo generators
   * bower commands
- afterwards the system will backup the state of the container volumes with duplicity and do a test restore


## notes
Our Dockistry YAML defines which build process to use in production environments on Amazon or Google clouds.  This is to prevent the build from trying to compile visual c++ apps, or other mobile-only or desktop-only builds that should be occurring on Darwin or Windows development environments.

#### other components
   * master registry [categories](https://labs.stackfork.com:2003/explore/groups) | [activity](https://labs.stackfork.com:2003/explore/projects/starred)
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
