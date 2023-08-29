# Ajouter une couche WMS

## Avant de commencer

- _Vous souhaitez ajouter un fond de carte � votre projet Qgis_
- _Vous avez d�j� ajout� le catalogue de ressources wms � l'aide de [ce tuto](./configuration_ressources_wms.md) ou avez le lien vers une autre ressource wms vous int�ressant._

## Etapes du param�trage


- Lancer Qgis
 
- Ouvrir le gestionnaire de sources de donn�es (Onglet "Couche>Gestionnaire de source de donn�es" ou CTRL+L). 

- Cliquer sur l'onglet "WMS" dans la colonne � gauche de la fen�tre.

<img src="./img/gestionnaire_sources.png" alt= �� width="50%" height="50%"> 


## Si vous souhaitez ajouter une ressource se trouvant d�j� dans le catalogue

- Dans le menu d�roulant des couches, choisir la source de donn�es qui vous int�resse (ici : "IGN - Licence 7569 - Usages gratuits")
- Cliquer sur connexion
- Les couches li�es � la couche choisie vont appara�tre. Choisir celle qui vous int�resse (ici la carte topographique "SCAN25"):
- Prendre soin de bien remplir les champs "taille de la tuile" avec, par exemple 256 comme valeur, ou moins.

_Entrer une valeur dans ce champ �vite que Qgis n'essaie de charger des tuiles trop grosses depuis le WMS, ce qui peut ralentir voire compl�tement bloquer l'affichage de votre projet._

<img src="./img/ajout_wms_parametres.png" alt= �� width="90%" height="90%"> 

- Appuyer sur ajouter.
 

## Vous souhaitez ajouter une ressource depuis un nouveau lien

- Cliquer sur "Nouveau"

- Entrer un nom clair permettant de comprendre de quelle ressource il s'agit ( "IGN - base de donn�es Hydro" par exemple)

- Coller le lien de la ressource dans le champs "URL"

- Cliquer sur "OK"
