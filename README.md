# Dockistry 
> "offering modular stack strategies powered by caffeine and forking pterodactyls"

##### status / ~pre-alpha 0.5.0 / [gitlab-ce](https://labs.stackfork.com:2003/?) / author: CDH / date 04-15-2016

## introduction
Every developer uses different tooling, environments, and every project use different dependencies and package management tools, scaffolds, and testing/monitoring tools.

Have you ever desired to unify those considerations into singular format so that your favorite environment setup for development and production can be distributed and stablized for mass consumption?  

It's under that premise that Dockistry has been invented.  If you answered yes, then read on friend...

### Dockistry is a "strategy engine"  
##### 100% comprehensive, Platform Agnostic, AGPL, community-driven.

Dockistry empowers developers to quickly implement expert strategies from a centralized repository that is curated.   Each strategy is created by expert developers to serve a very specific purpose.   The developers of Dockistry build web apps that use Electron, so that's been our focus.  We've incorporated many framework & stack options that we find useful in our repo (over 10 baselines and 300 forks, with thousands of possible combinations).

The repositories we host utilize a compose process that is 100% YAML driven for the stack, but applications within it are volume mounted in their filesystem using Aufs/Docker on the host.  We believe this to be the best scenario for backups and storage, because the containers are fully disposable, but the host data is easily backed-up without messing around inside each container.  It also means that since these volumes are available after they are composed on the host container, our CLI can finish the compose process by executing all sorts of package managers and other tasks to set up tooling properly.

We offer AMI/Kubernetes images for quickly deploying 100% bullet-proof cloud-init based formations, in the event you run into any trouble with our CLI composing your management tools, developer stacks, private registries, or anything else.

# Why Dockistry?
##### Well, our belief is that: 
> **There are currently too many projects focused on tooling being provided in communities like GitHub, and not enough focus on providing stable Continuous Delivery Strategies.**  

So because of that, Dockistry focuses **only** on the big picture & elegant simplicity.  We operate containers as a service (CaaS) via a  **platform agnostic** tooling kit over existing technologies only, and using a powerful CLI that works on any cloud provider as a compiled binary.  

# Examples
> **example #1:**  You might have a strategy for a single page application (SPA) that builds out your mobile app via Cordova/Phonegap variations and using an Amazon Code Pipeline with Gulp compiler process housed on Docker and served by HHVM with Citus or MongoDB.  That's complex and the stack is far different if it's to be production-ready.

> **example #2:** That would be far different from the tooling used on a performance tuned API stack written on the NodeJS API or using something like Goat/ Gorilla on a GVM powered stack running Go-lang 1.4.  If we are using this stack for testing or development, we might use something like Ansible or Vagrant to configure our stack with the right tools and this can be done inside the stack repository (strategy).  

For every development or production use case, there are considerations and almost certainly caveats, especially when executing a comprehensive E2E strategy with a code-pipeline and multiple collaborating developers.

> Each stack you compose using the Dockistry CLI will operate to serve the needs of a particular strategy for   development or production (or both).  All repos are prefixed with "dev, prod, or fork" to make that clear.  So if we are creating a stack that focuses on wordpress theme development, it will contain no performance tuning, but it will contain a ton of developer tools like vim-spf13, samson, c++ nodegyp, and it will be called something like "devstack-wp-cplus".

Simple installation for our tools:
* download CLI from our dockerhub image
* run ``` dockistry setup ```

That's pretty much it, then just run:
``` dockistry make /location/of/dockistry-compose.yml  ```

``` pTero devops ``` handes everything from there through Rancher, Docker-Compose, and using a variety of tooling set up commands like npm, bower, and anything else existing in the mount yml.  This allows for a full stack to be created along with load balancing, clustering, and everything else necessary to operate both development and production stacks using the repositories we host.  

The dockistry YAML rules provide a roadmap for the system to follow when installing repositories, which allows it to dynamically update the docker-compose container attachments & paths.  It then passes all of that info to the Rancher API and builds the cluster so it will appear in there all nicely!

Because we install a webterm and editor on your specified URL (over SSL proxy), you can use that as a management tool too.
It allows for browsing and composing our repos, and configuring the stacks using the dockistry, docker, and rancher compose yaml, along with other yaml directives for npm, bower, yeoman, and more.

