# course information

Simple project contains the information about course, number of exercises.



# Prerequisites

Install [node]
v12.18.2
is working well for that simple project but you can use others.
```
curl -sL https://deb.nodesource.com/setup_14.x | bash
sudo apt install -y nodejs
```

Install all packages with `npm install`

# Starting in production mode

First you need to build the static files with `npm run build`

An example for serving static files:
Use npm package called serve to serve the project in port 5000:
- install: `npm install -g serve`
- serve: `serve -s -l 5000 build`

Test that the project is running by going to <http://localhost:5000>


# Starting in developement mode

Start the developement server with `npm start`
Test that the project is running by going to <http://localhost:3000>
