

# Glossaire

### Base de donn�es
Au sens large, une base de donn�e permet de stocker des donn�es. 

On parle de base de donn�es relationnelles quand ces donn�es sont structur�es en tables, g�rant de fa�on explicite les relations entre entit�s. C'est le cas de la base de donn�es du Parc du Mercantour qui est d�crite dans ce d�p�t. 

Les logiciels permettant de g�rer ces bases de donn�es sont appel�s des Syst�mes de Gestions de Bases de Donn�es Relationnelles (SGBDR). 

### Couche
Dans un projet Qgis, une couche est une repr�sentation de donn�es spatialis�e. Elle contient le lien vers le fichier contenant la donn�es, ainsi que les informations permettant sa repr�sentation (notamment sa symbologie).
Une couche _n'est pas_ en elle m�me de la donn�e, mais le lien vers une donn�e. 

On peut toutefois, depuis Qgis �diter et changer les donn�es vers lesquelles une couche renvoie (notamment en activant l'outil "�diter").

### D�p�t
Un d�p�t git est un entrep�t virtuel, qui permet d'enregistrer et de maintenir facilement du code et de la documentation, notamment par la gestion de versions.

### Projet
Un projet Qgis contient un ensemble de couches, les informations permettant de les repr�senter, ainsi que l'ensemble des param�tres conditionnant la r�alisation de g�otraitements. 
En tant que tel, un projet Qgis ne contient **pas** de donn�es, mais des liens (ou chemins) vers des donn�es, repr�sent�es sous formes de couches. 


### Raster
En g�omatique, un raster est l'un des deux modes principaux de repr�sentation des donn�es spatiales. A la fa�on d'une photographie, il stocke l'information spatiale dans une matrice r�guli�re de pixels, contenant chacun une information chiffr�e.

Une matrice dans un raster est appel�e "bande". Un raster peut �tre multi-bandes, c'est-�-dire contenir plusieurs matrices superpos�es - � la fa�on d'une photographie qui contient tois matrices: rouge-vert-bleu. 

Un raster est caract�ris� par sa "r�solution spatiale" qui est d�finie par la taille de ses pixels. 


### Sch�ma
Dans une base de donn�es relationnelle, un sch�ma regroupe diff�rents objets dont des tables, vues et fonctions. 
Il permet d'organiser le contenu d'une base de donn�es en th�matique, de mani�re similaire � un dossier dans un r�pertoire de fichier - on ne peut pas cependant imbriquer un sch�ma dans un autre. 

Dans la base de donn�es du parc, un sch�ma sp�cifique est d�di� � chaque principale th�matique (i.e. : ag_pasto, flore, limites). Ce d�p�t contient pour les principaux sch�mas la documentation permettant d'en comprendre le contenu. 

### Vecteur
En g�omatique, un vecteur est l'un des deux modes principaux de repr�sentation des donn�es spatiales. 
Il est bas� sur l'utilisation de coordonn�es qui permettent de localiser des points d�finissant la g�om�trie de chaque entit�.

Dans Qgis un vecteur peut contenir soit: 
- des points, 
- des lignes, 
 - des polygones. 
Chaque entit� est caract�ris�e par sa g�om�trie (les coordonn�es des points la composant), et des attributs qui peuvent �tre variables. 


