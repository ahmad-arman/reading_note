
## Heroku 

### When installation completes, you can use the heroku command from your terminal.

On Windows, start the Command Prompt (cmd.exe) or Powershell to access the command shell. Use the `heroku login`
 command to log in to the Heroku CLI:
 ```
  $ heroku login
heroku: Press any key to open up the browser to login or q to exit
 ›   Warning: If browser does not open, visit
 ›   https://cli-auth.heroku.com/auth/browser/***
heroku: Waiting for login...
Logging in... done
Logged in as me@example.com 
```

### This tutorial will work for any version of Node greater than 10 - check that it’s there:
```
 $ node --version
v14.15.4
``` 

###  npm is installed with Node, so check that it’s there. If you don’t have it, install a more recent version of Node:

```
 $ npm --version
6.14.11
```

### Now check that you have git installed. If not, install it and test again.

```
 $ git --version
git version 2.28.0
```

## Prepare the app:
In this step, you will prepare a sample application that’s ready to be deployed to Heroku.

### To clone a local version of the sample application that you can then deploy to Heroku, execute the following commands in your local command shell or terminal:
 
 ``` 
 $ git clone https://github.com/heroku/node-js-getting-started.git
   cd node-js-getting-started
```

### Deploy the app:
In this step you will deploy the app to Heroku. <br>
Create an app on Heroku, which prepares Heroku to receive your source code.

``` 
 $ heroku create
Creating sharp-rain-871... done, stack is heroku-18
http://sharp-rain-871.herokuapp.com/ | https://git.heroku.com/sharp-rain-871.git
Git remote heroku added
```

When you create an app, a git remote (called heroku) is also created and associated with your local git repository.

Heroku generates a random name (in this case sharp-rain-871) for your app, or you can pass a parameter to specify your own app name.

Now deploy your code:

``` 
git push heroku main
Counting objects: 488, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (367/367), done.
Writing objects: 100% (488/488), 231.85 KiB | 115.92 MiB/s, done.
Total 488 (delta 86), reused 488 (delta 86)
remote: Compressing source files... done.
remote: Building source:
remote:
remote: -----> Node.js app detected
remote:
remote: -----> Creating runtime environment
remote:
remote:        NPM_CONFIG_LOGLEVEL=error
remote:        NODE_VERBOSE=false
remote:        NODE_ENV=production
remote:        NODE_MODULES_CACHE=true
remote:
remote: -----> Installing binaries
remote:        engines.node (package.json):  14.x
remote:        engines.npm (package.json):   unspecified (use default)
remote:
remote:        Resolving node version 14.x...
remote:        Downloading and installing node 14.15.4...
remote:        Using default npm version: 6.14.11
       ....
remote: -----> Build succeeded!
remote: -----> Discovering process types
remote:        Procfile declares types -> web
remote:
remote: -----> Compressing...
remote:        Done: 19M
remote: -----> Launching...
remote:        Released v3
remote:        http://sharp-rain-871.herokuapp.com deployed to Heroku
remote:
remote: Verifying deploy... done.
To https://git.heroku.com/nameless-savannah-4829.git
 * [new branch]      main -> main

 ```
