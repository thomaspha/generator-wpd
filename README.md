# generator-wpd [![Build Status](https://secure.travis-ci.org/hite/generator-wpd.png?branch=master)](https://travis-ci.org/hite/generator-wpd)

quick start up to build modern webapp.
>wpd means `W`eb `P`roduct `D`evelop;

## Getting Started

 Make sure you have installed [Node.js](http://nodejs.org/) because all tools are based on nodejs to work out. If not ,visit [http://nodejs.org/download/](http://nodejs.org/download/) ,and find out the right version installer accorded with your OS. Install it step by step.

 Assumed that you have Node.js > v0.9.0, some npm packages are also needed.    
 First, you'll need to install `yo` and other required tools.


```bash
$ npm install -g yo
```

If you are using npm 1.2.10 or above, this will also automatically install grunt and bower for you. If you're on an older version of npm, you will need to install them manually:

```bash
# For npm versions < 1.2.10.
npm install -g grunt-cli bower
```

### what is generator-wpd

Generator-wpd is a project generator for wpd group aimed to quickly set up a new webapp project develop enviroment including css framework, css validation, html scaffolding ,JS util, AMD or CMD modular, UI library, grunt tasks, delopy tools etc.  
Generator-wpd includes four sub modules by now.

+ mobile-basic
+ mobile-appjs
+ mobile <font color=green>(coming soon)</font>
+ desktop-basic 
+ desktop <font color=green>(coming soon)</font>

To install generator-wpd from npm, run:

```bash
$ npm install -g generator-wpd
```

Finally, initiate the generator in some directory your project resides (by now desktop-basic and mobile-basic are available):

```bash
$ yo wpd:mobile-basic # yo wpd:desktop-basic
```

And now, you enter into the app directory to start coding. That is fast and esay.

The last keyboard hits are `grunt rundemo` ,and you will see the demo,ENJOY!

### About generator submodules
> mobile-basic
  
+ Aim at small project which does't have much pages. Such project page also have a simple pageflow , few widgets , basic interaction model
+ technology stack.[zepto.js](http://zeptojs.com/) for DOM\EVENT util instead of jQuery on desktop;         [GMU](http://gmu.baidu.com/) for UI library;[seajs](seajs.org) for module management ; [grunt](http://gruntjs.org) for tasks building; [mocha][] for test framework

>mobile-appjs

+ Aim at one page on application.
+ [techology stack]. [appjs](http://code.kik.com/app/2/index.html);[seajs](seajs.org) for module management ; [grunt](http://gruntjs.org) for tasks building;
 
> mobile

+ Aim at bigger project which have some pages. Such project page  have a long pageflow , tabs\pageview\listview widgets using around the app . Due to complex page relationship, MVC structure is the best choice.
+ technology stack.[backbone.js](http://backbonejs.org/) for MVC; Css framework in [{less}](lesscss.org) or [sass](http://sass-lang.com) or [stylus](http://learnboost.github.io/stylus), and make your choice; html scaffolding can be [bootstrap][] or [Intel's App Framework](http://app-framework-software.intel.com/documentation.php) ; [grunt][] or [gulp][] for tasks building; [BEM][] or [wpdcsscode][] for code style; [mocha][] or [jasmine][] for test framework 

>desktop-basic

+ Aim at bussiness website building
+ technology stack.[jquery][] for DOM\EVENT util ; CSS coding using [WPD Css code style][wpdcsscode];[requirejs](http://requirejs.org) for module management ; [grunt][] for tasks building; [sharkjs][] for UI library;[mocha][] or [jasmine][] for test framework 

>desktop

+ Aim at flexiable configure project. use different tools chain in corroding to different bussiness system;
+ technology stack. [bootstrap][] or [foundation5][] for css framework; [wpdcsscode][] or [BEM][] for css code style;[grunt][] or [gulp][] for tasks building; bower for client package management;[mocha][] or [jasmine][] for test framework 

## Changlog

**Release log @2014-10-17 in version 0.4.0 for mobile-appjs template**

+ add [grunt-pack-static](https://github.com/hite/pack-static/) supports
+ fix much config errors
+ and one-click deployment. Just hit `grunt deploy --force`
 
**Release log @2014-09-23 in version 0.3.5**

+ bugfixs

**Release log @2014-09-13 in version 0.3.4**

+ bugfixs
+ remove some useless questions in desktop-basic
+ remove autowire ip into file for weinre support


**Release log @2014-8-9 in version 0.3.0**

+ add mobile-appjs generator

**Release log @2014-7-28 in version 0.2.2**

+ add fake domain `demo.mail.163.com`. please make sure 'demo.mail.163.com 120.0.0.1' is in your hosts
+ remove grunt-contrib-watch package because of grunt localserver doesn't support watch function.
+ add demo written with Ratchet framework and GMU.
+ fix some bower dependencies (seajs, gmu etc.)
+ add **common** directory


**Release log @2014-7-21 in version 0.2.1**

+ fix grunt-localserver config errors. now grunt rundemo works properly in both generators.
+ add static server to mobile-basic generator . More about grunt-localserver
+ remove GMU static directory , replace with bower import in generator mobile-basic
+ add missing packages in package.json of mobile-basic
+ simplify `yo wpd:mobile-basic` flow of installation
+ add scss demo files in generator mobile-basic
+ enable weinre and watch function  running in concurrent

**Release log @2014-7-18 in version 0.2.0 (just about desktop-basic generator )**

+ rewrite the `yo wpd:desktop-basic` flow of installation . Add few questions about Ruby installation and CodeSinppet installation in WebStrom or SublimeText.
+ add static server which surpports ftl files parsing and ajax-server emulator . More about [grunt-localserver](https://www.npmjs.org/package/grunt-localserver)
+ add run-demo grunt task to quick see the demo page. Just run `grunt rundemo` in directory containing Gruntfile.js.
+ optimize Gruntfile.js, and delete unnecessary tasks and configuration


**Release log @2014-7-14 in version 0.1.0**

+ add desktop-basic generator
+ remove all questions in mobile-basic generator
+ add debugger scheme in mobile-basic generator
+ add demo\issues\bugs directory for later usage
+ add freemarker template file's parser in desktop-basic generator
+ add default favicon.ico in both generators
+ add sass grunt task in desktop-basic generator
+ add basic demo files in desktop-basic generator

## License

MIT


[bootstrap]: http://getbootstrap.com/2.3.2 
[grunt]: http://gruntjs.org 
[bem]: http://bem.info 
[jquery]: https://jquery.org/
[wpdcsscode]: http://mail.163.com
[sharkjs]: http://sharkjs.org
[foundation5]:http://foundation.zurb.com/develop/download.html
[gulp]:http://gulpjs.com
[mocha]:http://visionmedia.github.io/mocha/
[jasmine]:https://github.com/pivotal/jasmine
