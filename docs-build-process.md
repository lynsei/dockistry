## production builds
Our production CLI tools allow you to create Amazon AWS instances and install any of our fullstack strategies by configuring their options.
The following is the "order of operations" for how stacks are installed in production:

- sets up the git location for installing (or pass it with --gitpath)
- fetches specified repo (local/master)
- reads the following files:
    * dockistry-compose.yml - specific rules for the cli to follow
    * docker-compose.yml - docker composition 2.0
    * rancher-compose.yml - cluster setup info
- upon reading the rules, the CLI will execute the creation of the docker-compose using the install path
- volume paths not specified will prompt the user for those
- containers are brought online, as is the cluster via Rancher
- once containers are online the system executes commands based on the dockistry-compose.yml rules
   * npm installation commands
   * jspm commands
   * yo generators
   * bower commands
- afterwards the system will backup the state of the container volumes with duplicity and do a test restore


## notes
Our Dockistry YAML defines which build process to use in production environments on Amazon or Google clouds.  This is to prevent the build from trying to compile visual c++ apps, or other mobile-only or desktop-only builds that should be occurring on Darwin or Windows development environments.

