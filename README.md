
[![Build Status](https://travis-ci.org/yinanfang/GoldenCompass.png?branch=master)](https://travis-ci.org/yinanfang/GoldenCompass)


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
