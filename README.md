docker build -t wordpress .
docker run --name mysql -e MYSQL_ROOT_PASSWORD=password -d mysql:5.7
docker run --name wp --link mysql:mysql -p 8080:80 -d wordpress

