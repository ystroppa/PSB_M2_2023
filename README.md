# PSB_M2_2023
Supports de cours pour PWA

Deux fichiers pour docker-compose pour exécuter deux ou trois conteneurs  <br />
Exécution de deux conteneurs wordpress et mysql   <br />
<br />
-- Exemple : docker_compose_2c.yml --- <br />
Attention à deux éléments : la localisation des volumes et le port ouvert sur wordpress 
(attention à remplacer les répertoires par les vôtres /home/ystroppa/PSB/2023/M2/psbwordpress)  <br />
<br />
<br />
Exécution en ligne de commande : docker-compose -f docker-compose_2c.yml up -d  <br />
<br />
Pour accèder au service sasiir sous un navigateur l'url http://localhost:9995  <br />
<hr />
Exécution de trois conteneurs : wordpress, mysql et phpmyadmin  <br />
<br />
-- Exemple : docker_compose_3c.yml --- <br />
Attention à deux éléments : la localisation des volumes et le port ouvert sur wordpress 
(attention à remplacer les répertoires par les vôtres /home/ystroppa/PSB/2023/M2/psbwordpress)  <br />
<br />
<br />
Exécution en ligne de commande : docker-compose -f docker-compose_3c.yml up -d  <br />
<br />
Pour accèder au service sasiir sous un navigateur l'url http://localhost:9996  <br />
<hr />




