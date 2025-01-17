# Accès la base de données.



## Explications:
Dans ce tuto, vous allez permettre à Qgis de se connecter à la base de données. Pour cela, il faut déposer certains fichiers
qui vous auront été envoyés par le SI  - ce sont les certificats.
Pour cela, il faudra dézipper ce fichier, copier-coller son contenu dans un dossier spécifique. 
Ce répertoire peut être masqué par défaut, on utilisera donc une méthode particulière pour y accéder. 

Cette opération doit être renouvelée tous les ans, les certifiats vous identifiant à la base de données ayant une durée
limitée pour des raisons de sécurité. 


## Pas à pas

 _Vous avez reçu un fichier zip permettant le paramétrage de la connexion de la part du service informatique_
 
 _Vous êtes bien connecté sur votre session._


- Télécharger le fichier zip 
- Dézipper le fichier reçu dans un dossier. 
- Aller dans le dossier AppData. Deux façons de faire sont possibles:
	- 1- _Recommandé_ :Appuyer sur  _touche windows + R_ (la touche windows se trouve entre Ctrl et Alt) puis entrer la commande "%AppData%"
	- 2- Naviguer manuellement dans l'explorateur de fichiers jusqu'à
```
C:\Users\ *[nomdelasession]* \AppData\Roaming
```

- Vérifier si un dossier "postgresql" existe dans ..\AppData\Roaming  
- Sinon, le créer.

- Copier dans ce dossier tous les fichiers du zip à votre nom, y compris - et surtout - le fichier masqué .pg_service.conf. S'ils existent déjà, les remplacer.


- Lancer Qgis

- Ouvrir le gestionnaire de sources de données (Onglet "Couche>Gestionnaire de source de données" ou Ctrl+L) 

- Cliquer sur PostgreSQL dans la barre de gauche
<img src="./img/gestionnaire_sources_pg.png" alt= “” width="50%" height="50%"> 

- Vérifier que la connexion "Service projets" est disponible, et se connecter

_La liste des tables et schémas accessibles devrait apparaître._

_Vous pourrez aussi directement charger des projets directement depuis:_
> Projet > Ouvrir depuis... > PostgreSQL

_Puis en choisissant la connexion "Service projets" et le schéma concerné._




