# PSB_M2_2023
Supports de cours pour PWA

Deux fichiers pour docker-compose pour exécuter deux ou trois conteneurs 
Exécution de deux conteneurs wordpress et mysql 
(attention à remplacer les répertoires par les vôtres /home/ystroppa/PSB/2023/M2/psbwordpress)

version: "3.3" <br />
services: <br />
  db:  <br />
    image: mysql:5.7  <br />
    volumes:  <br />
      - /home/ystroppa/PSB/2023/M2/psbwordpress/db_data:/var/lib/mysql <br />
    restart: always <br />
    environment: <br />
      MYSQL_ROOT_PASSWORD: somewordpress <br />
      MYSQL_DATABASE: wordpress   <br />
      MYSQL_USER: wordpress       <br />
      MYSQL_PASSWORD: wordpress   <br />
<br />
  wordpress:   <br />
    depends_on:   <br />
      - db   <br />
    image: wordpress:latest   <br />
    volumes:    <br />
      - /home/ystroppa/PSB/2023/M2/psbwordpress/wordpress_data:/var/www/html   <br />
    ports:    <br />
      - "9915:80"    <br />
    restart: always    <br />
    environment:   <br />
      WORDPRESS_DB_HOST: db:3306    <br />
      WORDPRESS_DB_USER: wordpress   <br />
      WORDPRESS_DB_PASSWORD: wordpress   <br />
      WORDPRESS_DB_NAME: wordpress   <br />
<br />

Exécution en ligne de commande : docker-compose -f docker-compose_2c.yml up -d 



Exécution de trois conteneurs : wordpress, mysql et phpmyadmin 



