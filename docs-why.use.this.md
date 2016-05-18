	     ||`           '||               ||                  
	     ||             ||     ''        ||                  
	 .|''|| .|''|,.|'', || //` || (''''''||'' '||''|'||  ||` 
	 ||  || ||  ||||    ||<<   ||  `'')  ||    ||    `|..||  
	 `|..||.`|..|'`|..'.|| \\..||.`...'  `|..'.||.       ||  
	                                                  ,  |'  
	 ~ Fullstack strategies by forking pterodactyls    ''              

 
# why use dockistry? 
> "It is not our intention to create (yet another) package manager."

- The developers of Dockistry have created it for developing websites and mobile apps using a technology.
- We use tons of web components, CDNjs packages, SVG tools, and lots of other shiny web things.  

It's because of the ***overwhelming*** amount of fullstack customization options currently available, that we identified a clear need for devtools & stack management software that is focused on strategy management and setup.  More info on that [here](https://github.com/dockistry/devtools-multi-clis).

# instant infrastructure
Use Dockistry to instantly create the infrastructure necessary to operate any web development shop, freelancer, or software firm's baseline.  Here's what's included:

- Setup Rancher as a master instance using our AMI/Kube/Droplet
- Pre-configured deployment of Gitlab CE, Rancher, Discourse, Rocketchat-Hubot, Private Registries (Dockers/ NPMs), a Wekan board and other nifty stuff
- Optionally pre-load test frameworks for React, Aurelia, Wordpress, Angular, and Feathers and build/deploy them on your test environments by using our boilerplates
- Our Go CLI can build test stacks for a variety of strategies in a single process
- The build process is entirely customizable via the dockistry-yml file, and the other configs in the repository.
- You can easily fork a repository to make minor modifications for your deployment

# stack info
- docker-composed stacks for production
- automated devtools installs for local testing
- all dockistry strategies are contained in forkable repositories.  
- we encourage forking and contributing 
- extremely simple setup and default-secure
- unit-tested  
 
# technical overview
- base installation includes access to our master registry, which can be easily cloned locally to "shop" strategies
- each strategy is easy to fork and modify, and we use many existing technologies to accomplish this
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

#### built specifically for fullstack
Dockistry was started on AWS by a [devops guru](https://labs.stackfork.com:2003/dockistry-contributors/cho) with over 15 years of experience building multi-platform software.

# approach
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
