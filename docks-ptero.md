> ** original concept document for forktheweb/pTero
> example terminal output:

```bash
genus:go:crypto:cli > capscicum-based tokens are now available.
-> Armor M3 Hash > type: 'inv' to validate the DEV_REX_SRC HASHED_SECURITY_CHKSUM or saws to enter aws mode
  
 ~ # ptero
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
                          
Objectcode pTero                           "an overseer of things..."
[pre-alpha 0.2.0.1]
```

# pTero automation
> killer software and entertaining devOps solutions that are highly-opinionated&trade;

welcome to devops: a science we bring to life featuring the form of a large watchful pTerodactyl.  
our benevolent overseer.

## this powerful winged beast exists:
* FULL WORDPRESS INTEGRATION 
* 110% API driven
* Postgre, Mysql, Redis, Elasticache, Memcached, and many other awesome tech
* Rad webservices including HHVM and PHP7 using Nginx
* Automated SSL provisioning and only basic domain information needed
* Automatic Route 53 domain setup, optional S3 backups, and RDS/Aurora provisioning for External production databases
* Stellar testing tools for your hipster design crew

> Optionally deploy "Calypso" and "Rocket Chat" with meteor/mongodb; 
>... but only if the pterodactyl gets to EAT YOUR HIPSTERS afterwards.


You see, the Internet is serious business.  

We are nearly finished building a "go-lang, cobra-driven CLI wrapper" that allows for:

* sophisticated, opinionated dependency management 
* strategic end-to-end solutions for unit-testing and mobile apps
* a list of our favorite BigBoy View Kits, UI Kits, and componentry
* all your favorite node.js tools except the ones that suck

> It's one badass flying beast!

## why?
> everyone needs a truly end-to-end solution for web, mobile, desktop apps with npm/jspm compatibility

- a full-feature set is needed for JSON on both the client and server side
- a full-stack approach rife with good technology, using clean and elegant code (think Ruby or Lumen/Artisan code)

> nobody can ever argue they don't need more ptero/dactyl in their lives


> ** this project is in pre-alpha as of 3/13/2016.  it will be supported by 3/20.
> ** author:  @disruptive on freenode https://chat.echoplex.us/irc:irc.freenode.com#go-nuts

# allwedoisfork.com
- full stack compositional tools built with docker compose, npm, jspm, bower, grunt, &amp; gulp on various os'
- full wordpress integration via a custom json api written and integrated as a plugin (Genus)
- granular configuration file in YML using Roots
- embraces reactive methodology for SPA, and YML/JS-API server side "clean" configurations
- fully embraces docker-compose methodology

## operating systems
- ubuntu trusty 
- debian jessie
- centos 6

## key features
- designed as an opinionated full stack for php devlopers, go lang developers, and jscript/typescript developers 
- embraces API(s) for EVERYTHING
- wordpress managment through calypso clone (optional)
- wordpress json api support (not used by default)
- custom "genus" api we have developed that uses a plugin to attach itself to custom post types
- custom plugin called "raptor" that acts as a flat-file independent caching layer for storage on s3
- incremental backups allow high-speed cache pre-loading
- bedrock/ sage style theme with gulp/grunt task running 
- webpack / browserify support based on your UI choice and framework choice

## mandated systems for this repository
#### nginx reverse-proxy
- jwilder/reverse-proxy
- nginx-proxy-companion

#### mandated software
- wordpress installation a cached filesystem layer @ port 80:443 virtual port 5051
- hhvm or php7 with optional laravel/postgre driven api or consul driven api
- npm with private repository support
- git support with private repository using FoxLab (included)
- grunt and gulp installed task runners
- mocha, chai, karma support
- typescript + babel support
- go lang custom CLI with development tools

#### devops mandates
- pTero operations provisioning (YML driven mini-toolkit for AWS and Google Cloud)
- pTero wordpress provisioning via RDS/Aurora or using localized mysqlTuner
- S3 data sync for automated backup provisioning
- RDS/Aurora provisioning and automatic wp-optimzations, JSON optimizations
- 
#### optional mini-frameworks
- roots.cx or expressjs 
- coffee + watcher
- xtag

## opinionated code!
> everyone else appears to be ignoring the big green elephant in the room (except transpose! haha ... ew evernote joke!)
- people need to manage large-scale wordpress plugins deployments and licensing effectively 
- we know what is best for you, but we give you options... like any good teacher;  but beware the winged creatire in our midst!

### how pTero sees all
- 90% dockerization with docker-compose and YAML driven config files
- 100% through the use of JSON-API based technology.
> full stack compositional tools built with all the stuff you love and none of the crap you don't!
- docker compose, npm, jspm
- grunt, &amp; gulp
- stable linux and rdbms development environments
- enterprise production options currently include :
   * RDS Aurora InnoDB (the fastest Mysql around)
   * Elasticache
   * Elastisearch (with Algolia instant search as an option)

#### pTero does not see eye-to-eye
- We don't use ansible or vagrant or anything digital ocean provisioned, but you can if you want
- This is a platform agnostic, but we are starting testing on AWS and moving across a broad spectrum of providers
 
#### Stack UI management tools
We prefer Rancher nodes for this using a master-slave system, and offering a slew of badass features and we can help you with custom needs... just ask me.
> i.e.- this essentially would get you all the tools you need to host various devstacks using our tech, in a repeatable, cost-optimized manner on any host.   (we provide cost optimization tools as well)

