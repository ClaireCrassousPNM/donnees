# Acc�s la base de donn�es.


## Avant de commencer

 - _Vous avez re�u un fichier zip permettant le param�trage de la connexion de la part du service informatique_
 - _Vous �tes bien sur une session windows qui n'est pas partag�e._
 - _Vous pouvez charger les couches du projet "Strategie flore.qgz" - t�l�chargeable [ici](./ressources/Strategie_Flore.qgz)._



## Etapes de param�trage � l'aide du fichier xml

- T�l�charger le fichier zip 

<!-- Naviguer jusqu'au dossier AppData.

Il se trouve typiquement dans un chemin ressemblant �:
```
C:\Users\ *[nomdelasession]* \AppData\Roaming
```
Le fa�on la plus simple de l'atteindre consiste � appuyer sur  _touche windows + R_, 
puis � entrer la commande "%AppData%" dans l'invit� de commande (la touche windows se trouve entre Ctrl et Alt). [Illustration](#Acces-au-dossier-AppData)

(Ce r�pertoire est masqu� par d�faut, il est aussi possible de naviguer jusqu'� lui, en autorisant
l'affichage des fichiers cach�s dans les options)

- Cr�er un dossier "postgresql" dans le dossier AppData\Roaming s'il n'existe pas
- Copier dans ce dossier tous les fichiers du zip, y compris le fichier masqu� .pg_service.conf
(les remplacer s'ils existent d�j�)
-->
- Enregistrer et d�compresser si n�cessaire le fichier zip contenant le fichier "service projets.xml".

- D�placer ce fichier dans un dossier o� il sera facile � retrouver.
 
> Exemple: C:\Users\VotreNom\Documents\QgisXML


- Lancer Qgis

- Ouvrir le gestionnaire de sources de donn�es (Onglet "Couche>Gestionnaire de source de donn�es" ou Ctrl+L) [Illustration](#Gestionnaire-de-sources-de-donnees)

- Cliquer sur PostgreSQL dans la barre de gauche

- Cliquer sur "charger" et retrouver le fichier "service projets.xml" que vous venez de copier

- V�rifier que la connexion "Service projets" est disponible, et se connecter

_La liste des tables et sch�mas accessibles devraient appara�tre._

_Vous pourrez aussi directement charger des projets directement depuis:_
> Projet > Ouvrir depuis... > PostgreSQL

_Puis en choisissant la connexion "Service projets" et le sch�ma concern�._


____
## FAQ
> Je ne vois pas les projets, mais seulement les tables de la base de donn�es

 Faire un clic droit sur Postgis/Service Projets dans l'explorateur, cliquer "Editer la connexion" et cocher "Permettre le chargement et l'enregistrement de projets QGIS" puis "OK".
 [Illustration](#Autoriser-le-chargement-des-projets)
____

## Illustrations

<!--

### Acc�s au dossier AppData

<img src="./img/appdata.png" alt= �� width="50%" height="50%">

_Apr�s avoir appuy� sur la touche WINDOWS+R , la fen�tre "Ex�cuter" apparait_
-->
### Gestionnaire de sources de donnees
<img src="./img/gestionnaire_sources.png" alt= �� width="50%" height="50%"> 



<img src="./img/gestionnaire_sources_pg.png" alt= �� width="50%" height="50%"> 

_Le gestionnaire de donn�es est le moyen � privil�gier pour importer des donn�es au projet courant._

_(Les autres fa�ons d'ajouter des couches peuvent cr�er des probl�mes en appliquant des param�tres d'import par d�faut)_

### Autoriser le chargement des projets

<img src="./img/editerconnexion_chargerprojets.png" alt= �� width="50%" height="50%"> 
