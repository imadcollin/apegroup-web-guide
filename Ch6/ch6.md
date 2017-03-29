# Chapter 6 
Now, almost we were done. Two small things we must cover and then u will build nice projects for Apegroup.

### Intro
In this chapter, you should check the normal packages that we use all the time in all our projects. 
So, please check the file below and once again” Go to your colleagues in case of any problem. It could be difficult to catch everything inside but, this important to know.

### Package.json 
> this file is the main part of any project we built.These files include the scripts,
> which will run when we start the project.
> It also contains the server , gulp task, and more executing command. 
> You shall learn these scripts and how they are working :) 
```javascript
/*******************************************************************************
1. Here the project name -Normally the name is given when you start npm init 
*******************************************************************************/
{
  "name": "apegroup-dashboard-web",
  "version": "1.0.0-build.4",
  "description": "Progressive Web Application.",
  "private": true,
  "main": "server",
  "engines": {
    "node": ">=6.0.0"
  },
  /*******************************************************************************
2. The scripts -This could be differ from an implementation to another 
   Remember Scripts need to run with npm command like: npm run gulp  
  *******************************************************************************/
  "scripts": {
    "firebase": "firebase",
    "gulp": "./node_modules/gulp-cli/bin/gulp.js --gulpfile=./gulp/gulp.js --require babel-register --cwd=./",
    "preversion": "npm test",
    "postversion": "git push && git push --tags",
    "start": "firebase serve --port=3000",
    "test": "npm run test:client",
    "test:client": "wct --local=chrome './src/**/*.spec.html'",
    "test:server": "mocha --compilers js:babel-register ./server/**/*.spec.js"
  },
  /*******************************************************************************
3. We write our server dependencies here 
   -Koa is a backage where you can find online //try to see express as well 
  *******************************************************************************/
  "dependencies": {
    "koa": "^2.0.0-alpha.7",
    "koa-compress": "^2.0.0",
    "koa-conditional-get": "^2.0.0",
    "koa-etag": "^3.0.0",
    "koa-static": "^3.0.0"
  },
  /*******************************************************************************
4.  This section contains all required dependencies for running/compiling/Interpretering 
    the files and code to understandable language by the machine
    -Try to read about babel and what it doing 
    -Try to read about browser/sync 
    -Try to see what mocha is for and how you write tests with it 
    -Firesbase is very important we will cover in details 
    *******************************************************************************/
  "devDependencies": {
    "babel-core": "^6.21.0",
    "babel-preset-env": "^1.1.5",
    "babel-register": "^6.18.0",
    "browser-sync": "^2.18.5",
    "eslint": "^3.12.2",
    "firebase-tools": "^3.4.0",
    "gulp": "github:gulpjs/gulp#4.0",
    "gulp-babel": "^6.1.2",
    "gulp-cli": "^1.2.2",
    "mocha": "^3.2.0",
    "polymer-build": "^0.5.1"
  },
 /*******************************************************************************
4. Here you can define the data as needed --remember always what we are doing is for 
   Ape group not for our private names :)
  *******************************************************************************/
  
  "repository": {
    "type": "git",
    "url": "git+ssh://git@bitbucket.org/apegroup/apegroup-template-web.git"
  },
  "author": "Apegroup AB",
  "contributors": [
    {
      "name": "<name>",
      "email": "<name>@apegroup.com"
    }
  ],
  "license": "Apegroup AB. All rights reserved.",
  "homepage": "http://apegroup.com"
}

```