#### Performance
- Both HHVM and PHP7 are fast as lightning
- All JS is bundled using browserify / webpack
- Memcached or flat file store using EFS (where available) and our custom plugin (i.e.- not w3tc cache cause it make dinosaurs cry)
- Full horizontally scalablility in production environments.
- Dev environments host everything in a single container that is designed on the fly with the tools you prefer and select from the pTero command line interface binary
- custom json api written in laravel available
- front-facing data-sync available
> (external-db or flat-files on S3/Gluster on both of the above API gateways)


### External APIs
- postgreSQL support and [HTSQL](http://htsql.org/doc/overview.html#what-is-htsql) support for mission critical views and reports that can be synced dynamically from wordpress or *any* database for that matter.  (it's all a CRUD API baby)
- granular configuration files for wordpress config, hhvm tuning, php tuning, etc... YML driven.
- external databases are very good if done right using batch syncing or versioning via flat file storage.
- if your website isn't large, you can pre-load your cache often

## operating systems options
- ubuntu trusty 
- debian jessie
- centos 6 with optional scientific support (phase 2)
- optional c++ compiler support (phase 2)

## mandated systems for this repository
#### nginx reverse-proxy
- jwilder/reverse-proxy
- nginx-proxy-companion

#### mandated software
- wordpress installation a cached filesystem layer @ port 80:443 virtual port 5051
- hhvm or php7 with optional laravel/postgre driven api or consul driven api
- npm with private repository support
- git support with private repository using FoxLab (included)
- grunt and gulp installed task runners
- mocha, chai, karma support
- typescript + babel support
- go lang custom CLI with development tools

#### devops mandates
- pTero operations provisioning (YML driven mini-toolkit for AWS and Google Cloud)
- pTero wordpress provisioning via RDS/Aurora or using localized mysqlTuner
- S3 data sync for automated backup provisioning
- RDS/Aurora provisioning and automatic wp-optimzations, JSON optimizations
- 
#### optional mini-frameworks
- roots.cx or expressjs 
- coffee + watcher
- xtag


### NPM/ JSPM Container config
> each primary configuration is based around the developer's Router/Framework choice.


#### Atom module support
* coffeesript watchers (transpile)
* watchers for taskrunning/ karma tests

### View Framework

* roots minimalist
* react (+express option)
* vue.js
* angular2
* angular1
* aurelia (+atom, +typescript)

----------------

#### ES support
* es6 support 
* es5 support via babel downgrade transpile

----------------

## Task Running
> once a primary framework and ES decision are made, the rest of the options become available.
> all of this happens in a node-jitsu style CLI that I'm custom building using go-lang + cobra.

### Components/ UI
* ui-kit 
* widget-kit
* kendo ui
* polymer components
* semantic-ui

#### Testing options
* mocha
* chai
* karma
* sentry 
* phantomjs
* gremlins tests

#### CSS pre-compilers
> i'm very opinionated about css compiling, and I'm not favorable to using
> pre-processors except for if you are stuck with them.  
* not to worry though, you can always easily modify the css.sh script in the Makefile of this app and add in the support you need

#### SASS Replacement using PostCSS style code
- this devstack features my handpicked CSS choices for pre-compilation by using Post CSS instead
  * [PreCSS](https://github.com/jonathantneal/precss)
  
> "Most people use PostCSS and don't realize it.  AutoPrefixer is actually one of those situations"

- Currently we only support two main areas, and we let the rest happen from the UI kits integration with our selected task runners.
  * [autoprefix](https://github.com/postcss/autoprefixer)
  * [lostgrids](http://peterramsing.github.io/lost/)
  

### SPA Mobile/Desktop 

> Container Attachment *Optional*

* gem support via RVM
* compass support
* cordova support/ phonegap
* electron support



## Documentation
> I'm very opinionated about documentation integration and auto-gens, and I take a minimalist approach overall:
- I prefer not to write docs in the code itself, but rather write extremely simple code that reads easily.
- I feel that developers should be planning everything *prior* to coding, by documenting first.

#### For up-front documentation I recommend:
- Install Mark Down Here chrome plugin
- 

#### JS Autogen Documentation Support:
> Container Attachment *Optional*

[http://usejsdoc.org/]

#### Optional One-Per-Host (i.e.- the host container has one of each of these as an option)
> we offer instant deployment options and price-comparison for pTero Devops tools, and everything you see here.  

- [container-management-ui](http://rancher.com/) - instant rancher deployment
- [automatic-codegen](http://usejsdoc.org/) - automatic documentation generator optionally supported in boilerplate
- [wekan-board](http://www.wekan.org/) - KanBan Board using Meteor/Electron/Wekan for your organization's projects and internal usage
- gitlab single instance automatic community edition + build runners CL
- wordpress cli installation for each site (optionally)
- each site uses SSL by default, and is instantaneously SSL provisioned via Let's Encrypt
- we utilize a top-level nginx reverse-proxy for all apps
- internal containers for hhvm, php7, json-api, etc.  all run from the same container Makefile and Docker-compose system

## Datagrids 
> options are interdependent with the View framework in this case, but we support the following:

#### Lightweight
* [aurelia-bs](http://charlespockert.github.io/aurelia-bs-grid-demo/)
* [react-data-grid(http://adazzle.github.io/react-data-grid/examples.html#/editors)
* [backgrid](http://backgridjs.com/#basic-example)
* [dynatable](https://www.dynatable.com/) 
   - dynatable is my new favorite for lightweight json/html native grids
* [embergrid](http://opensource.addepar.com/ember-table/#/overview)
 
 
## Datagrids for Enterprise SPA
> If you don't require state management or crazy features in the grids, you might not need to go this route.
> My strategy is to lazy-load enterprise grid features only on the parts of the aplication that absolutely need it.
> In my experience they are very heavy, and the cost can mostly be mitigated when dynamically loading data into an iframe.  


