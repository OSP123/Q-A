## JavaScript

* How does document.write work? 

    * [https://teamtreehouse.com/community/what-is-the-point-of-documentopen-and-documentclose-in-javascript](https://teamtreehouse.com/community/what-is-the-point-of-documentopen-and-documentclose-in-javascript). 

    * Document.write() will add whatever string you want to the content of your web app. If you don’t include a document.open() and a document.close(), the browser will add it for you. 

## jQuery

* What’s the difference between .html() and .text()?

    * Basically, uses .innerHTML and .textContent, respectively. .html() is supposedly faster, though: [http://stackoverflow.com/questions/1910794/what-is-the-difference-between-jquery-text-and-html](http://stackoverflow.com/questions/1910794/what-is-the-difference-between-jquery-text-and-html) 

## Firebase

* What does ref() do? 

    * "A Reference represents a specific location in your Database and can be used for reading or writing data to that Database location."([https://firebase.google.com/docs/reference/js/firebase.database.Reference](https://firebase.google.com/docs/reference/js/firebase.database.Reference))

## MySQL

* What is a thread and thread ID in MySQL?

    * A thread ID in MySQL is just the process that runs for the connection. However, there might be additional threads that are not connected; these are in the thread pool. [http://code.openark.org/blog/mysql/mysql-terminology-processes-threads-connections](http://code.openark.org/blog/mysql/mysql-terminology-processes-threads-connections)

* What is RowDataPacket? 

    * Not sure, but basically you can convert to JSON using JSON.stringify on the returned object: [https://github.com/mysqljs/mysql/issues/1330](https://github.com/mysqljs/mysql/issues/1330)

* Why use ? in WHERE for sql statements? 

    * These are parameterized statements that can take input rather than setting the input manually. This protects from SQL injection attacks and is more flexible.

* What’s the difference between mysql and mysqld?

* Why use Alter User instead of Update User?

* Why do I need a primary key in my db?

    * [http://stackoverflow.com/questions/840162/should-each-and-every-table-have-a-primary-key](http://stackoverflow.com/questions/840162/should-each-and-every-table-have-a-primary-key)

## Node.js

* What is a web client?

    * [http://www.pcmag.com/encyclopedia/term/54284/web-client](http://www.pcmag.com/encyclopedia/term/54284/web-client) "Typically, the web browser in a client’s machine".

* What is Node.js?

    * Node.js is an open-source, cross-platform JavaScript runtime environment designed to be run outside of browsers. 

    * [https://www.youtube.com/watch?v=GJmFG4ffJZU](https://www.youtube.com/watch?v=GJmFG4ffJZU) 

## Node, Express, Web Server

* What are the different http methods and how do they work?

    * [https://www.tutorialspoint.com/http/http_methods.htm](https://www.tutorialspoint.com/http/http_methods.htm) 

* What are Port Numbers?

* Difference between http and https

    * Essentially, https encrypts your data when the request is being made, so anyone looking at the data would just see gibberish. 

* What are the different parts of a url?

    * https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_URL

* What is SSL?

    * [http://info.ssl.com/article.aspx?id=10241](http://info.ssl.com/article.aspx?id=10241) 

* How do web servers work?

    * [https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_web_server](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_web_server)

    * Basically, web server hosts files and sends them based on request. Web server can work with application and database server to send information after being processed. 

* Difference between request and response?

    * **Request :** From Client to Server

    * **Response:** From Server to Client

    * **Server:** Receive Request and Send Response

    * **Client:** Send Request and Receive Response

* Inside the http package for Node, what does res.writeHead() and res.end() do?

    * [http://stackoverflow.com/questions/14243100/response-writehead-and-response-end-in-nodejs](http://stackoverflow.com/questions/14243100/response-writehead-and-response-end-in-nodejs)

    * writeHead() sends header info and end() sends body info, along with a signal that response is completed.

* What does create server and listen do in http package in Node?

    * [https://nodejs.org/api/http.html#http_http_createserver_requestlistener](https://nodejs.org/api/http.html#http_http_createserver_requestlistener)

    * createServer() takes in a function that is added to the request event. 

    *  listen() listens for a server request

* What does the error Error: listen EACCES 0.0.0.0:80 mean?

    * That is just a permissions error. Any port below 1024 needs administrative privileges to access.

* What does Postman do?

    * Tests endpoints both locally and on live sites. Is mainly used for checking data from APIs and on seeing the effect of different HTTP method requests. 

* What does Gulp do?

    * Build tool to run tasks

        * [https://www.youtube.com/watch?v=LmdT2zhFmn4](https://www.youtube.com/watch?v=LmdT2zhFmn4)

    * Competes with grunt.js

* What does Bower do?

    * Manages front-end dependencies such as jQuery, Backbone, Angular

* What are streams in Node?

    * [https://www.sitepoint.com/basics-node-js-streams/](https://www.sitepoint.com/basics-node-js-streams/)

    * Streams are unix pipes that let you easily read data from a source and pipe it to a destination. Simply put, a stream is nothing but an EventEmitter and implements some specials methods. Depending on the methods implemented, a stream becomes Readable, Writable, or Duplex (both readable and writable). Readable streams let you read data from a source while writable streams let you write data to a destination.

* What does body parser do?

    * [http://stackoverflow.com/questions/26417297/what-do-nodes-body-parser-and-cookie-parser-do-and-should-i-use-them](http://stackoverflow.com/questions/26417297/what-do-nodes-body-parser-and-cookie-parser-do-and-should-i-use-them)

    * https://www.quora.com/What-exactly-does-body-parser-do-with-express-js-and-why-do-I-need-it

    * Basically, gets the data and decodes it to whatever format you want it to be in before it hits the server.

    * When you submit form data with a POST request, that form data can be encoded in many ways. The default type for HTML forms is [application/x-www-urlencoded](http://www.w3.org/TR/html401/interact/forms.html#h-17.13.4.1), but you can also submit data as JSON or any other arbitrary format. bodyParser.urlencoded() provides middleware for automatically parsing forms with the content-typeapplication/x-www-urlencoded and storing the result as a dictionary (object) in req.body. The [body-parser](https://www.npmjs.com/package/body-parser) module also provides middleware for parsing JSON, plain text, or just returning a raw Buffer object for you to deal with as needed.

* What is req.body?

    * It is the request body from the request object: [http://expressjs.com/en/api.html#req.body](http://expressjs.com/en/api.html#req.body)

* What is browserify?

    * Makes modules that would normally only work in node work in the browser.

* What is an ORM?

    * Object/Relational Mapper allows you to use OO language to use MySQL 

## Node, Express, Handlebars

* Videos: [https://www.youtube.com/watch?v=QseHOX-5nJQ](https://www.youtube.com/watch?v=QseHOX-5nJQ) : Express, templating, routes with routing file

* What is Handlebars.js?

    * Templating engine used to reduce redundancy in HTML files

* How does it work?

    * Handlebars uses expressions, which are in {{}} form. These are then populated from a global JavaScript object. Rendering a template means you have to compile a template using Handlebars.compile(template). You can also pass in an optional "options" as a second argument. Compile function returns a new function typically saved for later use. 

        * For example,

            * Var template = "Yo, whatupppp {{name}}";

            * Var compiled = Handlebars.compile(template);

            * Var rendered = compiled({ name: "Omar" });

* What is the difference between Embedded JavaScript and Handlebars.js?

    * [https://www.slant.co/versus/181/184/~handlebars-js_vs_ejs](https://www.slant.co/versus/181/184/~handlebars-js_vs_ejs)

* How do I change the default handlebars template?

    * [http://stackoverflow.com/questions/26871522/how-to-change-default-layout-in-express-using-handlebars](http://stackoverflow.com/questions/26871522/how-to-change-default-layout-in-express-using-handlebars) 

* What is REST?

    * [http://www.restapitutorial.com/lessons/whatisrest.html](http://www.restapitutorial.com/lessons/whatisrest.html) 

* What’s the difference between __dirname, "./", and process.cwd()?

    * [http://stackoverflow.com/questions/9874382/whats-the-difference-between-process-cwd-vs-dirname](http://stackoverflow.com/questions/9874382/whats-the-difference-between-process-cwd-vs-dirname)

    * [http://stackoverflow.com/questions/16727045/node-js-express-js-relative-paths-dot-or-dirname-or-without-any-prefix/16730379#16730379](http://stackoverflow.com/questions/16727045/node-js-express-js-relative-paths-dot-or-dirname-or-without-any-prefix/16730379#16730379) 

    * [__dirname](https://nodejs.org/docs/latest/api/globals.html#globals_dirname) === where the currently executing javascript file is located

    * [process.cwd()](https://nodejs.org/docs/latest/api/process.html#process_process_cwd) returns the current working directory, i.e. the directory from which you invoked the node command.

    * ./ refers to path where the current file is. Used mostly in require. 

    * http://www.hacksparrow.com/understanding-directory-references-in-node-js.html

* What is process.env.port?

    * [http://stackoverflow.com/questions/18864677/what-is-process-env-port-in-node-js](http://stackoverflow.com/questions/18864677/what-is-process-env-port-in-node-js)

## Sequelize

* VIDEOS:

    * Sequelize short videos - informative and more for general implementation: [https://www.youtube.com/watch?v=qsDvJrGMSUY&list=PL5ze0DjYv5DYBDfl0vF_VRxEu8JdTIHlR](https://www.youtube.com/watch?v=qsDvJrGMSUY&list=PL5ze0DjYv5DYBDfl0vF_VRxEu8JdTIHlR)

    * Sequelize long video, but comprehensive (more boring, though): [https://www.youtube.com/watch?v=53bdrz7cZ-c](https://www.youtube.com/watch?v=53bdrz7cZ-c) 

* What is Sequelize?

    * An ORM node module

* JavaScript Web Tokens

    * Security: [http://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure](http://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

    * Basics of how they work: [https://medium.com/vandium-software/5-easy-steps-to-understanding-json-web-tokens-jwt-1164c0adfcec#.y21tlbljj](https://medium.com/vandium-software/5-easy-steps-to-understanding-json-web-tokens-jwt-1164c0adfcec#.y21tlbljj) 

    * Tutorial and working application from Jonathan Arellano: [https://github.com/jarellano01/Tutorial_Sails-API-Authentication](https://github.com/jarellano01/Tutorial_Sails-API-Authentication) 

* What does SET FOREIGN_KEY_CHECKS = 0 do?

* What does CASCADE Delete do?

    * [https://www.techonthenet.com/sql_server/foreign_keys/foreign_delete.php](https://www.techonthenet.com/sql_server/foreign_keys/foreign_delete.php) 

    * A foreign key with cascade delete means that if a record in the parent table is deleted, then the corresponding records in the child table will automatically be deleted. This is called a cascade delete in SQL Server.

* What does hooks: true do? For example, Manager.hasMany(models.Employee, {onDelete: 'cascade', hooks:true});

    * [http://docs.sequelizejs.com/en/latest/docs/hooks/](http://docs.sequelizejs.com/en/latest/docs/hooks/) 

    * [https://gist.github.com/OSP123/dce5d8e0eaa178b8d501792fda5973d0](https://gist.github.com/OSP123/dce5d8e0eaa178b8d501792fda5973d0)

* What does .bin/www do? [http://stackoverflow.com/questions/23169941/what-does-bin-www-do-in-express-4-x](http://stackoverflow.com/questions/23169941/what-does-bin-www-do-in-express-4-x)

## Testing

* Videos: [https://www.youtube.com/watch?v=u2XCdkL4bWI&t=842s](https://www.youtube.com/watch?v=u2XCdkL4bWI&t=842s) 

* What the hell does Morgan do?

    * [http://stackoverflow.com/questions/25468786/what-does-morgan-module-have-to-do-with-express-apps](http://stackoverflow.com/questions/25468786/what-does-morgan-module-have-to-do-with-express-apps)

    * http://stackoverflow.com/questions/23494956/how-to-use-morgan-logger

* Difference between expect, should, and assert. 

    * [http://stackoverflow.com/questions/21396524/what-is-the-difference-between-assert-expect-and-should-in-chai](http://stackoverflow.com/questions/21396524/what-is-the-difference-between-assert-expect-and-should-in-chai) 

* Assertion styles in Chai

    * [http://chaijs.com/guide/styles/](http://chaijs.com/guide/styles/) 

* Videos: 

    * [https://www.youtube.com/watch?v=CTAa8IcQh1U](https://www.youtube.com/watch?v=CTAa8IcQh1U) - Official video from site, but not as good as video from below. Video is from 2012.

    * [https://www.youtube.com/watch?v=FQwZrOAmMAc](https://www.youtube.com/watch?v=FQwZrOAmMAc) - Watch 10:00 - 20:50 for karma.config explanation. 

SEO

* Videos: [https://www.youtube.com/watch?v=mRj8YwBrLx8](https://www.youtube.com/watch?v=mRj8YwBrLx8) 

## React

* Videos: 

* What is Redux?

    * [https://www.quora.com/What-is-Redux-and-who-uses-it](https://www.quora.com/What-is-Redux-and-who-uses-it)

* What is Webpack?

    * [https://webpack.github.io/docs/what-is-webpack.html](https://webpack.github.io/docs/what-is-webpack.html) 

* When should I use webpack?

    * [http://blog.andrewray.me/webpack-when-to-use-and-why/](http://blog.andrewray.me/webpack-when-to-use-and-why/) 

* What are lifecycle methods? 

    * [https://youtu.be/pW5xnis7ABk](https://youtu.be/pW5xnis7ABk)

* What is react router and how does it work?

    * Good tutorial: [https://github.com/reactjs/react-router-tutorial/tree/master/lessons](https://github.com/reactjs/react-router-tutorial/tree/master/lessons)

* What resources are good for es6?

    * Rapid React Training

## Java

* What are Java classes and objects?

    * [https://www.tutorialspoint.com/java/java_object_classes.htm](https://www.tutorialspoint.com/java/java_object_classes.htm) 

* What are Java Packages?

    * [http://beginnersbook.com/2013/03/packages-in-java/](http://beginnersbook.com/2013/03/packages-in-java/)

    * [https://www.tutorialspoint.com/java/java_packages.htm](https://www.tutorialspoint.com/java/java_packages.htm) 

* What is autoboxing?

    * [http://stackoverflow.com/questions/27647407/why-do-we-use-autoboxing-and-unboxing-in-java](http://stackoverflow.com/questions/27647407/why-do-we-use-autoboxing-and-unboxing-in-java) 

* Why use getters and setters?

    * [http://stackoverflow.com/questions/1568091/why-use-getters-and-setters/1568230#1568230](http://stackoverflow.com/questions/1568091/why-use-getters-and-setters/1568230#1568230) 

* What is a vertex or vertices?

    * Point where two or more straight lines meet. 

* What are abstract methods and abstract classes?

    * [https://www.tutorialspoint.com/java/java_abstraction.htm](https://www.tutorialspoint.com/java/java_abstraction.htm) 

    * Abstract methods represent ideas that can be enforced in their subclasses, but are not implemented as is. 

* What is Polymorphism?

    * [https://www.tutorialspoint.com/java/java_polymorphism.htm](https://www.tutorialspoint.com/java/java_polymorphism.htm) 

* What are errors and exceptions?

    * [https://www.youtube.com/watch?v=R86ObiKhMNc](https://www.youtube.com/watch?v=R86ObiKhMNc) - Great Video on making Try/Catch blocks and creating your own exceptions

* When to handle Errors using Exceptions?

    * Whenever you have user input, File I/O, and accessing resources out of your control. 

* Does order of Exceptions matter? What are general exceptions?

    * [http://www.rapidprogramming.com/tutorial/Java-Error-Exception-exception-name-has-already-been-caught-341](http://www.rapidprogramming.com/tutorial/Java-Error-Exception-exception-name-has-already-been-caught-341) 

* Inner Classes:

    * [https://www.tutorialspoint.com/java/java_innerclasses.htm](https://www.tutorialspoint.com/java/java_innerclasses.htm) 

* Why use Streams over Collections?

    * [http://www.java8examples.com/difference-collections-streams-java-8/](http://www.java8examples.com/difference-collections-streams-java-8/) 

    * It often makes sense if we're unsure of how many items we'll receive, or if the items arrive over time. In either case, we can't use a collection, because we don't have all the items!

