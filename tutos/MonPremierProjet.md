# Mon Premier projet

_Vous avez re�u des la confirmation du SI que vous �tes autoris� � utiliser la base de donn�es du parc ? Voil� comment faire !_


_Ce tutoriel contient les �tapes pour la consultation d'un projet existant, ainsi que les possibles op�rations � r�aliser pour en faciliter la visualisation._

> Sc�nario: On vous a demand� d'�tablir pour certaines zones la pr�sence ou l'absence d'une esp�ce v�g�tale donn�e. 
> 
> Pour cela, vous devez consulter un projet Qgis, faire vos relev�s terrains, puis entrer les r�sultats en modifiant une couche existante.


## Acc�s � la base de donn�es
_Cette partie reprend le processus d�crit dans [ce tutoriel](./Acces_BD.md)._
### 1. V�rifier que vous avez bien acc�s � la base de donn�es par Qgis. 

Pour cela vous pouvez t�l�charger le projet � [ce lien]() et tenter de le lancer. Si les couches s'affichent bien, vous pouvez continuer,
sinon contacter le SI. 


### 2. Charger l'ensemble des connexions

Vous devez aussi avoir re�u un fichier zip permettant le param�trage de la connexion de la part du service informatique.

Enregistrer et d�compresser si n�cessaire ce fichier zip contenant le fichier "service projets.xml".

D�placer ce fichier dans un dossier o� il sera facile � retrouver.
 
> Exemple: C:\Users\VotreNom\Documents\QgisXML


Une fois Qgis lanc�, vous pouvez ouvrir le gestionnaire de sources de donn�es (Onglet "Couche>Gestionnaire de source de donn�es" ou Ctrl+L) 

<img src="./img/gestionnaire_sources.png" alt= �� width="50%" height="50%"> 


- Cliquer sur PostgreSQL dans la barre de gauche

<img src="./img/gestionnaire_sources_pg.png" alt= �� width="50%" height="50%"> 

- Cliquer sur "charger" et retrouver le fichier "service projets.xml" que vous venez de copier


- V�rifier que la connexion "Service projets" est disponible, et se connecter

_La liste des tables et sch�mas accessibles devraient appara�tre._



_NB: Le gestionnaire de donn�es est le moyen � privil�gier pour importer des donn�es au projet courant. (Les autres fa�ons d'ajouter des couches peuvent cr�er des probl�mes en appliquant des param�tres d'import par d�faut)_

_Cette �tape visait � v�rifier la connexion � la base de donn�es. Maintenant nous allons charger effectivement des donn�es._

### 3. Charger le projet d'int�r�t

Pour cela, cliquer sur l'onglet projet en haut � gauche de la fen�tre Qgis: Projet>Ouvrir Depuis>PostgreSQL

<img src="./img/charger_projet.png" alt= �� width="50%" height="50%"> 

Ensuite vous aurez acc�s � la liste des serveurs disponibles. 
Ici, il s'agit du projet "Mon premier projet" dans le sch�ma "tutos".



## Visualisation des donn�es du projet
_Vous avez bien r�ussi � charger le projet "MonPremierProjet" et voyez des couches, nous allons maintenant passer en revue 
les moyens de naviguer dans le projet et observer les donn�es._

0. Enregistrer le projet en local

Vous pouvez � tout moment "enregistrer sous" un projet qui est enregistr� sur le serveur. 
Cela en cr�e une copie qui ne sera plus accessible qu'� vous, 
mais que vous pourrez modifier sans risquer de perdre le travail de vos coll�gues.


1. Afficher/masquer des couches

_Dans Qgis, la position de la plupart des �l�ments est personnalisable, et il arrive qu'on les modifie par accident. 
Auquel cas on pourra les retrouver dans l'onglet "Vue", et v�rifier que le panneau ou la barre d'outils concern�e est bien visible._


<img src="./img/vue_panneaux_barres.png" alt= �� width="30%" height="30%"> 

A gauche de chaque couche se trouve une petite boite qui peut �tre coch�e ou d�coch�e. 
Cette boite permet d'afficher ou de masquer chaque couche, ou �l�ment de symbologie d'une couche.




2. Les propri�t�s

Double cliquer sur une couche, ou faire "clic droit > Propri�t�s" en affiche les propri�t�s. 

_**Le d�tail de la table attributaire n'est pas visible dans les propri�t�s**_

L� vous avez acc�s � une s�rie d'onglet donnant des informations sur la couche en question. 
L'onglet "Information" est particuli�rement important pour:
- v�rifier la source des donn�es (si vous travaillez sur des donn�es stock�es sur votre machine, le chemin d�taill� vers le fichier apparaitra, 
si vous travaillez sur le serveur ce seront les param�tres de connexion qui seront visibles).
- v�rifier le type de donn�es ( raster/vecteur, type de g�om�trie) et la projection
- v�rifier le d�compte d'entit� (il s'agit du d�compte apr�s application du filtre)



3. Les filtres

Vous pouvez remarquer un symbole : <img src="./img/symbole_filtre.png" alt= �� width="05%" height="05%"> 
 � droite de certaines couches:


<img src="./img/filtres_dans_fenetre.png" alt= �� width="30%" height="30%"> 




Il signifie que la couche en question est filtr�e. Les filtres sont des outils tr�s puissants, notamment pour limiter la charge sur vos ordinateurs. 
Ils sont appliqu�s au niveau du serveur, et permettent de ne charger que les entit�s d'une couche que vous aurez choisies par une expression. 

Par exemple, en cliquand sur le symbole filtre de XXXXXX ou en faisant clic droit > Filtre sur cette couche vous voyez l'expression suivante :



qui signifie: 



_Certaines couches du serveur sont charg�es par d�faut avec des filtres. Il est tout � fait possible de les modifier pour acc�der � d'autres donn�es, 
ou de restreindre encore le filtre propos�_

<!--
_Les filtres sont aussi visibles en dans les propri�t�s d'une couche, � l'onglet "Source". Ce n'est pas tr�s intuitif...._  
--> 

4. La table attributaire

Les couches au format vecteur (qu'est-ce que c'est?) contiennent une table attributaire, donnant des informations sur les donn�es qu'elles contiennent. 
Vous pouvez visualiser cette table en cliquant droit sur la couche puis sur "Ouvrir la table d'attributs".

<img src="./img/ouvrir_latable_attribut.png" alt= �� width="15%" height="50%"> 


Il existe deux fa�ons de repr�senter la table attributaire. Une vue "Table" et une vue "Formulaire". On peut basculer de l'une � 
l'autre en cliquant sur l'icone correspondante en bas � droite de la fen�tre. 



<img src="./img/tableattributaire.png" alt= �� width="15%" height="50%">  <img src="./img/tableattributaire_form.png" alt= �� width="15%" height="50%"> 

_A gauche, la table atributaire en format table. A droite,en format formulaire. Le mode table permet de visualiser d'un coup d'oeil l'ensemble des entit�s et attributs simultan�ment.
Le mode formulaire permet de visualiser et dles entit�s une � une, la liste des entit�s apparaissant sur la gauche._



## Modification d'une couche




<!--
### Autoriser le chargement des projets

<img src="./img/editerconnexion_chargerprojets.png" alt= �� width="50%" height="50%">  -->
