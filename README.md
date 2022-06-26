# Djangology
This project is intended to be a django boilerplate example.
It ships using docker-compose, Makefile, and a one-file enviroment (.env)
The default database schema is set to be Postgres, and it runs automatically on docker.
Enjoy!

## Running the project

1. Clone the repository
2. Copy-paste the `.env.example` file and name your enviroment as `.env`.
3. Build your web server using the command: `make build`

## Explaining the commands

 
 ```
 ➜ make build
 ```
Build your project containers. This command will always kill your existing containers and build brand new Containers from scratch. Note that your db data will also disappear.  
<br /> 
 ```
 ➜ make start
 ```
Runs your containers  
<br /> 
 ```
 ➜ make logs
 ```
Show your container logs (as in runserver)  
<br /> 
 ```
 ➜ make restart
 ```
Restart your containers  
<br /> 
 ```
 ➜ make stop
 ```
Stop your containers  
<br />
 ```
 ➜ make dump <app> num=<num:optional>
 ```
Dump your app fixtures to fixtures folder. you can use the arg 'num' to define the order your fixtures should be loaded  
<br />
 ```
 ➜ make migrate
 ```
Make your migrations and migrate. Same as makemigrations followed by migrate  
<br /> 
 ```
 ➜ make app <name>
 ```
Create a new app and move it to the apps folder  
<br />
 ```
➜  make populate
 ```
Load the fixtures that are stored in the fixtures folder  
<br />