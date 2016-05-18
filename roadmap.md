	     ||`           '||               ||                  
	     ||             ||     ''        ||                  
	 .|''|| .|''|,.|'', || //` || (''''''||'' '||''|'||  ||` 
	 ||  || ||  ||||    ||<<   ||  `'')  ||    ||    `|..||  
	 `|..||.`|..|'`|..'.|| \\..||.`...'  `|..'.||.       ||  
	                                                  ,  |'  
	 ~ Fullstack strategies by forking pterodactyls    ''              

> last updated: 05-18-2016 2pm

# dockistry roadmap
>  "a reference roadmap for dockistry platform agnostic, language agoric software"

Dockistry provides native tooling & docker-driven images that ease deployment and E2E considerations across multiple architectures, and in multiple languages.  This is done to provide options for developers both locally, and in staging/production environments at Amazon and Google.


## management tools

##### dockistry is offering the following flavors (pre-alpha)
| name | description | architectures | purpose | built with |
| :-------- | --------:| :------: | :------: | :------: |
| *"stackerize app"*  |   desktop E2E primary  | darwin, win10, ubuntu | desktop installer baseline: live strategy management & toolkit installers |  angular2, electron, and using Falcor & RethinkDB.  immediately deploy stacks to any AWS/ Google Cloud/ Windows, or Ubuntu environment
| *"[devtools packages](https://github.com/dockistry/devtools-multi-clis)"*  |  multi-platform, agoric packages designed to streamline developer tooling &  consolidate build-tools and unit-testing.   | all platforms and devices | the goal is to keep the tooling the same for all packages in our registry. |  go, node, powershell, docker... [phase 2 maybe some elixir, swift, ionic] |

## stackerize app

#### desktop 
Dockistry comes in several flavors for desktop users.  All of our tools are installed from a single package called "Stackerize", which provides everything you will need for infrastructure and devtools packages. [you can also [download these tools individually](//github.com:443/dockistry/) if you wish].

Dockistry is fundamentally a developer-oriented project that is designed to compose projects as "stacks", and do so with incredible speed and reliability.   This can only happen if a robust set of tools are offered through a CLI.  Dockistry developers intend to build a community on top of the CLI tools and technologies, and this is why we are separating our CLI tools from the Stackerize app itself, which will be more community focused.  The primary reason the Stackerize app exists is to integrate everything together, the tools, and the community.


 
  
 



