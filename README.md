 *** note: this is an early-stage project and has not yet been merged into this public repo.  but we are actively looking for people who build react apps on various platorms and frameworks to participate by contributing their own config repos (docker-composed 2.0).

> Dockistry provides a platform agnostic, fullstack deployment solution for web based apps and apis using 12-factor, Reactology, and Continuous Integration (SOA).  

### modular and no-bullshit
All stacks are 100% SSL-LE, Docker-composed, in modular-fork format.  You just pick the repositories you want, and use the YAML config they supply.  That means they can easily be joined together in various configs with various UI, datagrids, cdnJS, NPM, Bower, Yeoman, JSPM, Go-lang, RVM, and other dependency management tools.  No limitations on language or platform but obviously we lean towards NodeJS and Go with Citus/Postgre or Mysql/Aurora.


# about
### Dockistry is a collection of tools and technologies that comes as a pre-packaged instance AMI/ Kubernetes stack.
- Comes pre-configured with Gitlab CE, Rancher, Discourse, Rocketchat-Hubot, Private Registries (Dockers/ NPMs), Wekan board, and we pre-load test frameworks for React, Aurelia, Wordpress, Angular, Ember and VueJS. 
- One-click setup with a very short configuration, just deploy our AMI/ Stack
- Instant setup script(s) on Amazon AWS or Google Cloud

## do you hate bullshit and love pterodactyls?

If you answered yes, it's possible you too may be looking for a fullstack deploy that doesn't suck.
Perhaps we can help.

### we focus on reactive apps
- all our stacks are docker-composed, rancher managed, single-step deployed (i.e.- aws ec2-create-instance blah)
- we support flocker and gluster for volume mounting docker containers, which is dope cause then you can shard your citus & nginx instances and horizontally scale the shit out of them
- we have several cloud formation examples including:
    * SSL Citus [Postgre] with Go Json Api paired with React App
    * SSL Rancher on Ubuntu/ROS set up with NginxProxy/LetsEncrypt
    * Wordpress with Zero PHP (i.e.- Calypso backend, Aurelia Front-end, Composer)
 - nearly zero setup api
 - unit-tested

### we are building an editor
 - we are currently developing a web-terminal that allows YAML development for our stacks
 - it allows you to manage the entire stack as YAML (including all the front-end and middleware stuff)

#### currently we support
- amazon aws [instantly cloud-formation deploy & hot-sync of data from our S3 multi-az
- google cloud [instantly deployed from gluster or s3 using convoy or duplicity]

#### soon we will provide drop-ins for
- digital ocean
- bare metal
- heroku 
- scalingo
- devo.ps

#### how we manage gitlab updates
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
- we embrace port 80 shaming.  "america... fuck yeah!".  [contact us](https://gitter.im/forktheweb/dockistry) here if you need us to brighten someone's day.
- yes, we do this for developer environments automatically too
- immediately deploy our unit-tested, validated configurations via a private ECR
- we also offer a private registry for nodejs packages called sinopia

- we also embrace calling out comcast for injecting javascript, an illegal practice (as seen with the recent Verizon suit)

#### security
We use Ephemeral & destructive Gnupg keyrings with external etcd/ consul & watchtower support. Moderately opinionated, but adoptive of docker-compose, Rancher, Ubuntu, and in favor of YAML ubiquity.

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
