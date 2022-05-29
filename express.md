# Express
- ## What is Node.js
runtime environment that allows developers to create all kinds of server-side tools and applications in JavaScript.

- ## what is Express
** It is a framework.

 ** Express is unopinionated. You can insert almost any compatible middleware you like into the request handling chain, in almost any order you like. 

- ## What does Express code look like?

 const express = require('express');

const app = express();

const port = 3000;

app.get('/', function(req, res) {

  res.send('Hello World!')
});

app.listen(port, function() {

  console.log(`Example app listening on port ${port}!`)
});

## Importing and creating modules

const express = require('express');

const app = express();

## Handling Routes

const app1 = express();

app1.get("/", handleHome);

function handleHome(req, res) {
 
}

# Every thing about npm

- npm (Node Package Manager) 

- To get started with npm, you can create an account, which will be available at http://www.npmjs.com/~*yourusername*.

- All npm packages are defined in files called package.json.

- The content of package.json must be written in JSON.
- in the terminal npm init -y

# What is TDD
“Test-driven development”

Rules
write a “single” unit test describing an aspect of the program

run the test, which should fail because the program lacks that feature

write “just enough” code, the simplest possible, to make the test pass

“refactor” the code until it conforms to the simplicity criteria

repeat, “accumulating” unit tests over time<br>
<br>

# CI/CD

CI =>Continuous Integration
CD =>Continuous Delivery
