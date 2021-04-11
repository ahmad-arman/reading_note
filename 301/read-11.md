 #  Options
  `cache` Compiled functions are cached, requires filename <br>
 `filename` Used by cache to key caches, and for includes<br>
 `root` Set project root for includes with an absolute path (e.g, /file.ejs). Can be array to try to resolve include from multiple directories.<br>
` views` An array of paths to use when resolving includes with relative paths. <br>
 `context` Function execution context <br>
 `compileDebug` When false no debug instrumentation is compiled <br>
 client Returns standalone compiled function<br>
 delimiter Character to use for inner delimiter, by default '%'<br>
 openDelimiter Character to use for opening delimiter, by default '<' <br>
 closeDelimiter Character to use for closing delimiter, by default '>' <br>
 debug Outputs generated function body <br>
 strict When set to `true`, generated function is in strict mode <br>
 _with Whether or not to use with() {} constructs. If false then the locals will be stored in the locals object. (Implies `--strict`) <br>
 




# Tags 
 `<%` 'Scriptlet' tag, for control-flow, no output <br>
 `<%_` ‘Whitespace Slurping’ Scriptlet tag, strips all whitespace before it <br>
 `<%=` Outputs the value into the template (HTML escaped) <br>
 `<%-` Outputs the unescaped value into the template <br>
 `<%#` Comment tag, no execution, no output <br>
 `<%%` Outputs a literal '<%' <br>
 `%>` Plain ending tag <br>
 `-%>` Trim-mode ('newline slurp') tag, trims following newline <br>
 `_%>` ‘Whitespace Slurping’ ending tag, removes all whitespace after it <br>













## How To Use EJS to Template Your Node Application
 Setting up the Demo App
  We will be making two pages for our application with one page with full width and the other with a sidebar. <br>
  Get the code: You can find a git repo of the complete demo code on GitHub here File Structure <br>
  Here are the files we will need for our application. <br>
  We will do our tempesting inside of the views folder and the rest is pretty standard Node practices.

  ```
  - views
----- partials
---------- footer.ejs
---------- head.ejs
---------- header.ejs
----- pages
---------- index.ejs
---------- about.ejs
- package.json
- server.js

  ```

Here we define our application and set it to show on port 8080. We also have to set EJS as the view engine for our Express application using `app.set('view engine', 'ejs');`. Notice how we send a view to the user by using` res.render()`. It is important to note that` res.render()` will look in a views folder for the view. So we only have to define pages/index since the full path is
 views/pages/index.

```
// load the things we need
var express = require('express');
var app = express();

// set the view engine to ejs
app.set('view engine', 'ejs');

// use res.render to load up an ejs view file

// index page
app.get('/', function(req, res) {
    res.render('pages/index');
});

// about page
app.get('/about', function(req, res) {
    res.render('pages/about');
});

app.listen(8080);
console.log('8080 is the magic port');

```

Go ahead and start the server using: <br>
`node server.js`  <br>

Now we can see our application in the browser at http://localhost:8080 and http://localhost:8080/about. Our application is set up and we have to define our view files and see how EJS works there.


























# REFERENCE 

1- [Watch EJS tutorial from WalkThroughCode on YouTube, Videos 1-5](https://www.youtube.com/playlist?list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt)

2- [ Google Books API Docs ](https://developers.google.com/books/docs/v1/using#WorkingVolumes)

3-[ EJS Docs ](https://ejs.co/)

4-[ EJS Tutorial](https://www.digitalocean.com/community/tutorials/how-to-use-ejs-to-template-your-node-application)








[main page](https://ahmad-arman.github.io/reading_note/)