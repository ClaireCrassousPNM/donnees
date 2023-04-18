# Acc�s au catalogue de donn�es WMS/WFS.

<!--Ce tutorial d�taille les �tapes permettant de configurer l'acc�s au catalogue de donn�es WMS/WFS du Parc national du Mercantour.
Il exige d'avoir re�u au pr�alable un fichier zip du service informatique du Parc. --> 

## Avant de commencer

 - _Vous avez re�u un fichier zip ou .xml permettant le param�trage de la connexion de la part du service informatique_
 - _Vous �tes bien sur une session windows qui n'est pas partag�e._

## Etapes du param�trage


- Enregistrer et d�compresser si n�cessaire le fichier zip contenant le fichier "service WMS.xml".

- D�placer ce fichier dans un dossier o� il sera facile � retrouver.
 
> Exemple: C:\Users\VotreNom\Documents\QgisXML

- Lancer Qgis
 
- Ouvrir le gestionnaire de sources de donn�es (Onglet "Couche>Gestionnaire de source de donn�es" ou CTRL+L). _[Illustration](#Gestionnaire-de-sources-de-donnees)_

- clic droit sur WMS/WMTS dans l'explorateur, s�lectionner "charger des connexions" 

 - S�lectionner le fichier "service WMS.xml" pr�c�demment enregistr�. 
Une fen�tre s'ouvre, clic sur 'Tout S�lectionner' puis 'Importer'

_Cette op�ration a enrichi l'annuaire des couches WMS avec les catalogues IGN les plus souvent utilis�s._



____

## Illustrations

### Gestionnaire de sources de donn�es
<img src="./img/gestionnaire_sources.png" alt= �� width="50%" height="50%"> 
