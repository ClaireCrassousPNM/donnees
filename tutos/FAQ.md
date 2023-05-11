# F.A.Q.

_Vous trouverez dans ce fichier une liste de probl�mes et questions fr�quentes avec des solutions simples. 
En cliquant en haut � gauche de cette fen�tre vous avez acc�s � la table des mati�res pour chercher directement la question qui vous int�resse_




## Dans QGIS

### Message d'erreur " L'entit� ...  a une g�om�trie non valide" pendant un g�otraitement
M�me si elles ne sont pas formul�es, les g�om�tries dans Qgis r�pondent � des r�gles. Une entit� invalide peut tout de m�me �tre affich�e, mais
toute tentative de traitement, ou de jointure avec une autre couche renverra cette erreur. 

_Solution_

- > "R�parer les g�om�tries": dans la bo�te � outil de Qgis se trouve un outil "R�parer les g�om�tries" qui peut tenter de r�parer les erreurs de g�om�tries.

- > Modification manuelle: Si le message d'erreur donne les identifiants des entit�s aux g�om�tries incorrectes, il est possible de les examiner et 
modifier manuellement pour corriger les �ventuelles erreurs. 

## Impossible de charger un projet depuis la base de donn�es PostgreSQL
Il existe plusieurs cas de figures:

- 1. Vous ne disposez pas d'un acc�s � la base de donn�es

_Solution_

> Si vous �tes bien sur votre poste de travail, et que c'est la premi�re fois que vous vous connectez � la base de donn�es contacter le SI.


- 2. Vous pouvez charger des couches depuis la base de donn�es en passant par le gestionnaire de sources de donn�es

_Solution_

> Dans le Gestionnaire de source de donn�es, s�lectionner l'onglet "PostgreSQL". Puis s�lectionner la connexion "Service projets". Enfin, cliquer sur "Editer". 
Une nouvelle fen�tre s'affiche en bas de laquelle se trouve la case � cocher "Permettre l'enregistrement et le chargement de projets QGIS dans la base de donn�es. "