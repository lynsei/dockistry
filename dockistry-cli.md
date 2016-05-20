## t.o.c.
- [dockistry home](https://github.com/forktheweb/dockistry)
- [why use dockistry?](https://github.com/forktheweb/dockistry/blob/master/docs-why.use.this.md)
- [what do we mean by fullstack strategy?](https://github.com/forktheweb/dockistry#what-is-a-fullstack-strategy)
- [author info](https://labs.stackfork.com:2003/dockistry-contributors/cho)
- [preface to dockistry](https://github.com/forktheweb/dockistry/blob/master/docs-preface.md) 
- [videos](https://github.com/forktheweb/dockistry/blob/master/docs-videos.md) of ***some*** functionality
- [changelog](https://github.com/forktheweb/dockistry/blob/master/changelog.md)
- [roadmap](https://github.com/forktheweb/dockistry/blob/master/roadmap.md)


# Production CLI
```please note: this CLI is not publicly available yet, as it is in pre-alpha 0.7. This page is a total work in progress, and I'm using it as a map for the development effort.```

### We have two primary types of CLI
- Production
- Developer Tools

Both are integrated into the [primary desktop app]().

Our dockistry CLI is written in Go-lang using [Spf13/Cobra](https://github.com/spf13/cobra).
It operates using the following options menu:

### AWS Production features
These are features currently in development, aggressively so:

 - configure aws credentials
 - install infrastructure packages
 - install any fullstack strategy
 - set up reverse proxy via nginx
 - set up automatic SSL provisioning for docker containers
 - set up automatic dns setup via route 53
 - set up automatic s3 backups
 - run any fullstack strategy on rancher
 - search & fork any fullstack strategy
 - operate saws command line app
 
## installation
We supply a binary that you can run from these operating systems:

### supported platforms
- aws ec2 using Ubuntu Trusty 14.4
- gcp using docker
- docker swarm

 

## usage
For first-time setup
``` ./dockistry setup ```
 
For documentation within the system shell:
``` dockistry help ```

To run the CLI executable (complete menu)
``` dockistry ```

## uninstalling
```dockistry uninstall```

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
