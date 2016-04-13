 *** note: this is an early-stage project and has not yet been merged into this public repo.  but we are actively looking for people who build react apps on various platorms and frameworks to participate by contributing their own config repos.

> Dockistry provides a platform agnostic, fullstack deployment solution for web based apps and apis


# about
### Dockistry is a collection of tools and technologies that comes as a pre-packaged instance AMI/ Kubernetes stack.
- Comes pre-configured with Gitlab CE, Rancher, Discourse, Rocketchat-Hubot, Private Registries (Dockers/ NPMs), Wekan board, and we pre-load test frameworks for React, Aurelia, Wordpress, Angular, Ember and VueJS. 
- One-click setup with a very short configuration, just deploy our AMI/ Stack
- Instant setup script(s) on Amazon AWS or Google Cloud

# stacks for reactive apps
- all our stacks are docker-composed, rancher managed
- we support flocker and gluster for volume mounting docker container to the host
- we have several cloud formation examples including:
    * SSL Citus [Postgre] with Go Json Api paired with React App
    * SSL Rancher on Ubuntu/ROS set up with NginxProxy/LetsEncrypt
    * Wordpress with Zero PHP (i.e.- Calypso backend, Aurelia Front-end, Composer)
 - nearly zero setup api
 - unit-tested

# currently we support
- amazon aws [instantly cloud-formation deploy & hot-sync of data from our S3 multi-az
- google cloud [instantly deployed from gluster or s3 using convoy or duplicity]

# soon we will provide drop-ins for
- digital ocean
- bare metal
- heroku 
- scalingo
- devo.ps

# updates
- we push updates to our repoistories automatically
- git updates are *not* pushed to your test sites automatically

# want access? 

> important note: _this project is pre-alpha, though many modules are production tested and ready for immediate use_ 

- we currently are offering private repos for community development, so just ask to get access.
- interested in participating:__
[![Gitter](https://badges.gitter.im/disruptiveware/dockistry.svg)](https://gitter.im/disruptiveware/dockistry?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge) is the best way to reach us, as it filters directly into our internal Rocket webRTC and Xampp set-ups.
- mention "@ptero help" if the bot is available.  the winged-beast install your oauth credentials from github and even deploy certain apps automatically based on a simple questions & a basic sms validation (no-github).

# pre-alpha gitlab
- provides a collection of packages in the form of forkable repositories designed to be docker-composed and interchanged

# participate
- If you wish to participate in the development effort, visit [gitter]().  both are very new to the community so we appreciate any smoke or sage you might have to offer.

# features from "go"
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
- we embrace port 80 shaming.  "america... fuck yeah!".  [contact us]() here if you need us to brighten someone's day.
- yes, we do this for developer environments automatically too
- immediately deploy our unit-tested, validated configurations via a private ECR
- we also offer a private registry for nodejs packages called sinopia

- we also embrace calling out comcast for injecting javascript, an illegal practice (as seen with the recent Verizon suit)

# security
Ephemeral & destructive Gnupg keyrings with external etcd/ consul & watchtower support. Moderately opinionated, but adoptive of docker-compose, Rancher, Ubuntu, and in favor of YAML ubiquity.
provided by a well-read group of pterodactyl enthusiasts" 


#### built specifically for fullstack

Started on AWS by a Devops team with 30 years combined experience

- We understand the importance of infrastructure-through-code and repeatable patterns.
- We embrace [12-factor methods](http://12factor.net/)
- 100% Afero GPL code with enterprise capabilities out-of-the-box
- We intend to offer enterprise services and world class support alongside the apps web build which utilize this platform.
- We also offer best-in-class encryption & compliance for HIPAA, HITECH, and GLBA.

 
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
