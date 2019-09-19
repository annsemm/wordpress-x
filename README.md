# BUILD IMAGE 
$ build -t=NAME PATH         #start image from dockerfile
$ docker run -p 4000:80 NAME #connect to port 4000 localhost

# ADD DATABASE
$  docker run --name wpdb -e MYSQL_ROOT_PASSWORD=MyPassword1! -d mysql:latest #create database

$ docker run -it --network wp-network --rm mysql mysql -hwpdb -uroot -p #Connect to MySQL from the MySQL command line client

# CREATE NETWORK
$ docker network create NAME

$ docker network connect NETWORKNAME NAME --alias ALIAS

$ docker network connect NETWORKNAME NAME --alias ALIAS


# OR USE DOCKER-COMPOSE.YML

$ docker-compose up -d #from working directory run 


$ docker-compose down #remove containers and default network, but preserves WordPress database


$ docker-compose down --volumes #remove everything with database
