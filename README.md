# Django Docker Example
This project is intended to be a django-with-docker boilerplate example.  
It helps on setting up Django Projects integrating with PostgreSQL Database by running everything on Docker Containers.  

Enjoy!

## Running the project

1. Clone the repository
2. Copy-paste the `.env.example` file and name your enviroment as `.env`.
3. Build your web server using the command: `make build`

## Explaining the commands
 
 ```
 make build
 ```
  ➜ This command will:

- Stop and Delete your existing containers
- Remove old migrations (as your DB container was destroyed)
- Build brand new containers using docker-compose 
- Setup a new DB using django migrations api
- Create a superuser using username and password found in '.env' file
- Populate your DB using fixutes stored in the 'fixtures/' folder. If the fixtures are numbered, they will be loaded in numerical order.  

<br /> 


```
make start
```
  ➜ Run your containers   
<br /> 

```
make app <name>
```
  ➜ Create a new app and move it to the apps folder  
<br />
```
make logs
```
  ➜ Show your container logs (as in runserver)  
<br /> 

```
make restart
```
  ➜ Restart your containers  
<br /> 

```
make stop
```
  ➜ Stop your containers  
<br />
```
make migrate
```
  ➜ Make your migrations and migrate. Same as makemigrations followed by migrate  
<br /> 

```
make dump <app> num=<num:optional>
```
  ➜ Dump your app fixtures to the correct folder. The 'num' arg is used to define the order your fixtures should be loaded  
<br />
```
make populate
```
  ➜ Load the fixtures that are stored in the fixtures folder  
<br />
