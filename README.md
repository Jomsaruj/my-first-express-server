# my-first-express-server
Here is my first experience with NodeJS web application framework - Express

### How to add express to your project

NOTE: you can start with only empty server.js file in your directory, commands below will generate the rest to you automatically

0. make sure you have node installed on your computer
1. open terminal
2. cd to the directory
3. enter ```node npm init``` (npm will let you enter some infomation, if you do not want to input anything, you can just press ENTER for every step, it is fine)
4. enter ```npm install express```

### How to run server

NOTE: at this step, I have already modified server.js by add this command to the code.

```
const express = require("express");
const app = express();

app.get("/", function(request,response){
	response.send("<h1>This is root page</h1>");
})

app.listen(3000, function(){
	console.log("Server started on port 3000");
});

```

1. open terminal
2. cd to the directory
3. enter ```node server.js``` to run server
4. open your search engine to localhost:3000(depend on your defined port)
5. you should see word "This is root page" (at root)
6. This is how to create express server
7. you also can add different routes, see more in server.js

### How to response to request with HTML file

1. create index.html with HTML code that you like
2. create new route(if needed) and use command ``` sendFile``` as below

```
app.get("/calculator", function(request,response){
	response.sendFile(__dirname + "/index.html");
})
```
NOTE: __dirname command will seek for path before reach index.html file

At this step, if you run ```node server.js``` again and go to localhost:3000/calculator you will see your HTML file render there
