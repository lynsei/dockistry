## Dockistry philosophies

#### Embrace 12-factor wherever possible
Read about 12 factor methods [here](http://12factor.net/).

#### Hogans are always applicable
Because [hogans](https://github.com/object-code/hogan.js) are always fast.

# apply the least astonishment principle
"if a necessary feature has a high astonishment factor, it may be necessary to redesign the feature."  In general engineering design contexts, the principle may be taken to mean that a component of a system should behave in a manner consistent with how users of that component are likely to expect it to behave.

DWIM
"correct errors automatically or with minor user intervention"

# Avoidance of false affordance
>An affordance is a relation between an object or an environment and an organism that, through a collection of stimuli, affords the opportunity for that organism to perform an action.   This concept is the opposite of that, and relates to web development more specifically than most other concepts.  a good example of a false affordance for web pages is a link that says "view bill", yet goes to a pdf for the bill in a new window.  False affordance is lazy programming typically, but it can also be as severe as "deceptive".  Google is super-tough now a days with V8 chrome and so we are using PhantomJS and Karma testing suites to prevent problems before they happen.  A good example of "deceptive" errors they prevent now-a-days are "download" buttons that redirect to another domain.  They also do not allow you to wget or curl, or use php to pull versions of their Google signup forms and display them in a frame... to prevent Phishing. (again, just an example).

## Minimist
> "If code were poetry, people would want to read it"

## Policies
* Use ubiquitous SSL and crypto on everything
* Don't store keys or write them down
* Automate everything that is repeated often; including unit, integration, functional and performance testing.
* Build quality in. Automate code quality analysis, code coverage.
* Creating processes primarily aimed at garnering fast feedback leads to a quality product.
* Release early and often and keep your application always production ready.
* Make your development, QA, and stage environment the same as production environment but on a smaller scale.
* Automate code deployment. Make it a repeatable process by ensuring deployment is same in all environments.
* Design and architect your applications to handle failure of individual components.
* Make your application stateless, and thereby ensuring the application can be installed without any downtime to end users. It is easier to do zero downtime deployments when the application is stateless.
* Collecting metrics and monitoring should be an integral part of application development, not an afterthought.
* Put your logs in a centralized location so that you can debug and troubleshoot issues quickly.
* Make your deployments as boring, drama-free and non-eventful as possible.

 

#### Find Humor Wherever Possible
- a foreward from our [forefathers](http://search.cpan.org/dist/perlsecret/lib/perlsecret.pod#SYNOPSIS)
- a [ruby reference](https://github.com/JuanitoFatas/what-do-you-call-this-in-ruby) of characters
 
> Pythonists are all "explicit is better than implicit" and Rubists are all like "LOOK AT ME I MADE A BONG OUT OF THIS HAIR DRYER"

- a [how-to](https://github.com/braydie/HowToBeAProgrammer) worth reading
- a [really funny guide](https://encyclopediadramatica.se/Ruby_on_Rails) to ruby
