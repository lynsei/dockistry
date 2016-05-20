	     ||`           '||               ||                  
	     ||             ||     ''        ||                  
	 .|''|| .|''|,.|'', || //` || (''''''||'' '||''|'||  ||` 
	 ||  || ||  ||||    ||<<   ||  `'')  ||    ||    `|..||  
	 `|..||.`|..|'`|..'.|| \\..||.`...'  `|..'.||.       ||  
	                                                  ,  |'  
	 ~ Fullstack strategies by forking pterodactyls    ''              

## t.o.c.
- [dockistry home](https://github.com/forktheweb/dockistry)
- [why use dockistry?](https://github.com/forktheweb/dockistry/blob/master/docs-why.use.this.md)
- [what do we mean by fullstack strategy?](https://github.com/forktheweb/dockistry#what-is-a-fullstack-strategy)
- [author info](https://labs.stackfork.com:2003/dockistry-contributors/cho)
- [preface to dockistry](https://github.com/forktheweb/dockistry/blob/master/docs-preface.md) 
- [videos](https://github.com/forktheweb/dockistry/blob/master/docs-videos.md) of ***some*** functionality
- [changelog](https://github.com/forktheweb/dockistry/blob/master/changelog.md)
- [roadmap](https://github.com/forktheweb/dockistry/blob/master/roadmap.md)

 
# why use dockistry? 
> "It is not our intention to create another tool or package manager, but rather... we intend to create a strategy engine and a community that contributes to it."

Dockistry was created specifically for developing and deploying fullstack solutions for:
- websites and web-apps
- mobile apps for iOS, Android, and Windows 
- desktop software for Linux, Darwin, and Windows

For each fullstack 'strategy' we require:
- a single code base for 'end to end' (E2E) development 
- unit-testing and multi-platform devtools architectures
- continuous integration and delivery support
- horizontal scalability 

Dockistry organizes [web components](https://github.com/forktheweb/dockistry/blob/master/docs-componentry.md),  [frameworks](https://github.com/forktheweb/dockistry/blob/master/docs-frameworks.md), [databases](https://github.com/forktheweb/dockistry/blob/master/docs-database.md), and other [shiny-things](https://github.com/forktheweb/dockistry/blob/master/docs-infrastructure-packages.md) our experts find useful.

> Why clone hundreds of git repositories searching for an end-to-end solution?

We have done the leg-work for you.  Our stacks are composed using some of the most popular frameworks and databases, and provide boilerplates that will save you time and money on your development effort.  *Enterprise support is available*.

It's because of the ***overwhelming*** amount of fullstack customization options currently available that we identified a clear need for a more [organized approach](https://github.com/forktheweb/dockistry/blob/master/roadmap.md) paired with architecture-specific [devtools packages](https://github.com/dockistry/devtools-multi-clis), one that also provides [setup options](https://github.com/forktheweb/dockistry/blob/master/docs-infrastructure-packages.md) for production/staging infrastructure.

> Fact: Fullstack development is overwhelming. Setting up tooling & package managers is often a frustrating process.

Dockistry simplifies the [setup process](https://github.com/forktheweb/dockistry/blob/master/dockistry-cli.md) for many dev & production concerns using our [multi-platorm toolkit](https://github.com/dockistry/devtools-multi-clis) and [infrastructure  tools](https://github.com/forktheweb/dockistry/blob/master/docs-infrastructure-packages.md), packaged in one [desktop app](https://github.com/forktheweb/dockistry/blob/master/roadmap.md).


# Benefits
- Get running on a full docker-driven AWS/Google infrastructure, quickly & painlessly.
- Shed light on language, database, framework, and boilerplate combinations your team hasn't considered
- Makes you a programming rockstar, just generally speaking.  ;)
- Impress your friends/boss with your broad range of tooling knowledge 
 
## about infrastructure setup
Use Dockistry to [instantly create](https://github.com/forktheweb/dockistry/blob/master/docs-infrastructure-packages.md) the infrastructure necessary to operate any web development shop, freelancer, or software firm's baseline.  

##### Here's what's included with our basic infrastructure setup:
- Private Registry Services (optional)
    - NPM registry
    - Docker registry
    - Git registry
- SSL-secured, Docker/ Rancher driven (optional) software such as:
    - [Rancher](https://rancher.com/) with reverse-proxy for managing SSL websites and docker images
    - [Discourse](https://www.discourse.org/), a ruby-driven web forum that kicks major ass
    - [Rocketchat-Hubot](https://github.com/RocketChat/hubot-rocketchat), because who doesn't want their own robot?
    - [Wekan Board](https://github.com/wekan/wekan), to help your projects stay organized (kinda like Trello)    
    - [Gitlab CE](https://gitlab.com/) for managing your very own git repositories
- Stack development
    - Optionally pre-load test [frameworks](https://github.com/forktheweb/dockistry/blob/master/docs-frameworks.md) and boilerplates for local or production stacks
- Our Go CLI can build test stacks for a variety of strategies in a single process, automatically for you.
- You can easily fork a repository to make minor modifications for your own deployment pipeline

## about stack deployment
Dockistry offers the following features for instantaneous fullstack software installation:

- fullstacks are designed for various [frameworks](https://github.com/forktheweb/dockistry/blob/master/docs-frameworks.md), [components](https://github.com/forktheweb/dockistry/blob/master/docs-componentry.md), and [databases](https://github.com/forktheweb/dockistry/blob/master/docs-database.md).
- automated [developer tooling packages](https://github.com/forktheweb/dockistry/blob/master/roadmap.md) are made for local development on your home/ office PC
- our [curated registry](https://labs.stackfork.com:2003/explore/projects/starred) is easily cloned and it's simple to [browse](https://labs.stackfork.com:2003/explore/groups) via the desktop app
- we encourage forking and contributing to the development of stacks for various purposes, our ultimate goal is to create a community that focuses on this which will be integrated into the desktop app
- our tools are extremely simple to setup and default-secured via our desktop-app & [infrastructure](https://github.com/forktheweb/dockistry/blob/master/docs-infrastructure-packages.md).  All tools can be downloaded and installed via our primary desktop app.

> note: if you don't see anything you like, your can build your own stack solution using our directory of modular dockers and components

# techniques
- we utilize [Docker Kung-fu](https://github.com/dockistry/docker-kungfu) "infrastructure through code" throughout Dockistry
- we embrace [12-factor methods](http://12factor.net/) wherever possible in respect to the above
- 100% open source code with enterprise capabilities and support services available
 
# features 
- base installation includes access to our master registry of fullstack strategies
- each strategy is easy to fork and modify, and we use many existing technologies to accomplish this
- provides a comprehensive fullstack solution for deployment to dev/stage/prod envs.
- peer-reviewed security practices and tools for keyring & cluster-devops security are included
- a modular git-driven architecture containing many unit-tested skeletons/boilerplates
- independent of any one cloud provider or platform
- immediate deployment and configuration of many [javascript frameworks](https://github.com/forktheweb/dockistry/blob/master/docs-frameworks.md) and their associated tools
- containers designed for docker-compose 2.0 and rancher-management
- automated [infrastructure](https://github.com/forktheweb/dockistry/blob/master/docs-infrastructure-packages.md) setup
- stacks and components are provided in [categories](https://labs.stackfork.com:2003/explore/groups) for browsing outside of our desktop app
- our stacks are designed for specific purposes, i.e.- backups, utilities, web software, servers, components
- our boilerplates use the aforementioned categories and are built for specific purposes (i.e.- CRM, E-commerce, etc.)

# encryption 
- we embrace [port-80-shame](https://github.com/jimmycuadra/port-80-shame) because we believe the web should be default-secure
- we fully automate SSL installation and renewal for all containers and websites by using the Let's Encrypt CA 
- we are [well on the way](https://labs.stackfork.com:2003/dockistry/cryptodev-ephemeral-ecdh) to implementing Gnupg keyrings and validated GPG signatures into Dockistry CLI(s) using elliptical curve crypography 

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

Devops by pTero                           "an overseer of things..."
```


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