# No Wheel Re-inventing
We use *only* existing tools for stack setup, such as NPM for depenencies, and/or systems such as Bower, scaffolds such as Yeoman, and Go-lang tools.  Docker stacks are composed to avoid custom Makefiles and custom Dockerfiles (ideally), this allows everything to be executed as a single process that is easy to review and organize in our YAML editor.  It's not *always* possible to do that (for certain compilation processes, for example), but we avoid Dockerfiles, Makefiles, and scripted shell commands whenever possible, and avoid JSON in favor of YAML whenever possible (we convert it on deploy for most configurations).

##### Strategy storage
We expect and encourage you to have your own strategies, and if they are working well for you, please contribute them to our StackFork master repo because the idea here is to implement strategy recommendations from developers all over the world.  Each developer has different goals and backgrounds, so we are certain to see a plethora of interesting use cases and tooling setups.  Our hope is to drive innovation in these areas, especially in the usage of of React/Aurelia SPA(s), datagrids, and componentry.

##### Master repo
One of our primary goals is to organize our "StackFork" master repository in such a way that it can be used as by anyone without making it complicated and confusing (and that's not easy).  This will allow developers to turn to Dockistry to allow them to switch strategy easily when new sets of tools come out without spending unnecessary time on configurations and tooling, and that includes use cases for tools like compass/phonegap or even Java operations like Gradle. 

The configuration and usage of tools like Atom or VIM can take *days*, so it is our goal to really remove that as a boundary because you know each time you download one of our stacks, it's been created by an expert in their respective field and curated through our peer review process.  We do not want our repository to operate like NPM (tons of dead and useless  projects).

##### E2E and Continuous Delivery focused
Using our registries as a playbook, and through using YAML, you can quickly create virtually any kind of relevant react application or API, go-lang app, or even an ethereum blockchain app.  

"Strategies" can include virtually anything that would need to live on an AWS or Google Cloud that horizontally scales:
* cloud instances/ environments
* servers/ backends
* middleware/ tasks
* uix/ componentry
* cli tools and editors

# Deploy clusters in a single step
Dockistry provides a simple, one-step, elegant method to deploy complex software in cloudbased clusters and for E2E implementations (apps) using one set of YAML and our web-based editor.  The only pre-requisite is a domain name that will be set up by our CLI (you will need to point the A record, or have the CLI do it via route53 automatically).

Dockistry is both an editor and a private provider for web-based git repos, docker registries, and npm registries.  When you install Dockistry for the first time, our CLI will provide installation options for deploying your own local copies of our master registries. 

These registries are in pre-alpha, but are <a href="https://labs.stackfork.com:2003/">available</a> here on request for those wishing to contribute.  

Our master contains many modular stacks that are packaged to deploy in development and production environments.  Your registry copies are ephemeral and you are encouraged to roll out updates by destroying them and downloading new copies with the CLI tools we provide.

The [Dockistry CLI](docs-cli.md) sets you up (optionally) with a full-on infrastructure using the AWS and Google SDK via pTero devops.
* gitlab ce installation and config over ssl on sub-domain
* rancher master/slave
* rocketchat and hubot instance
* nginx reverse proxy
* ssl fully automated 
* gnupg keyrings

Our open source web-based editor allows you to stack these repositories by automating the creation of cloud based servers on various providers, automating the Docker-Compose/ Rancher process & server configurations, installing your favorite dependency tools, and then rolling out your actual software for unit-testing.  We operate Gitlab CI for test automation on various OS.

**To put it as simply as possible:**

Dockistry is for building Reactive apps and the infrastructure necessary for any developer or company to do that quickly and easily on any cloud hosting provider.  


Dockistry currently supports these hosts:
* Amazon AWS
* Google Cloud
* Docker Machine/Swarm

We intend for this project to be fully platform agnostic upon launching the 1.0 version (Stable), but the beta versions are specific to AWS and Kubernetes environment setups. 

#### "It is not our intention to create (yet another) package manager."

### Primary use case
The developers of Dockistry have primarily used it for E2E websites and mobile apps using Javascript with React-style  frameworks and NodeJS.  We use tons of web components, CDNjs packages, SVG tools, and lots of other shiny web things.  It's because of the magpie-esque tooling considerations and overwhelming amount of customization options, that we identified this clear need for a strategic, focused, and comprehensive management system using existing tooling. 

> We intend to incorporate stacks in our repo that use the following types of React frameworks:

* React native
* Aurelia
* Angular
* VueJS
* Riot
* Roots

**When combining the above frameworks with baseline stacks, you can have hundreds of tooling considerations and variants:**

* package managers (npm/ bower/ yeoman scaffolds/ etc.)
* webpack & polymer components
* ui toolkits such as material-ui, angular-material, semantic ui, uikit
* there are nearly 40 different datagrid providers 
* editors are also available such as vim-spf13 and even SAWS (docker-composed)

> Dockistry code is stored on StackFork while we are in a pre-alpha stage, as we do not want people executing processes that may harm their servers or development environments.  

### Looking for contributors!
We are actively looking for developers to participate by contributing their own strategies (even portions of them that they are most familiar with).  Our devteam is super friendly, and we are available easily via Gitter.
 
# deploys

##### elegant forking & kitty-cat-simple stacking deploys
All stacks are 100% SSL-LE, Docker-composed, in modular-fork format.  You just pick the repositories you want, and use the YAML config they supply.  That means they can easily be joined together in various configs with various UI, datagrids, cdnJS, NPM, Bower, Yeoman, JSPM, Go-lang, RVM, and other dependency management tools. 

No limitations on language or platform but obviously we lean towards NodeJS and Go with Citus/Postgre or Mysql/Aurora.

# instances
Dockistry can build rock solid instances from the CLI automatically for Amazon AMI or Google Kubernetes hosts and using existing technology for HHVM/Paravirtual virtual servers that is very simple and elegant.  This allows you to install a full stack with tons of features without having to configure anything.

# infrastructure
We hope to make many people have an easier time setting up their programming tooling and infrastructure by using Dockistry Strategies including our tooling/ infrastructure options:

- Setup Rancher as a master instance using our AMI/Kube/Droplet
- Pre-configured deployment of Gitlab CE, Rancher, Discourse, Rocketchat-Hubot, Private Registries (Dockers/ NPMs), Wekan board and others
- Optionally pre-load test frameworks for React, Aurelia, Wordpress, Angular, and Feathers and build/deploy them on your test environments
- Our Go CLI can build test stacks for a variety of strategies in a single process
- The build process is entirely customizable via the dockistry-yml file, and the other configs in the repository.
- You can easily fork a repository to make minor modifications for your deployment

# specifications

- [frameworks](https://github.com/forktheweb/dockistry/blob/master/docks-frameworks.md) - supported reactive frameworks
- [componentry](https://github.com/forktheweb/dockistry/blob/master/docks-componentry.md) - tools we're considering supporting or ones we already are (WIP)
- [coding standards](https://github.com/forktheweb/dockistry/blob/master/docks-code.md) - our development philosophies
- [pTero devops](https://github.com/forktheweb/dockistry/blob/master/docks-ptero.md) - an example stack, but pTero is also a Go-lang shell program that does all our automation for AWS, GC, etc.
- [about](https://github.com/forktheweb/dockistry/blob/master/docks-ptero.md) - a little info about the developers

# stack info
- docker-composed, rancher managed, single-step builds
- all dockistry strategies are contained in forkable repositories.  
- we encourage forking and modification where necessary.
- there are many stack repos we house, but here are some examples:
    * SSL Citus [Postgre] with Go Json Api paired with React App (clustered and rancher manged)
    * SSL Rancher on Ubuntu/ROS set up with NginxProxy/LetsEncrypt (built to manage other hosts)
    * Wordpress with Zero PHP (i.e.- Calypso backend, Aurelia Front-end, Composer for deps, in a docker container group)
 - near-zero setup for most repos (some will require a top-level domain to be registered or added manually)
 - unit-tested (not all repos require unit testing, such as performance-tuned prod envs)

# scaling 
We love the ability to scale, and that's why we prefer to use postgre with citus, or mongo/rethink when creating projects that need scaling built right in.  

Rancher compositional YAML configures automatic container-scaling based on the settings of the health check and memory.  If you need the instances to scale based on alarms/monitoring that is a bit more complex, but can be done using the auto-scaling features of Cloudwatch for instance (with AWS).  Typically you won't run into this problem given enough swap space unless you are expecting to hit the front page of reddit, but it's nice to think about in advance of the scenario actually happening.

Another great option is to run the database instance on an entirely separate worker node, and run all containers externally.  Or you could use something like Mysql on Aurora if you are really wanting to pay a lot of money & get very improved speed.

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
