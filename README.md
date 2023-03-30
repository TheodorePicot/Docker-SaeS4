# Docker-SaeS4

## 1. Installation de docker sous windsows 
<br>

Installation de [Docker Desktop](https://docs.docker.com/desktop/install/windows-install/)
<br>

## 2. Configuration des serveurs

<br>

Création d'un dossier docker à la racine du projet ainsi que d'un fichier docker dans ce dossier afin d'y mettre le dossier docker-compose.yml. Ce dossier va contenir l'ensemble des conteneurs nécessaire pour la virtualisation.

<br>

#### 2.1. Mise en place du fichier compose 
<ol>
Installation de PHP et Apache : 
<ol>
<li> Ajout de l'image 'php:8.2-apache' dans le fichier compose</li>
<li> Création des volumes nécessaires pour le service Apache et PHP</li>


</ol>
</ol>

<br>

```
apache:
    image: php:8.2-apache
    container_name: 'apache'
    volumes:
      - ./apache/html:/var/www/html/
      - ./apache/sites_enabled:/etc/apache2/sites_enabled
      - ./apache/php/custom-php.ini:/use/local/etc/php/conf.d/custom-php.ini
    ports:
      - "8080:80"
    networks:
      - postgres

```

virtualisation de postgres IUT avec postgis

virtualisation  