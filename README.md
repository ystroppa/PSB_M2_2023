# PSB_M2_2023
Supports de cours pour PWA

Deux fichiers pour docker-compose pour exécuter deux ou trois conteneurs 
Exécution de deux conteneurs wordpress et mysql 
(attention à remplacer les répertoires par les vôtres /home/ystroppa/PSB/2023/M2/psbwordpress)

version: "3.3"

services:
  db:
    image: mysql:5.7
    volumes:
      - /home/ystroppa/PSB/2023/M2/psbwordpress/db_data:/var/lib/mysql
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: somewordpress
      MYSQL_DATABASE: wordpress
      MYSQL_USER: wordpress
      MYSQL_PASSWORD: wordpress

  wordpress:
    depends_on:
      - db
    image: wordpress:latest
    volumes:
      - /home/ystroppa/PSB/2023/M2/psbwordpress/wordpress_data:/var/www/html
    ports:
      - "9915:80"
    restart: always
    environment:
      WORDPRESS_DB_HOST: db:3306
      WORDPRESS_DB_USER: wordpress
      WORDPRESS_DB_PASSWORD: wordpress
      WORDPRESS_DB_NAME: wordpress


Exécution en ligne de commande : docker-compose -f docker-compose_2c.yml up -d 



Exécution de trois conteneurs : wordpress, mysql et phpmyadmin 



