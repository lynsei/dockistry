	     ||`           '||               ||                  
	     ||             ||     ''        ||                  
	 .|''|| .|''|,.|'', || //` || (''''''||'' '||''|'||  ||` 
	 ||  || ||  ||||    ||<<   ||  `'')  ||    ||    `|..||  
	 `|..||.`|..|'`|..'.|| \\..||.`...'  `|..'.||.       ||  
	                                                  ,  |'  
	 ~ Fullstack strategies by forking pterodactyls    ''              

> last updated: 05-12-2016 2pm

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

#### tooling considerations
  > *... a bit of background information and a preface by [forktheweb](//github.com:443/forktheweb)*

  All too frequently over the course of [my career](https://labs.stackfork.com:2003/dockistry-contributors/cho), I've chosen the wrong technology and gotten stuck with it.  This is easy to do.  Given the vast amount of tools and technologies readily available on the web, I've turned into a bit of a magpie developer.  I don't think this is a bad thing, but there certainly needs to be an organized method to address the relative chaos of fullstack development.

 It's not uncommon for fullstack developers to have huge amounts of starred/watched repos on github.  If you've ever been burned on technology decisions when implementing on a grand scale, then you know the key is to avoid dependencies on any one technology where possible, and enourage flexibility in resolving dependency issues network wide via an abundance of practical alternatives. The problem this creates is that there really isn't too much focus on pairing technologies together, which is the problem Dockistry aims to primarily address.  We call such pairing "strategy".
  
   I've chosen to intentionally moderate how far I get involved with various frameworks and other technologies.  After all, there is always something new coming out, and the grass *really is* greener on the other side.  This approach provides a broad viewport, and from there I can see far-reaching interactions & possibilities.   

  The success I've had using the aforementioned technique along with early adoption of newer technologies such as Docker & Rancher, is what has inspired me to bring a fresh perspective to the open source community through Dockistry.   Dockistry intends to be a strategy-based engine to deploy both devtools & production stacks. It will be truly accomodating to multi-platform, multi-language deploys.
  
   The tools provided by Dockistry are curated & lean intentionally so they can be re-used/ easily forked.  I am building the primary desktop software based off an entirely web-based app integrated into a Git, Docker, and NPM registry.  This allows the app to stay current without regular updates to the binaries, and will allow the same API to be accessed through a variety of separate tooling packages as things progress.  The registry is pretty lightweight, since it's all just docker-composition files and basic boilerplates.  So the idea is to clone the whole thing and quickly browse various strategies locally, then deploy them.

I intend to galvanize any skeptic-thinkers by hitting people with a truly fresh take on stack development & deployment, something they haven't seen ever before.  I'm stoked to be able to do that.
 
  
 



