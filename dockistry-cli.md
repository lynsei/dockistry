# Dockistry CLI
```please note: this CLI is not publicly available yet, as it is in pre-alpha 0.5.9```

# How it works

- each stack is different, and is purposed for either development or production environments
- we have separate distributions for the CLI ops for production and development (for tuning/tooling)
- the example below is a custom tooling for Angular, RethinkDB, StrongLoopAPI, StrongLoop Arc, and Restangular
- it allows the developer to choose from multiple themes including blur-admin, material, and semantic-ui
- it runs on local domains using .dev extensions using hotel

### Example stack using developer tooling:
Sometimes the best way to understand what a thing does, is to watch a quick video.  Just keep in mind that this is a very specific stack example, and we have many different stacks and many configurable options within them:

> Watch the [video screencast](http://screencast-o-matic.com/watch/cDf0fO1GWx) (don't worry it's only like 99 seconds long!)

#### Short version:

<img src="http://pterops.com.s3.amazonaws.com/cli-devtools-powershell-windows.gif" width="100%" alt="Windows Developer Tooling" />

### How the CLI distribution works:

Our dockistry CLI is written in Go-lang using [Spf13/Cobra](https://github.com/spf13/cobra).
It operates using the following options menu:

 - tools (on host, or ignore and use docker attachment layers)
    * management tools
    * rancher
    * docker tools
    * update registries
    * npm & jspm
    * saws
    * kubernetes
 - search
    * search npm
    * search dockerhub
    * search jspm
    * search bower
    * search yeoman generators
    * search cdnjs
 - install stack
    * autocompletes 
      - devstack-*
      - prodstack-*
      - forkme-*
    * search instances (pre-created)
 - deploy stack
 - test stack
 - configure system
    * backups via duplicity
    * database hot backups using bup
    * webterm & editor URL config
    
## installing
We supply a docker image that makes installation very easy:

##### first make the install path:
``` mkdir -p /usr/local/dockistry; cd /usr/local/dockistry ```

##### then run the docker image
``` docker run -it ./:/usr/src/dockistry forktheweb/dockistry ```


## usage
For first-time setup
``` dockistry setup ```
 
For documentation within the system shell:
``` dockistry help ```

To run the CLI executable (complete menu)
``` dockistry ```

## uninstalling
```docker rm forktheweb/dockistry```

## what setup does
Once the Go binary is installed, run the setup command and you will be asked a few questions about what you are using dockistry to do.
Based on those questions, the CLI will install a variety of things or store your configuration for future reference.  
- builds/restores registries from our master
- can create new server instances for:
   * rancher master (it's good to keep this separate)
   * worker instance
   * infrastructure instance (developer tooling, rocketchat, hubot, gitlab, backups etc.)
   * gluster filesystem mounts
   * private registries
- optionally, it can do all of the creations above locally too. (see size recommendations)
- configure backup locations (i.e.- on S3 or locally)
- configure smtp settings
- configure primary let's encrypt e-mail and primary devops url (used to create reverse-proxies over SSL)

## what build or deploying repos does
- sets up the git location for installing (or pass it with --gitpath)
- fetches specified repo (local/master)
- reads the following files:
    * dockistry-compose.yml - specific rules for the cli to follow
    * docker-compose.yml - docker composition 2.0
    * rancher-compose.yml - cluster setup info
- upon reading the rules, the CLI will execute the creation of the docker-compose using the install path
- volume paths not specified will prompt the user for those
- containers are brought online, as is the cluster
- once containers are online the system executes commands based on the dockistry-compose.yml rules
   * npm installation commands
   * jspm commands
   * yo generators
   * bower commands
- afterwards the system will backup the state of the container volumes with duplicity and do a test restore

##### why we built things this way (Go/Cobra/Docker/Rancher/etc)
 - works on any platform because it's a compiled app
 - we use a webterm so you can perform operations via the web if needed (along with the editor)
 - installs all your local registries
 - stores your favorite commands in a local (or remotely stored) Etcd container (handy! for shell commands)
 - sets up backups with duplicty & bup for all of your volume mounts on s3 or other provider(s)
 - sets up crontab(s) depending on your needs
 - validates backup checksums for incrementally stored database and filesystem backups
 - installs gitlab ce, dockistry, rocketchat-hubot, reverse proxy with automated ssl
 - installs rancher on a separate management instance or locally (over ssl)
 - destroys and creates git, docker, and npm repostiories locally
 - create new container services via rancher api or docker-compose & registries you specify

##### What does the CLI *not* do
 - manage the docker containers (we feel Rancher does this amazingly well and so do not provide that)
 - manage registry data (they are disposable anyway, don't repair them, just copy from our master back down)
 - manage docker container volume data (only backups & initial setup of new containers)
