# Classes
- **Creat new class**

let Rectangle = class {

  constructor(height, width) {

    this.height = height;

    this.width = width;
  }
};

- **Body ,constrctor and method**

class Rectangle {

  constructor(height, width) {

    this.height = height;

    this.width = width;
  }

  // Getter

  get area() {

    return this.calcArea();
  }

  // Method

  calcArea() {

    return this.height * this.width;
  }
}

# Routing

- **Create basic route**

const express = require('express')

const app = express()

// respond with "hello world" when a GET request is made to 
the homepage

app.get('/', (req, res) => {

  res.send('hello world')
})

- **Route methods**

1- GET

2-POST

3-DELETE

4-PUT

- **Route paths**

This route path will match requests to the root route, /.


app.get('/', (req, res) => {

  res.send('root')

})

   - **Route parameters**

app.get('/users/:userId/books/:bookId', (req, res) => {

  res.send(req.params)

})

- **Route handlers**

app.get('/example/a', (req, res) => {

  res.send('Hello from A!')

})

*callback function can be one function ,array of function or a combination of independent functions


- **Response methods**


res.download()  <>	Prompt a file to be downloaded.

res.end()<>	End the response process.

res.json()<>	Send a JSON response.

res.jsonp()	<>Send a JSON response with JSONP support.

res.redirect()<>	Redirect a request.

res.render()<>	Render a view template.

res.send()<>	Send a response of various types.

res.sendFile()<>	Send a file as an octet stream.

res.sendStatus()<>	Set the response status code and send   its string representation as the response body.

# Express Routing

**Express Router :It is a mini express application without all the bells and whistles of an express application, just the routing stuff**

- **Basic Routes express.Router()**

 var router = express.Router();

 // route middleware that will happen on every request

    router.use(function(req, res, next) {

        // log each request to the console

        console.log(req.method, req.url);

        // continue doing what we were doing and go to the 
        
        route
        
        next();
    });

    // home page route (http://localhost:8080)

    router.get('/', function(req, res) {

        res.send('im the home page!');
    });

      app.use('/', router);

 - **Route with Parameters** 


        router.get('/hello/:name', function(req, res) {

        res.send('hello ' + req.params.name + '!');
         });


   we can use Express’s .param() middleware

         router.param('name', function(req, res, next, name) {
       
        console.log('doing name validations on ' + name);

        
        req.name = name;
        
        next();
    });

- **Conclusion**


-Use express.Router() multiple times to define groups of routes

-Apply the express.Router() to a section of our site using app.use()

-Use route middleware to process requests

-Use route middleware to validate parameters using .param()

-Use app.route() as a shortcut to the Router to define multiple requests on a route
