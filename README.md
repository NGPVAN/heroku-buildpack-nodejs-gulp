Heroku Buildpack for Node.js and gulp.js
========================================

DevOps forked this on 2019-11-25 after https://elements.heroku.com/buildpacks/appstack/heroku-buildpack-nodejs-gulp started 
404ing on us. Heroku recommends forking them intentionally to prevent exactly that scenario. We had F. Stephen Quaratiello, 
our current AppSec engineer, audit it for any signs of nefarious code. All other aspects of this are the same as upstream unless otherwise indicated by commits like the one for this readme.
 
Usage
-----

- Set your Heroku app's buildpack URL to `https://github.com/timdp/heroku-buildpack-nodejs-gulp.git`
- Run `heroku labs:enable buildpack-env-arg` to enable environment variable support
- Run `heroku config:set NODE_ENV=production` to set your environment to `production` (or any other name)
- Add a Gulp task called `heroku:production` that builds your app
- Serve your app using Express or whatever

Credits
-------

Forked from [heroku-buildpack-nodejs](https://github.com/heroku/heroku-buildpack-nodejs).

Heavily based on [heroku-buildpack-nodejs-grunt](https://github.com/mbuchetics/heroku-buildpack-nodejs-grunt).
