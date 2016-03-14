![Golden Compass: An Elegant Full-Stack Project](https://raw.githubusercontent.com/yinanfang/GoldenCompass/master/materials/images/logo_github.png)

[![Build Status](https://travis-ci.org/yinanfang/GoldenCompass.png?branch=master)](https://travis-ci.org/yinanfang/GoldenCompass)

# Goal
- Language: ES6
- Backend: Express! -> Meteor-
- Frontend: React
- Architecture: Redux and immutable-js: http://www.ackmanndickenson.com/2015/11/blog-redux-and-immutable-js-take-center-stage/
- Bundler: Gulp! -> Webpack-
- Folder structure: https://github.com/kriasoft/react-starter-kit, polymer-starter-kit
- Tutorial:
  - http://marmelab.com/blog/2015/11/27/meteor-webpack-react-redux.html
  - http://sahatyalkabov.com/create-a-character-voting-app-using-react-nodejs-mongodb-and-socketio/
  - Used to setup initial express structure
    - http://www.dampmann.com/2014/09/nodejs-mongodb-jwt-bcrypt-and.html

# To-dos
- git
  - git model with: http://nvie.com/posts/a-successful-git-branching-model/
- Build system
  - Exact token and credentials in config.js to a env file. Copy the env file before starting node with env file. Don't commit env file.
    - http://himanshu.gilani.info/blog/2012/09/26/bootstraping-a-node-dot-js-app-for-dev-slash-prod-environment/
  - gulp-eslint
  - Notification with [gulp-notify](https://github.com/mikaelbr/gulp-notify)
- Restructure & Refactor
  - Example:
    - https://github.com/madhums/node-express-mongoose-demo
    - https://gist.github.com/lancejpollard/1398757
    - http://stackoverflow.com/questions/5778245/expressjs-how-to-structure-an-application
    - https://www.terlici.com/2014/08/25/best-practices-express-structure.html
- Log with winston
  - GCLog
  - move Loggly script from LikeIt repo. Use winston the Loggly
  - create new if not exist or append to existing log file: http://stackoverflow.com/questions/28924835/node-js-winston-can-i-append-log
  - Add https://github.com/visionmedia/debug to log.js
- Deployment
  - Development mode
    - nodemon -debug app.js
  - Production mode with pm2
    - pm2 start with json add log files for output and errors.
    - start pm2 with config file
  - Continuous Deployment with Webfaction
    - https://www.jamestease.co.uk/blether/deploying-express-nodejs-app-to-webfaction-using-git-hooks
    - http://www.raymonschouwenaar.nl/deploy-website-git-webhosting-webfaction-github-bitbucket/
    - https://gist.github.com/exclsr/8047140
  - Continuous Integration with Travis CI and auto deployment after success
    - https://gist.github.com/lukewpatterson/4242707
    - http://www.jvandemo.com/how-to-use-travis-ci-to-automatically-deploy-a-harpjs-application-to-github-pages/#
    - Production mode with pm2 node balance mode -i 0: http://pm2.keymetrics.io/docs/usage/cluster-mode/
  - post-receive problem
    - Can't do npm install on post-receive?
    - pm2 will be execute from git/LikeIt.git so express's views path will be wrong. How to pretend it's started from likeit/app?
    - Just do reload instead of delete+start! https://keymetrics.io/2015/03/26/pm2-clustering-made-easy/
- Authentication with JWT Token
  - Tutorials
    - https://scotch.io/tutorials/authenticate-a-node-js-api-with-json-web-tokens
  - Ideas
    - jsonwebtoken: https://github.com/auth0/node-jsonwebtoken
    - Check if JWT decode correctly. Add a certain answer. Add general format. Separate db queries to db.js. Take out all ps before return
    - Check password validity. char limit, IP?
    - Borrow login script form GC/LikeIt but with Sequalize
  - How to store JWT token in the browser
    - https://stormpath.com/blog/where-to-store-your-jwts-cookies-vs-html5-web-storage/
    - http://security.stackexchange.com/questions/87130/json-web-tokens-how-to-securely-store-the-key
    - https://stormpath.com/blog/build-secure-user-interfaces-using-jwts/
    - https://blog.prevoty.com/does-jwt-put-your-web-app-at-risk
    - http://www.sitepoint.com/php-authorization-jwt-json-web-tokens/
    - https://github.com/dwyl/learn-json-web-tokens
    - http://stackoverflow.com/questions/27067251/where-to-store-jwt-in-browser-how-to-protect-against-csrf
    - https://auth0.com/blog/2014/01/27/ten-things-you-should-know-about-tokens-and-cookies/
  - Secure & HttpOnly Coockie
    - http://www.troyhunt.com/2013/03/c-is-for-cookie-h-is-for-hacker.html
    - https://www.learnallthenodes.com/episodes/35-protecting-against-csrf-attacks-in-node
    - use express-session & csurf for CSRF prevention
      - http://scottksmith.com/blog/2014/09/04/simple-steps-to-secure-your-express-node-application/
      - https://www.learnallthenodes.com/episodes/35-protecting-against-csrf-attacks-in-node
  - HTTPS server
    - webfation special: https://community.webfaction.com/questions/4915/https-site
      - guide: https://docs.webfaction.com/user-guide/websites.html#secure-sites-https
      - not match problem: https://community.webfaction.com/questions/17306/using-https-and-http-on-a-nodejs-server
    - node, both http & https: http://stackoverflow.com/questions/11744975/enabling-https-on-express-js
    - force https
      - http://stackoverflow.com/questions/7450940/automatic-https-connection-redirect-with-node-js-express
    － Javascript inline function: http://stackoverflow.com/questions/10238849/how-to-get-a-variable-out-of-an-inline-function
    - Free SSL with https://www.startssl.com/
- User icon
  - [Identicon](https://github.com/dmester/jdenticon)
    - Generate a default icon with jdenticon and store url along with user info table
    - get code from Compass-old
- Server
  - Express:
    - static folder path problem: http://expressjs.com/en/starter/static-files.html
    - routing restriction, callback require - http://expressjs.com/api.html#app.all
    - https - http://expressjs.com/api.html#app.listen
    - http://expressjs.com/api.html#res.send
  - Better node require path
    - https://gist.github.com/branneman/8048520
    - http://www.bennadel.com/blog/2169-where-does-node-js-and-require-look-for-modules.htm
- plugin:
  - time zone: https://github.com/samsonjs/strftime
  - multi-form: https://www.npmjs.com/package/multer
- Testing
  - Postman
    - TDD - Write Postman test
    - Chain request http://blog.getpostman.com/2014/01/27/extracting-data-from-responses-and-chaining-requests/
  - Test Internet speed with Network Link Conditioner
    - http://nshipster.com/network-link-conditioner/
  - Type Checker Flow
    - http://flowtype.org/
    - http://www.keendevelopment.ch/flow-babel-gulp-es6/
  - Code complexity, coverage, style with [Code Climate](https://codeclimate.com)
  - Code complexity with plato
    - https://github.com/es-analysis/plato
    - Tutorial: http://ariya.ofilabs.com/2013/01/javascript-code-complexity-visualization.html
  - Browser test with Sauce Labs
    - https://github.com/wycats/handlebars.js/
    - https://github.com/chaijs/chai
- Debug
 - node inspector
- Compiler
  - https://github.com/babel/babel/
- Real time communication
  - Socket.IO
    - Authentication: https://auth0.com/blog/2014/01/15/auth-with-socket-io/
- Personal Page
  - React with Node
    - Intro: https://www.youtube.com/watch?v=NhoAxLElb-0&list=PLS0I2BfrZhzfT2EaYcRzClQlTPScKMzdK
      - Code: https://github.com/DavidWells/isomorphic-react-example
      - Slide and demos: http://davidwells.io/talks/isomorphic-javascript/#19
    - Use it with BrowserSync
      - https://github.com/Browsersync/recipes/tree/master/recipes/gulp.browserify
    - Use it with Handlebars
      - https://github.com/DavidWells/isomorphic-react-example#tutorial--video
      - https://scotch.io/tutorials/build-a-real-time-twitter-stream-with-node-and-react-js#routes
      - Important: http://www.crmarsh.com/react-ssr/
    - Real time
      - https://scotch.io/tutorials/build-a-real-time-twitter-stream-with-node-and-react-js
    - Isomorphic Javascript Rendering
      - https://www.youtube.com/watch?v=8wfY4TGtMUo
- SASS
  - Why http://www.zingdesign.com/less-vs-sass-its-time-to-switch-to-sass/
- Server comparison:
  - http://blog.litespeedtech.com/2013/11/12/new-benchmarks-litespeed-vs-apache-vs-nginx-for-static-content/
- Example repos
  - Danny's repo
    - https://github.com/HackrLabs/hackrtrackr-api/tree/refactor/es6
    - https://github.com/HackrLabs/hackrtrackr-web
    - https://github.com/Swiip/generator-gulp-angular
- ES6 Feature
  - https://github.com/lukehoban/es6features
- Server monitor
  - Use pmx with pm2
    - monitor trafic: https://app.keymetrics.io/#/bucket/5644e8cdc0d152ac7f59a3aa/transactions
    - add custom actions: http://docs.keymetrics.io/docs/pages/custom-actions/
    - logs for
      - post-receive
      - npm install
      - update server
      - connect to loggly?
  - glances & grafana
- Tools
  - https://www.airpair.com/node.js/posts/top-10-mistakes-node-developers-make
  - PhotoSwipe
    - http://photoswipe.com/documentation/getting-started.html
    - http://dimsemenov.com/plugins/magnific-popup/
    - http://getbootstrap.com/examples/jumbotron-narrow/
  - Async utility with [Async](https://github.com/caolan/async)
  - Promise with [bluebird](https://github.com/petkaantonov/bluebird/)
  - HTML with Modernizr: http://alistapart.com/article/taking-advantage-of-html5-and-css3-with-modernizr
- GC api structure
  - http://www.scriptscoop.net/t/4040f7d2bb7f/node.js-correct-modular-structure-of-nodejs-express-app-for-api.html
  - http://www.codekitchen.ca/guide-to-structuring-and-building-a-restful-api-using-express-4/
  - api/v1.0
    - gc
    - dbd
      - db.js
      - auth.js
      - list.js
- Design
  - For GC home page
    - use random Home page using [particle.js](https://github.com/VincentGarreau/particles.js/), [TheaterJS](https://github.com/Zhouzi/TheaterJS), [bigpicture.js](https://github.com/josephernest/bigpicture.js), or simple static page
  - logo design like code climate. Second beaker goes up
- Statistics??
  - [statsd](https://github.com/etsy/statsd)
  - https://www.datadoghq.com/blog/statsd/
- Style guide
  - [Airbnb Javascript Syntax](https://github.com/airbnb/javascript)
- Database
  - Chose MySQL because DBDCapital is more like a book keeping system
  - Separate db for GC and DBD Capital
  - [ ] Daily backup for the entire DB
    - [ ] Backup after a successful update of DB. Use it to restore if something goes wrong next time
  - Don't use user email as id, use userID. DB table prefix. dotenv. brosersync proxy port, get from env|config
- Summarize Great Article from
  - [ ] Make them a feature of this project.
    - [ ] [VIPER modularity ](http://www.objc.io/issues/13-architecture/viper/) - Get great links in this article
    - [ ] 10 key points: https://www.airpair.com/node.js/posts/top-10-mistakes-node-developers-make
    - [ ] This too: https://medium.com/@faisalabid/7-tips-for-a-node-js-padawan-e7c0b0e5ce3c
    - [ ] https://auth0.com/blog/2014/01/27/ten-things-you-should-know-about-tokens-and-cookies/



#### Structure

  - GoldenCompass
    - app.js
    - app
      - api
      - model
      - db
      - view
    node_modules
      - GCAppKit

- [ ] Build with Facebook [Flux](https://www.youtube.com/watch?list=PLb0IAmt7-GS188xDYE-u1ShQmFFGbrk0v&t=602&v=nYkdrAPrdcw) & React
  - MVC doesn't scale
    - MVC is pretty good for small application. Everything has its particular roll to play. The problem is that it doesn't make room for the new features
    - Increase predictability
    - MVC allows bi-direction data flow, but Flux allows only one direction data flow
    - When data changes, React re-renders the component
    - Referentially transparent functions
      - Describe UI at any point in time
      - Trivial to predict for a given input
      - Easy to test
    - React builds a new virtual DOM subtree
      - diffs it with the old one
      - computes the minimal set of DOM mutations and puts them in a queue
      - and batch executes all updates
    - Might worries about the performance if only a small changes occurs in a huge DOM tree. There're a lot of useless diffs



#### Architecture

1. Authentication
  - [x] Choose [Json Web Token over Session](https://auth0.com/blog/2014/01/27/ten-things-you-should-know-about-tokens-and-cookies/) with [Bcrypt](dcodeIO/bcrypt.js) Encryption
2. [JWT Advantage](https://scotch.io/tutorials/the-anatomy-of-a-json-web-token#what-are-json-web-tokens?)
  - JSON Web Tokens (JWT), pronounced “jot”, are a standard since the information they carry is transmitted via JSON. We can read more about the draft, but that explanation isn’t the most pretty to look at.
  - JSON Web Tokens work across different programming languages: JWTs work in .NET, Python, Node.js, Java, PHP, Ruby, Go, JavaScript, and Haskell. So you can see that these can be used in many different scenarios.
  - JWTs are self-contained: They will carry all the information necessary within itself. This means that a JWT will be able to transmit basic information about itself, a payload (usually user information), and a signature.
  - JWTs can be passed around easily: Since JWTs are self-contained, they are perfectly used inside an HTTP header when authenticating an API. You can also pass it through the URL.
  - Authentication with JWT because
    - [Cookies are bad for you](http://sitr.us/2011/08/26/cookies-are-bad-for-you.html)
    - [Difference between JWT and Cookie](https://stormpath.com/blog/where-to-store-your-jwts-cookies-vs-html5-web-storage/)





Random Icon from
https://www.iconfinder.com/iconsets/social-aquicons

https://www.iconfinder.com/iconsets/Insane_Icons
https://www.iconfinder.com/iconsets/Gallifreyan_icons
https://www.iconfinder.com/weather-icons?price=free&page=2
https://www.iconfinder.com/iconsets/characters-from-pop-culture
https://www.iconfinder.com/iconsets/jolly-icons-social-media-and-communication
https://www.iconfinder.com/iconsets/whiteboard-business-graphics
https://www.iconfinder.com/iconsets/christmas-icon-set-02
https://www.iconfinder.com/iconsets/christmas-icon-set-01
https://www.iconfinder.com/iconsets/snowflakes-free
https://www.iconfinder.com/iconsets/christmas-icons
https://www.iconfinder.com/iconsets/clothing-t-shirts-west
https://www.iconfinder.com/iconsets/hand-drawn-academic-icons-2
https://www.iconfinder.com/iconsets/Sketchy_icons_by_ma
https://www.iconfinder.com/iconsets/green-energy-initiative-1
https://www.iconfinder.com/iconsets/snowflakes-free
