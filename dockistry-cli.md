# Dockistry CLI

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
 
# How it works

Our dockistry CLI is written in Go-lang using [Spf13/Cobra](https://github.com/spf13/cobra).
It operates using the following order of operations:
 - installations (on host, or ignore and use docker attachment layers)
    * management tools
    * rancher
    * docker
    * npm & jspm
 - search repo
    * search npm
    * search dockerhub
    * search jspm
    * search bower
    * search yeoman generators
    * search cdnjs
  - install dockistry repo
    * autocompletes 
      - devstack-*
      - prodstack-*
      - forkme-*
    
