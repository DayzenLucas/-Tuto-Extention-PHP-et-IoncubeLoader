# Extention-PHP-et-IoncubeLoader
Extention PHP et IoncubeLoader

Installation des Extensions PHP
Il suffit tout simplement de copier les lignes les une après les autres !

 

#Attention remplacer le php7.4 par votre versions PHP

#Pour savoir votre versions php
php -v


#Installations des paquets
```
apt install php-zip 
apt install php7.4-dom 
apt install php7.4-xmlreader 
apt install php7.4-gd
apt install php7.4-bcmath
apt install php-curl
apt install grub-pc-bin  
```
                                         
#Vérification des mises a jours en cas d'erreurs       
```
sudo apt update && sudo apt dist-upgrade 
```
#Extensions NON PHP mais très utiles
```
apt-get install libxml-parser-perl libpath-class-perl perl-modules screen rsync sudo e2fsprogs unzip subversion pure-ftpd libarchive-zip-perl libc6 libgcc1 git curl
```
Voila vous avez installer quelques Extensions importantes pour votre serveur !


Installation IONcube_Loader
Pour l'installation du loader , commencer par télécharger le paquet suivant : 

```
wget http://downloads3.ioncube.com/loader_downloads/ioncube_loaders_lin_x86-64.tar.gz
Extraction et direction du paquet :

tar xzf ioncube_loaders_lin_x86-64.tar.gz -C /usr/local

Installation de la libs 
```

#Vérification de la versions php
php -v

#Installation du Paquet FPM
```
apt install php7.4-fpm

#ou

apt install php-fpm
```

#N'oublier pas de modifier le 7.4 de la versions php par la votre !

#AJOUTER DANS LE 1ER LIGNE DES FICHIES CI-DESSOUS
```
zend_extension = /usr/local/ioncube/ioncube_loader_lin_7.4.so
```
#modification des services php
```
sudo nano /etc/php/7.4/cli/php.ini
sudo nano /etc/php/7.4/fpm/php.ini
sudo nano /etc/php/7.4/apache2/php.ini

sudo systemctl restart apache2
sudo systemctl restart php7.4-fpm
```
#ou
```
sudo systemctl restart apache2
sudo systemctl restart php-fpm
```
Vérification de la libs si elle ses biens .
php -v

PHP 7.4.14-6+ubuntu18.04.1+deb.sury.org+1 (cli) (built: Feb  5 2020 16:51:13) ( NTS )
Copyright (c) 1997-2018 The PHP Group
Zend Engine v3.3.14, Copyright (c) 1998-2018 Zend Technologies
    with the ionCube PHP Loader + ionCube24 v10.3.9, Copyright (c) 2002-2019, by ionCube Ltd.
    with Zend OPcache v7.3.14-6+ubuntu18.04.1+deb.sury.org+1, Copyright (c) 1999-2018, by Zend Technologies
Voila tout est installer !
