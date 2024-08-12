docker-compose.yml

version: '3.8'

services:
  wordpress:
    image: wordpress:latest
    ports:
      - "8000:80"
    environment:
      WORDPRESS_DB_HOST: db:3306
      WORDPRESS_DB_NAME: wordpress
      WORDPRESS_DB_USER: exampleuser
      WORDPRESS_DB_PASSWORD: examplepass
    volumes:
      - wordpress_data:/var/www/html
    depends_on:
      - db

  db:
    image: mysql:5.7
    environment:
      MYSQL_ROOT_PASSWORD: rootpassword
      MYSQL_DATABASE: wordpress
      MYSQL_USER: exampleuser
      MYSQL_PASSWORD: examplepass
    volumes:
      - db_data:/var/lib/mysql

volumes:
  wordpress_data:
  db_data:

nmap installatation in docker.


# Use a base image with your preferred OS
FROM ubuntu:latest

# Update package lists and install Nmap
RUN apt-get update && \
    apt-get install -y nmap

# Set the default command
CMD ["bash"]

docker build -it foldername .


docker run -it file name 


copy file from local to container 

rohit@rohit-Virtual-Box:~$ pwd
/home/rohit
rohit@rohit-Virtual-Box:~$ docker cp /home/rohit/myhero.txt  2e527842e45d:/myfiles

Successfully copied 2.05kB to 2e527842e45d:/myfiles
rohit@rohit-Virtual-Box:~$

  
