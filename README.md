# BUILD IMAGE 
$ build -t=NAME PATH         #start image from dockerfile
$ docker run -p 4000:80 NAME #connect to port 4000 localhost

# ADD DATABASE
$  docker run --name wpdb -e MYSQL_ROOT_PASSWORD=MyPassword1! -d mysql:latest

#Connect to MySQL from the MySQL command line client
$ docker run -it --network wp-network --rm mysql mysql -hwpdb -uroot -p

# CREATE NETWORK
$ docker network create NAME
$ docker network connect NETWORKNAME NAME --alias ALIAS;
$ docker network connect NETWORKNAME NAME --alias ALIAS
