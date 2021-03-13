#Dockerized Lemp by Padawan
###Startup
Copy the **.env.example** file to **.env** and run the up command:  
`docker-compose up -d`

It will build the images when you run it for the first time. Afterwards you should be able to see the phpinfo() on
http://localhost:8081/ in your preferred browser.

###Configs
To change the version of Nginx, PHP or MYSQL take a look at .env file. After this run the build again.  

`docker-compose up -d --build`

Other configs for the specific services can be found in **/etc/** folder.

###Stop the containers
`docker-compose stop`