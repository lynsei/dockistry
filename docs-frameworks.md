# frameworks
This is a bleeding edge list of the frameworks we support for SPA (reactive) strategies within our Developer CLI and as part of our "baselines" for stack deployment on Docker/ Rancher/ Npm.   

Because Dockistry maintains private repos and is built on Docker-compose YAML, we can avoid Node-gyp and other package issues commonly occurring in NPM (depending on your platform).  This also allows you to run test instances on separate  versions of the master registries thereby circumventing unit testing/ versioning issues on HHVM/ROS/Node environments.

For more information on how the CLI operates, view [docs-cli](https://github.com/forktheweb/dockistry/blob/master/dockistry-cli.md).
For windows examples view [experimental-cli](https://github.com/forktheweb/dockistry/blob/master/docs-experimental-cli.md).

To contribute or view our (pre-alpha) registry of stack strategies, say hi on [gitter](https://gitter.im/forktheweb/dockistry).

### aurelia 
http://aurelia.io

- aurelia-skeleton-navigation
   * webpack-typescript
   * es2016
- optional sample apps
  * aurelia-kendoui-bridge
  * aurelia-kendo-demo
- optional aurelia modules
  * aurelia-auth (jwt/ddd)
  * aurelia-config
- generators
   * [aurelia-ts generator](https://www.npmjs.com/package/generator-aurelia-ts)


### roots
http://roots.cx

- sprout based setup
- instant deploys on win32/64 node 0.12/4.43+/5.90+
- ptero rapid environments setup
- rethinkdb with strongloop
- lightweight alternative to gulp/grunt based setups
- great for desktop electron apps using coffee-basis
- stable cli integration with ptero devops

### feathers
http://feathersjs.com/

- feathersjs base
- material-ui
- feathers-accounts
- [this guy](http://kulakowka.com/) has more forks than even I do, so I follow him for feathers watching
- [feathersjs generator](https://github.com/feathersjs/generator-feathers)

### angular
https://angular.io/

 - [angular2-gulp-webpack generator](https://github.com/ericmdantas/generator-ng-fullstack)
 - [ui grid](http://ui-grid.info/)
 - [dynatable](https://www.dynatable.com/) for small page light-weight grids
 - [material2](https://github.com/angular/material2) or [semantic ui](http://semantic-ui.com/introduction/integrations.html)
 - https://material.angularjs.org
 - [mean stack generator optional](https://github.com/angular-fullstack/generator-angular-fullstack)
 - [blur example](https://github.com/akveo/blur-admin)
 
### react
https://facebook.github.io/react/

- generators
    * [react with flux and alt and webpack](https://github.com/weblogixx/generator-react-webpack-alt)
    * [react baseline with webpack](https://github.com/newtriks/generator-react-webpack)
    * [react material-ui](https://www.npmjs.com/package/generator-material-react)
- ui options 
    * [semantic ui](http://semantic-ui.com/introduction/integrations.html)
    * [material ui for react](http://www.material-ui.com)
- option for [structor](https://github.com/ipselon/structor) [material-ui-prepack](https://github.com/ipselon/material-ui-prepack)
