
[![Build Status](https://travis-ci.org/yinanfang/GoldenCompass.png?branch=master)](https://travis-ci.org/yinanfang/GoldenCompass)


# Goal
- Language: ES6
- Backend: Express! -> Meteor?
- Frontend: React
- Architecture: Redux
- Bundler: Gulp! -> Webpack?
- Folder structure: https://github.com/kriasoft/react-starter-kit
- Tutorial:
  - http://marmelab.com/blog/2015/11/27/meteor-webpack-react-redux.html
  - http://sahatyalkabov.com/create-a-character-voting-app-using-react-nodejs-mongodb-and-socketio/


# GoldenCompass-node guidline

Restructure the app - https://github.com/madhums/node-express-mongoose-demo
Continuous Deployment on Webfaction
  - https://www.jamestease.co.uk/blether/deploying-express-nodejs-app-to-webfaction-using-git-hooks
  - http://www.raymonschouwenaar.nl/deploy-website-git-webhosting-webfaction-github-bitbucket/
  - https://gist.github.com/exclsr/8047140
Continuous Integration with Travis CI and auto deployment after success
  - https://gist.github.com/lukewpatterson/4242707
  - http://www.jvandemo.com/how-to-use-travis-ci-to-automatically-deploy-a-harpjs-application-to-github-pages/#
https://scotch.io/tutorials/authenticate-a-node-js-api-with-json-web-tokens
Check if JWT decode correctly. Add a certain answer. Add general format. Separate db queries to db.js. Take out all ps before return
Check password validity. char limit, IP?
Save a default icon in file. After send back registration, set the default icon and request the jdenticon from Heroku server. Then change the icon path. Add a row in the user table
Try Identicon. Ask why it's not popular
Single page: page.js
Auto deployment: flight plan github??
Express:
  - static
  - routing restriction, callback require - http://expressjs.com/api.html#app.all
  - https - http://expressjs.com/api.html#app.listen
  - http://expressjs.com/api.html#res.send
Node architecture
  - https://github.com/madhums/node-express-mongoose-demo
plugin:
  - time zone: https://github.com/samsonjs/strftime
  - multi-form: https://www.npmjs.com/package/multer
Send status (in header) with message function, other function, overload?
Postman
  - TDD - Write Postman test
  - Chain request http://blog.getpostman.com/2014/01/27/extracting-data-from-responses-and-chaining-requests/
Compiler
  - https://github.com/babel/babel/
Network Link Conditioner
  - http://nshipster.com/network-link-conditioner/
Socket.IO
  - Authentication: https://auth0.com/blog/2014/01/15/auth-with-socket-io/
GSS
  - Speech: https://vimeo.com/91393694
  - https://github.com/gss/engine
Webpack
  - https://github.com/webpack/webpack
React with Node
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
Type Checker Flow
  - http://flowtype.org/
  - http://www.keendevelopment.ch/flow-babel-gulp-es6/
SASS
  - https://github.com/sass/sass

#### To read
- node inspector
- nodemon -debug app.js
- Angular
  - johnpapa/angular-styleguide
  - Angular UI: https://angular-ui.github.io/
    - https://github.com/angular-ui/bootstrap
    - Web code editor: https://github.com/angular-ui/ui-ace
- Tutorial - https://egghead.io/
- Danny's repo
  - https://github.com/HackrLabs/hackrtrackr-api/tree/refactor/es6
  - https://github.com/HackrLabs/hackrtrackr-web
  - https://github.com/Swiip/generator-gulp-angular
- Repo
  - Airbnb
    - UITableView for javascript: https://github.com/airbnb/infinity
    - Multi language - https://github.com/airbnb/polyglot.js
    - Style guide - https://github.com/airbnb/javascript
- ES6 Feature
  - https://github.com/lukehoban/es6features

#### To Think About
- EC6 Generator
  - Server - koa
  browser - bluebird, tracer-compiler
- Immutable State
  - [immutable-js](http://facebook.github.io/immutable-js/) - Immutable persistent data collections for Javascript which increase efficiency and simplicity.
- Type
  - flow - Adds static typing to JavaScript to improve developer productivity and code quality. http://flowtype.org/

#### Used
- blog post
  - Used to setup initial express structure
    - http://www.dampmann.com/2014/09/nodejs-mongodb-jwt-bcrypt-and.html


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

To-do

pm2 start with json add log files for output and errors.
Add comment to start, stop

Borrow login script form GC but with Sequalize
setup express, login.js with jsonwebtoken, simple webpage with handlebar. and database

Use pmx
  - monitor trafic: https://app.keymetrics.io/#/bucket/5644e8cdc0d152ac7f59a3aa/transactions
  - add custom actions: http://docs.keymetrics.io/docs/pages/custom-actions/
  - logs for
    - post-receive
    - npm install
    - update server
    - connect to loggly?

Add gulp-eslint

Exact token and credentials in config.js to a env file. Start node with env file. Don't commit env file

Badge to use

  - Sauce Labs
    - https://github.com/wycats/handlebars.js/
    - https://github.com/chaijs/chai
  - node-inspector
    - https://github.com/node-inspector/node-inspector
  - plato
    - Add it to gulp: https://github.com/sindresorhus/gulp-plato
    - Tutorial: http://ariya.ofilabs.com/2013/01/javascript-code-complexity-visualization.html

Find useful tools
  - https://www.airpair.com/node.js/posts/top-10-mistakes-node-developers-make

How to store JWT token in the browser
  - https://stormpath.com/blog/where-to-store-your-jwts-cookies-vs-html5-web-storage/
  - http://security.stackexchange.com/questions/87130/json-web-tokens-how-to-securely-store-the-key
  - https://stormpath.com/blog/build-secure-user-interfaces-using-jwts/
  - https://blog.prevoty.com/does-jwt-put-your-web-app-at-risk
  - http://www.sitepoint.com/php-authorization-jwt-json-web-tokens/
  - https://github.com/dwyl/learn-json-web-tokens
  - http://stackoverflow.com/questions/27067251/where-to-store-jwt-in-browser-how-to-protect-against-csrf
  - https://auth0.com/blog/2014/01/27/ten-things-you-should-know-about-tokens-and-cookies/
Secure & HttpOnly Coockie
  - http://www.troyhunt.com/2013/03/c-is-for-cookie-h-is-for-hacker.html
  - https://www.learnallthenodes.com/episodes/35-protecting-against-csrf-attacks-in-node

  - use express-session & csurf for CSRF prevention
    - http://scottksmith.com/blog/2014/09/04/simple-steps-to-secure-your-express-node-application/
    - https://www.learnallthenodes.com/episodes/35-protecting-against-csrf-attacks-in-node

HTTPS server
  - webfation special: https://community.webfaction.com/questions/4915/https-site
    - guide: https://docs.webfaction.com/user-guide/websites.html#secure-sites-https
    - not match problem: https://community.webfaction.com/questions/17306/using-https-and-http-on-a-nodejs-server
  - node, both http & https: http://stackoverflow.com/questions/11744975/enabling-https-on-express-js
  - force https
    - http://stackoverflow.com/questions/7450940/automatic-https-connection-redirect-with-node-js-express
  － Javascript inline function: http://stackoverflow.com/questions/10238849/how-to-get-a-variable-out-of-an-inline-function

Instagram API
  - https://lob.com/blog/building-an-instagram-postcard-app-in-express-js/
  - http://www.9lessons.info/2012/05/login-with-instagram-php.html
  - https://instagram.com/developer/authentication/
  - https://github.com/totemstech/instagram-node
  - https://github.com/jaredhanson/passport-instagram

Large scale express app folder structure
  - https://gist.github.com/lancejpollard/1398757
  - http://stackoverflow.com/questions/5778245/expressjs-how-to-structure-an-application
  - https://www.terlici.com/2014/08/25/best-practices-express-structure.html

winston
  - no such file error.
    - doesn't check log but need to create a empty file?
    - in utils/logger.js check if a empty file exist and create one?

GC api structure
  - http://www.scriptscoop.net/t/4040f7d2bb7f/node.js-correct-modular-structure-of-nodejs-express-app-for-api.html
  - http://www.codekitchen.ca/guide-to-structuring-and-building-a-restful-api-using-express-4/
  - api/v1.0
    - gc
    - dbd
      - db.js
      - auth.js
      - list.js
  - utils
  - app
    - index.js
  - views
    - html

Express static files
  - http://expressjs.com/starter/static-files.html
    - server some static files behind auth?

post-receive problem
  - Can't do npm install on post-receive?
  - pm2 will be execute from git/LikeIt.git so express's views path will be wrong. How to pretend it's started from likeit/app?

display url
  - make it different for home and login

PhotoSwipe
  - http://photoswipe.com/documentation/getting-started.html
  - http://dimsemenov.com/plugins/magnific-popup/
  - http://getbootstrap.com/examples/jumbotron-narrow/

