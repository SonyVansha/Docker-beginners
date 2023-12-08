# Docker Beginner

## start the application with Docker

### Project Setup

```sh
npm install
```

### Create mongo network

```sh
docker network create mongo-network 
```

### Setup mongoDB

```sh
docker run -d -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password --name mongodb --net mongo-network mongo
```

### Setup mongo-express

```sh
docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password --net mongo-network --name mongo-express -e ME_CONFIG_MONGODB_SERVER=mongodb mongo-express   
```

### Open mongo-express from browser

```sh
http://localhost:8080
```
username = admin
password = pass

### Run Server nodejs

```sh
node server.js
```

### Access application

```sh
http://localhost:3000
```

## Using Docker Compose

## Use Auto Yaml
```sh
docker-compose -f docker-compose.yaml up
```

### Run Server nodejs

```sh
node server.js
```

### Access application

```sh
http://localhost:3000
```