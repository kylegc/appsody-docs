---
title: "Appsody Quick Start"
---

# Appsody Quick Start

## Installing Appsody

Prerequisite: In order to use Appsody, [Docker](https://docs.docker.com/install/) must be installed and running.

On MacOS, run the following commands:
```
brew tap appsody/appsody
brew install appsody
```
On other OSs, check out the [complete installation guide]().

## Using Appsody

Creating a new Appsody project is easy! With only a few commands, you will have a containerized development environment running with the stack of your choice!

First, create a new directory for the project and run `appsody init stack` to download the template project.
```
mkdir my-project
cd my-project
appsody init nodejs-express
```
Tip: You can view other available stacks with `appsody list`

Now you have a fully functional project Appsody project. Start the development container.
```
appsody run
```
Great! Now the project is running in a docker container, and the container is linked to the project source code on your local system. For nodejs-express, navigate to http://localhost:3000 to see the output (other stacks may use a different URL). 

Finally, lets try changing the code. Edit the file `app.js` to output something other than "Hello World!". Upon saving the file, Appsody will pickup the change and automatically update the container. Refresh http://localhost:3000 to see the new message!

You are ready to continue developing your application. To stop the container, press ctrl-c in the terminal or run `appsody stop`. To enable the debugger, run `appsody debug`. 

Finally, when you are ready to publish a production docker image, run `appsody build`. 


<!-- This will be documentation for a quick install of the CLI and using the appsody CLI's basic commands
This will include a quick start video? 
(appsody init, run) (links to videos / demos?) -->