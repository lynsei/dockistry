	     ||`           '||               ||                  
	     ||             ||     ''        ||                  
	 .|''|| .|''|,.|'', || //` || (''''''||'' '||''|'||  ||` 
	 ||  || ||  ||||    ||<<   ||  `'')  ||    ||    `|..||  
	 `|..||.`|..|'`|..'.|| \\..||.`...'  `|..'.||.       ||  
	                                                  ,  |'  
	 ~ Fullstack strategies by forking pterodactyls    ''              

 
# why use dockistry? 
> "It is not our intention to create another tool or package manager, but rather... we intend to create a strategy engine."

- The developers of Dockistry have created it for developing websites and mobile apps using various languages and tooling.
- We aggregate many web components, CDNjs packages, SVG tools, and other shiny web things to organize them better
- Github is overwhelming to many developers, and there are too many options.  Setting up devtools for them sucks.
- Dockistry can help you shop around faster and more reliably by unifying the setup for many dev, staging, and production concerns.

It's because of the ***overwhelming*** amount of fullstack customization options currently available, that we identified a clear need for devtools & stack management software that is focused on strategy management and setup.  You can read more about that  [here](https://github.com/dockistry/devtools-multi-clis).

# instant infrastructure
Use Dockistry to instantly create the infrastructure necessary to operate any web development shop, freelancer, or software firm's baseline.  Here's what's included:

- Setup Rancher as a master instance using our AMI/Kube/Droplet
- Pre-configured deployment of Gitlab CE, Rancher, Discourse, Rocketchat-Hubot, Private Registries (Dockers/ NPMs), a Wekan board and other nifty stuff
- Optionally pre-load test frameworks for React, Aurelia, Wordpress, Angular, and Feathers and build/deploy them on your test environments by using our boilerplates
- Our Go CLI can build test stacks for a variety of strategies in a single process
- The build process is entirely customizable via the dockistry-yml file, and the other configs in the repository.
- You can easily fork a repository to make minor modifications for your deployment

# instant stack deploys
Dockistry offers the following features for instantaneous fullstack software installation:

- fullstacks are designed for various [frameworks](https://github.com/forktheweb/dockistry/blob/master/docs-frameworks.md), [components](https://github.com/forktheweb/dockistry/blob/master/docs-componentry.md), and [databases](https://github.com/forktheweb/dockistry/blob/master/docs-database.md).
- automated [developer tooling packages](https://github.com/forktheweb/dockistry/blob/master/roadmap.md) are made for local development on your home/ office PC
- our [curated registry](https://labs.stackfork.com:2003/explore/projects/starred) is easily cloned and it's simple to [browse](https://labs.stackfork.com:2003/explore/groups) via the desktop app
- we encourage forking and contributing to the development of stacks for various purposes, our ultimate goal is to create a community that focuses on this which will be integrated into the desktop app
- our tools are extremely simple to setup and default-secured via our desktop-app & [infrastructure](https://github.com/forktheweb/dockistry/blob/master/docs-infrastructure-packages.md).  All tools can be downloaded and installed via our primary desktop app.

> note: if you don't see anything you like, your can build your own stack solution using our directory of modular dockers and components

# our approach
- We understand the importance of infrastructure-through-code and repeatable patterns.
- We embrace [12-factor methods](http://12factor.net/)
- 100% Afero GPL code with enterprise capabilities out-of-the-box
- We intend to offer enterprise services and world class support alongside the apps web build which utilize this platform.
- We also offer DefaultSecure Let's Encrypt on SSL via Nginx-Proxy by default (automatic for all docker 443 hosts)

# features run-down
- base installation includes access to our master registry, which can be easily cloned locally to "shop" strategies
- each strategy is easy to fork and modify, and we use many existing technologies to accomplish this
- comprehensive fullstack solution for deployment to dev/stage/prod envs.
- peer-reviewed security practices and tools for keyring & cluster-devops security are included
- a modular git-driven architecture containing skeletons/boilerplates
- 12-factor support that aims to be indpendent of any one cloud provider or platform 
- immediate deployment and configuration of many NodeJS driven [javascript frameworks](https://github.com/forktheweb/dockistry/blob/master/docs-frameworks.md)
- containers designed for docker-compose 2.0 and rancher-management, automated [infrastructure](https://github.com/forktheweb/dockistry/blob/master/docs-infrastructure-packages.md) setup
- containers for production stacks are provided in [categories](https://labs.stackfork.com:2003/explore/groups) for easy browsing/contributing
- our stacks are designed for specific purposes, i.e.- backups, utilities, web software, components

# ssl is automated on every environment
- we embrace [port-80 shaming](https://github.com/jimmycuadra/port-80-shame) because it's fun.
- yes, we fully automate SSL deploys for you with Zero Setup using the Let's Encrypt CA (no SSL errors)
- we are on the way to implementing Gnupg keyrings and validated GPG signatures too.
- we also embrace calling out comcast for injecting javascript, an illegal practice (as seen with the recent Verizon suit)

#### about the author
Dockistry was started on AWS by a [devops guru](https://labs.stackfork.com:2003/dockistry-contributors/cho) with over 15 years of experience building multi-platform software.






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
