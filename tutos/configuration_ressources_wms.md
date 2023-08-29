# Acc�s au catalogue de donn�es WMS/WFS.

<!--Ce tutorial d�taille les �tapes permettant de configurer l'acc�s au catalogue de donn�es WMS/WFS du Parc national du Mercantour.
Il exige d'avoir re�u au pr�alable un fichier zip du service informatique du Parc. --> 

## Avant de commencer

 - _Vous �tes bien sur une session windows qui n'est pas partag�e._

## Etapes du param�trage


- T�l�charger le fichier [service WMS.xml en cliquant sur ce lien](https://github.com/PnMercantour/donnees/blob/main/tutos/ressources/service%20WMS.xml), puis sur l'ic�ne permettant le t�l�chargement.
_(Il sera n�cessaire de revenir manuellement sur cette page pour la suite du tuto)_
<img src="./img/wms_telecharger.png" alt= �� width="50%" height="50%"> 

- D�placer ce fichier dans un dossier o� il sera facile � retrouver.
 
> Exemple: C:\Users\"VotreNom"\Documents\QgisXML
_Remplacer "VotreNom" par le nom d'utilisateur sur votre machine._
- Lancer Qgis
 
- Ouvrir le gestionnaire de sources de donn�es (Onglet "Couche>Gestionnaire de source de donn�es" ou CTRL+L). 
<img src="./img/gestionnaire_sources.png" alt= �� width="50%" height="50%"> 

- clic droit sur WMS/WMTS dans l'explorateur, s�lectionner "charger des connexions" 

 - S�lectionner le fichier "service WMS.xml" pr�c�demment enregistr�. 
Une fen�tre s'ouvre, clic sur 'Tout S�lectionner' puis 'Importer'

_Cette op�ration a enrichi l'annuaire des couches WMS avec les catalogues IGN les plus souvent utilis�s._
_Vous pouvez maintenant ajouter des fonds de carte au format wms en suivant la d�marche d�crite [ici](./ajout_fond_de_carte.md)

