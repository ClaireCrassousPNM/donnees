# F.A.Q.

_Vous trouverez dans ce fichier une liste de probl�mes et questions fr�quentes avec des solutions simples._

_En cliquant en haut � gauche de cette fen�tre vous avez acc�s � la table des mati�res pour chercher directement la question qui vous int�resse_




## Recherche de donn�es

### Je souhaite importer des courbes de niveau dans mon projet Qgis. 



## Dans QGIS

### Ma table ne montre pas toutes les entit�s. 

Vous pouvez v�rifier le nombre d'entit�s contenu dans une couche en passant par:
> clic droit sur la couche > Propri�t�s > Information : D�compte d'entit�s
Si ce nombre ne correspond pas au nombre d'entit�s dans la table d'attribut vous pouvez appliquer la solution ci-dessous. 

_Solution_

En bas � droite de de la fen�tre de la table d'attributs se trouve une petite ic�ne avec un menu d�roulant "Ne montrer que les entit�s visibles sur la carte", 
vous pouvez choisir � la place l'option "Montrer toutes les entit�s" si vous savez que la taille de la table d'attributs n'est pas trop grande pour la m�moire de votre machine. 


### Message d'erreur " L'entit� ...  a une g�om�trie non valide" pendant un g�otraitement
M�me si elles ne sont pas formul�es, les g�om�tries dans Qgis r�pondent � des r�gles. Une entit� invalide peut tout de m�me �tre affich�e, mais
toute tentative de traitement, ou de jointure avec une autre couche renverra cette erreur. 

_Solution_

- > "R�parer les g�om�tries": dans la bo�te � outil de Qgis se trouve un outil "R�parer les g�om�tries" qui peut tenter de r�parer les erreurs de g�om�tries.

- > Modification manuelle: Si le message d'erreur donne les identifiants des entit�s aux g�om�tries incorrectes, il est possible de les examiner et 
modifier manuellement pour corriger les �ventuelles erreurs. 

### Impossible de charger un projet depuis la base de donn�es PostgreSQL
Il existe plusieurs cas de figures:

- 1. Vous ne disposez pas d'un acc�s � la base de donn�es

_Solution_

> Si vous �tes bien sur votre poste de travail, et que c'est la premi�re fois que vous vous connectez � la base de donn�es contacter le SI.


- 2. Vous pouvez charger des couches depuis la base de donn�es en passant par le gestionnaire de sources de donn�es

_Solution_

> Dans le Gestionnaire des sources de donn�es (Onglet "Couche > Gestionnaire des sources de donn�es" ou CTRL + L), s�lectionner l'onglet "PostgreSQL". Puis s�lectionner la connexion "Service projets". Enfin, cliquer sur "Editer". 
Une nouvelle fen�tre s'affiche en bas de laquelle se trouve la case � cocher "Permettre l'enregistrement et le chargement de projets QGIS dans la base de donn�es. "

### Je ne vois pas les projets, mais seulement les tables de la base de donn�es

 Faire un clic droit sur Postgis/Service Projets dans l'explorateur, cliquer "Editer la connexion" et cocher "Permettre le chargement et l'enregistrement de projets QGIS" puis "OK".
 [Illustration](#Autoriser-le-chargement-des-projets)




## Illustration

#### Autoriser le chargement des projets

<img src="./img/editerconnexion_chargerprojets.png" alt= �� width="50%" height="50%"> 