# Dockerized Lemp
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

Docker L(inux)E(Nginx) M(ySQL) P(HP) was made to have local setup ready for development up in basically no time. 

## :tada: Startup 
Run the following commands:
1. copy the `.env.example` to `.env` 
```bash
cp .env.example .env
```
2. Start up the docker containers
```bash
docker-compose up -d
```

It will build the images and start up the containers. Afterwards you should be able to see the phpinfo() output on the exposed port: `8081`.
Open the following URL in your preferred browser: `http://localhost:8081`
Now you are ready to just drop your PHP code inside the `/src` folder.

### Stop the containers
`docker-compose stop`

### Initial MySQL data 
Do you need to have initial MySQL data? No worries I got you! Just drop your SQL file inside the 

`./docker/mysql/` folder. There is an empty SQL file already. This will be imported on container start up.

## :gear: Configs 
To change the version of Nginx, PHP or MYSQL take a look at `.env `file. After this run the build again with the following command:

```bash
docker-compose up -d --build
```

## :beetle: Debugging
Xdebug is enabled by default. It is running on port `9003` . Other configs for a specific service can be found in `/etc/` folder.
In order to check everything works just comment in the __xdebug_info()__ inside `./src/index.php`
