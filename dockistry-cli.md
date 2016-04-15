# Dockistry CLI
```please note: this CLI is not publicly available yet, as it is in pre-alpha 0.5.0```

# How it works

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
We supply a docker image called forktheweb/dockistry that contains the go api, and it runs in a single step:

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

##### Why have a CLI tool written in Go using Cobra?
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
