# Dockistry 
> pre-alpha 0.5.0

##### Dockistry is strategy engine first and foremost, and is designed for developers. It provides a simple, one-step, elegant method to deploy complex software in cloudbased clusters and for E2E implementations (apps) using one set of YAML and our web-based editor.   

Dockistry is both an editor and a private provider for web-based git repos, docker registries, and npm registries.  When you install Dockistry for the first time, our CLI will provide installation options for deploying your own local copies of our master registries.  These registries are in pre-alpha, but are <a href="https://labs.stackfork.com:2003/">available</a> here.

Our registries contain many modular stacks that are packaged to deploy in development and production environments.  Our registry copies are ephemeral and you are not encouraged to roll out updates by destroying them and downloading new copies (much like how docker containers typically operate, only on a registry level).  

Our opensource web-based editor "stacks" these repositories by automating the creation of cloud based servers on various providers, automating the Docker-Compose process & server configurations, installing your favorite dependency tools, and then rolling out your actual software for unit-testing.  We operate Gitlab CI for test automation on various OS.

So to put it as simply as possible, Dockistry is for building Reactive apps and the infrastructure necessary for any developer or company to do that quickly and easily on any cloud hosting provider.  

Dockistry handles everything needed to run a complete E2E code pipeline
* cloud formations
* server tools 
* middleware
* frontend tools

Dockistry currently supports 
* Amazon AWS
* Google Cloud
* Docker Machine/Swarm

More support is actively being developed as we intend for this project to be fully platform agnostic, and independent of any package or depenency tools.  Instead, we try to embrace all the existing tools out there.  It is not our intention to create (yet another) package manager.

Dockistry is a comprehensive strategy engine for various types of fullstack deploys, though we use it primarily for web based apps using reactive SPA(s) over frameworks such as:

* React native
* Aurelia
* Angular
* VueJS
* Riot
* Roots

This allows you to use whatever framework you wish with hundreds of other web-based components such as:
* package managers (npm/ bower/ yeoman scaffolds/ etc.)
* webpack & polymer components
* semantic or material ui, or whatever other UI you want
* about 40 different datagrid providers (from jspreadsheets.com)
* badass devtools such as gulp, grunt, vinyl, and even editors such as vim-spf13

> dockistry is an early-stage project and has not yet been merged into this public repo.  but we are actively looking  for people who build react apps to participate by contributing their own strategies.  we do have a process and formula for how to do that, and it's entirely YAML driven using pTero and docker-compose.

## do you dislike bullshit and love pterodactyls?

If you answered yes, it's possible you too may be looking for a fullstack deploy that doesn't suck.
Perhaps we can help.

# What is Dockistry?

##### elegant forking format & kittycat simple stacking deploys
All stacks are 100% SSL-LE, Docker-composed, in modular-fork format.  You just pick the repositories you want, and use the YAML config they supply.  That means they can easily be joined together in various configs with various UI, datagrids, cdnJS, NPM, Bower, Yeoman, JSPM, Go-lang, RVM, and other dependency management tools.  No limitations on language or platform but obviously we lean towards NodeJS and Go with Citus/Postgre or Mysql/Aurora.

### Dockistry is a collection of tools and technologies that comes as a pre-packaged instance AMI/ Kubernetes stack.
- Comes pre-configured with Gitlab CE, Rancher, Discourse, Rocketchat-Hubot, Private Registries (Dockers/ NPMs), Wekan board, and we pre-load test frameworks for React, Aurelia, Wordpress, Angular, Ember and VueJS. 
- One-click setup with a very short configuration, just deploy our AMI/ Stack
- Instant setup script(s) on Amazon AWS or Google Cloud

##### Did you know that pTerodactyls can fly holding nearly 10x their wait in devops bullshit? (TRUE FACT)

##### Detailed specifications and other info:

