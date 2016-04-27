# experimental-cli
> this is a page devoted to detailed information on our experimental CLI(s)

`please note: this project is in pre-alpha and is still a major WIP`

## New Design
Since late 2015 I've redesigned ptero several times, and now it's morphed into the backbone behind Dockistry for devOps actions.
I have really dialed in the specific functionality that I want from it at this point, which includes:

- multi-platform binary distribution using [electron-boilerplate](https://github.com/szwacz/electron-boilerplate)
- local windows and mac testing using [hotel](https://github.com/typicode/hotel) and [travis / gitlab ci runners](https://github.com/electron/electron/blob/master/docs/tutorial/testing-on-headless-ci.md)
- maintaining distributions and synchronizations for [Dockistry](https://github.com/forktheweb/dockistry)



# Dockistry Experimental CLI

##### Below is the CLI Dashboard I'm playing around with in a Windows powershell


   * private, syncronizable, searchable registries
      * docker imagefile registry
      * npm package registry
      * git repository 
   * infrastructure setup for our baselines
      * AMI Image or Google Cloud distributions
      * Node driven installations
   * developer tooling for windows and linux
      * windows powershell
      * ubuntu docker stacks
      * rancher management tools
      * dockistry automation
   * web SPA for deploying stack strategies
   * production tooling
	   * volume management and docker image management via
	      * sen docker management cli
	      * samson build server
	      * rancher front-end
	   * continuous delivery setups
	      * backup setups via duplicity and s3/flocker/efs
	      * bot tie-ins and configurations
	      * auto-scaling groups based on CPU/memory for AWS/GCVM instances
	   * e2e tooling
		   * unit testing automation
       * monitoring via headless (phantomJS, Sentry, Mocha/Chai, External Heroku Buildpacks specifically for monitors.. that's all Heroku Dynos are really good for anyway lol)
		   * task runners for CI (i.e.- travis)



--------

![ec2-images-dockistry](http://pterops.com.s3.amazonaws.com/screen-dockistry/dockistry-cli-sample.gif)

 
# pTero
"**P**ortable **T**echnology **E**ngine for **R**eactive **O**perations"

## CLI Background Information
- Originally, ptero was conceived as a way to manage large volumes of wordpress sites and databases.
- It managed RDS instances, Mysql Innodb Operations, and repository cloning/ upgrading into environments on EC2 using FreeBSD and Centos
- I started building it about two years ago, and it's evolved into a comprehensive management solution for Wordpress sites (I host hundreds of them at AWS)
- Since late 2015 I began to evolve ptero into a multi-platform CLI that would embrace 12-factor methods and perform as a deployment engine for Reactive-style single page apps (SPA)

# The Original CLI
- performs all manner of operational commands for EC2 and RDS/Aurora, and has a built in git shell showing indications
- integrated with GNU screen & "boom" (etcd shell equivalent)
- integrated crypto vector management and hash verification/ role tokenization
- wordpress theme hashing support
- shadowfile, makefile, and git profile build support
- integrated vim-spf13 profiles
- driven mostly by shell scripts & node js (this is why I'm porting it to go-lang using cobra)


 This was the original structure, and is still widely utilized throughout my aws nodes. However, since the adoption of Docker and Rancher, 
 this CLI is becoming deprecated.  My intention is to make everything 100% microservices and HHVM images, and possibly adopt RancherOS when it stabilizes.
 
 The new Dockistry CLI will be entirely YAML-driven with a visual programming tool for stack and dependency management.  I'm also in favor of RethinkDB and Citus over Mysql/Aurora.
 
```
			 _____ ______ _________________________________ _____ ______ _______ (R)
			|     ||_____]  |  |______|         |   |      |     ||     \|______
			|_____||_____]__|  |______|_____    |   |_____ |_____||_____/|______
 

			Primary Help Command!  $ objectcode ...

 
			Devops Registries:

			pterops    --   this shows the devops ptero registry
			genops     --   this will show the genus sync tools (backups for RDS, R53, etc.)
			rexops     --   this will allow control over skel and rex instances for CRM cloning

			each of the above commands use a custom registry, which will not 
			execute unless you pass " | sh" after the command.

			i.e.-

			pterops backup.rvm     ---- will simply list what the command does
			pterops backup.rvm | sh  -- will execute the actual command

			most commands perform syncing operations to and from s3, and provide
			shortcuts for navigating repositories, github, apis, dockers, etc.

```
![ec2-images-dockistry](http://pterops.com.s3.amazonaws.com/screen-dockistry/cli-ptero-bsd.gif)

```

			SCREEN VIRTUAL COMMANDS REFERENCE:

			Ctrl A > Shift A     [rename window]
			Ctrl A > "           [window list]
			Ctrl A > c           [create window]
			Ctrl A > N           [says the window name]
			Ctrl A > n           [next farking window]
			Ctrl A > Ctrl A      [tab between two windows]
			Ctrl A > d           [detach session]
			screen -r            [reattach session]

			USEFUL SYSTEM COMMANDS:

			sys.loghead -- 110 lines of the head of the system log
			sys.log -- interactively tails the log events server wide
			sys.du -- specific disk usage of a directory in human form
			sys.mem -- useful memory information
			sys.init -- latest disk and memory happenings
			htop -- nicer top
			chkp -- performs a better ps grep for the process containing X string
			who -- whomai script
			ll -- laFh
			nocommit -- recent staging to git repos with FILE_NAME only
			noadd -- recent staging to git repos with gory details/diffs
			gc -- clones a git repo with basic hook that is customizable at post
			j -- jobs currently running
			mybash/ profile/ mebash -- immediately edits bash_profile (bash_rc not used)
			rehash -- sources the bash profile, like on freebsd
			inv -- outputs the current vector for a tokenized, active dev project of focus
			heroku.account -- staging area for heroku accounts
			skel -- outputs latest skel commands for amazon kinesis engine


			ptero Quick-reference Commands:    (when you hit "l" in bash)

			===    j | rm | cp | mv | ll | grep                    ===    
			===    vi+ | vi- | vc+ | vc - | p                      ===
			===    rex | theme | plug | gen | bow                  ===
			===    newize | bigize | bigify | sortize | memhead    ===
			===    rehash | who | aws | stECC | stRDS | stSSS      ===
			===    noadd | nocommit | dep | rex.prod | rex.dev     ===
			===    "l"  | rexbow | soa | comp | phar               ===  

```

# pTero Ubuntu CLI
- this is the current ubuntu toolkit including AWS docker CLI, and Etcd Docker CLI, EB Docker CLI and SAWS
- it is mainly utilized for production tasks, such as setting up new ubuntu server instances automatically
- the example below shows how I'm using it to automatically remember S3 filesyncing commands to pull data such as certs & profiles across the cluster
- I use this toolkit alongside the current Dockistry infrastructure tools with Rancher in production and have very few problems.
- I'm nearly done with this release and will be incorporating a duplicity docker backup solution and GPG keyring management into the next build
- It's written for Node Js deploys, and is entirely docker-container based, using Etcd and Samson/Sen for most storage considerations across the cluster
- This is the production toolkit, and it's totally separate from the development tooling CLI

--------

![ec2-images-dockistry](http://pterops.com.s3.amazonaws.com/screen-dockistry/cli-ubuntu.gif)


# monitoring example
- this is an example of a cloudwatch infrastructure dashboard
- all of these metrics will be available in the Experimental CLI using NPM WOPR & Blessed tooling (on the production toolkit)
- I would like for both Sentry and Cloudwatch alarms to push webhooks into the CLI and the Hubot Rocketchat instance
- There are a lot of other considerations for Docker management I would like to incorporate here but just don't have the time yet.

 
![ec2-images-dockistry](http://pterops.com.s3.amazonaws.com/screen-dockistry/dockistry-amazon-ec2.gif)