- [frameworks](https://github.com/forktheweb/dockistry/blob/master/docks-frameworks.md) - supported reactive frameworks
- [componentry](https://github.com/forktheweb/dockistry/blob/master/docks-componentry.md) - tools we're considering supporting or ones we already are (WIP)
- [coding standards](https://github.com/forktheweb/dockistry/blob/master/docks-code.md) - our development philosophies
- [pTero devops](https://github.com/forktheweb/dockistry/blob/master/docks-ptero.md) - an example stack, but pTero is also a Go-lang shell program that does all our automation for AWS, GC, etc.
- [about](https://github.com/forktheweb/dockistry/blob/master/docks-ptero.md) - a little info about the developers

# Reactive apps
- all our stacks are docker-composed, rancher managed, single-step deployed (i.e.- aws ec2-create-instance blah)
- we support flocker and gluster for volume mounting docker containers, which is dope cause then you can shard your citus & nginx instances and horizontally scale the shit out of them
- we have several stack examples in beta including:
    * SSL Citus [Postgre] with Go Json Api paired with React App
    * SSL Rancher on Ubuntu/ROS set up with NginxProxy/LetsEncrypt
    * Wordpress with Zero PHP (i.e.- Calypso backend, Aurelia Front-end, Composer)
 - near-zero setup (it requires a TLD)
 - unit-tested

### Dockistry CLI

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
 
#### currently we support
- amazon aws [instantly cloud-formation deploy & hot-sync of data from our S3 multi-az
- google cloud [instantly deployed from gluster or s3 using convoy or duplicity]

#### soon we will provide drop-ins for
- digital ocean
- bare metal
- heroku 
- scalingo
- devo.ps

#### gitlab updates
we exclude updates from forked repos intentionally because our stacks are unit-tested and stable.  we use bleeding-edge branches to test updates on forks prior to putting them in dockistry as masters.

> important note: _this project is pre-alpha, though many modules are production tested and ready for immediate use_ 

- we are opensource 100%
- private repos for community development, so just ask to get access.
- they are private cause we think it's bad if devs are downloading our broken stuff accidentally on github
- our first published release will incorporate one master dockistry with over 60 sub-repos that will be made production/public status

# technical overview
- comprehensive fullstack solution for deployment to dev/stage/prod envs.
- peer-reviewed security practices with fullstack capabilities above and beyond those of traditional dockerhub devops images
- a modular git-driven architecture containing skeletons & deployments for many different combinations of dockerhub driven app images
- complete 12-factor support that aims to be cloud-agnostic, platform-agnostic, and licensed under an AGPL
- immediate deployment and configuration of many NodeJS driven frameworks for developers building SPA apps (i.e.- Aurelia, React, Vue)
- containers designed for deployment virtually and which are fully docker-compose 2.0 ready with side-kick support into rancher-compose
- utility containers for backup automation on any mounted image via duplicity
- powerful backup & cache systems with incrementally recognizant architecture via bup and kup
- wordpress deployment using dependency management via composer, proactive environment setup using ansible

# ssl is automated on every environment
- we embrace [port-80 shaming](https://github.com/jimmycuadra/port-80-shame) because it's fun.
- yes, we fully automate SSL deploys for you with Zero Setup using the Let's Encrypt CA (no SSL errors)
- we are on the way to implementing Gnupg keyrings and validated GPG signatures too.
- we also embrace calling out comcast for injecting javascript, an illegal practice (as seen with the recent Verizon suit)

#### security
We intend to use Ephemeral & destructive Gnupg keyrings with external etcd/ consul & watchtower support.  For security reasons, our stacks are moderately opinionated as far as the types of SSL and encryption we use and recommend, but this still leaves developers in control because we are adoptive of docker-compose, Rancher, Ubuntu, and in favor of YAML ubiquity.  We are in favor of default-secure practices and SSL by default for all environments.

#### contact us
- [![Gitter](https://badges.gitter.im/disruptiveware/dockistry.svg)](https://gitter.im/forktheweb/dockistry) 
- mention "@ptero help" if the bot is available.  the winged-beast install your oauth credentials from github and even deploy certain apps automatically based on a simple questions & a basic sms validation (no-github).
##### "Dockistry is powered by a well-read group of pterodactyl enthusiasts" 

## how to contribute
- If you wish to participate in the development effort, visit [gitter](https://gitter.im/forktheweb/dockistry).  both are very new to the community so we appreciate any smoke or sage you might have to offer.
- our pre-alpha gitlab provides a collection of packages in the form of forkable repositories designed to be docker-composed and interchanged


#### built specifically for fullstack

Started on AWS by a Devops team with 30 years combined experience

- We understand the importance of infrastructure-through-code and repeatable patterns.
- We embrace [12-factor methods](http://12factor.net/)
- 100% Afero GPL code with enterprise capabilities out-of-the-box
- We intend to offer enterprise services and world class support alongside the apps web build which utilize this platform.
- We also offer DefaultSecure Let's Encrypt on SSL via Nginx-Proxy by default (automatic for all docker 443 hosts)

 
```bash
                            <\              _
                            \\          _/{
                     _       \\       _-   -_
                   /{        / `\   _-     - -_
                 _~  =      ( @  \ -        -  -_
               _- -   ~-_   \( =\ \           -  -_
             _~  -       ~_ | 1 :\ \      _-~-_ -  -_
           _-   -          ~  |V: \ \  _-~     ~-_-  -_
        _-~   -            /  | :  \ \            ~-_- -_
     _-~    -   _.._      {   | : _-``               ~- _-_
  _-~   -__..--~    ~-_  {   : \:}
=~__.--~~              ~-_\  :  /
                           \ : /__
                          //`Y'--\\
                         <+       \\
                          \\      WWW
                          XvX

Devops by pTero                           "an overseer of things..."```
