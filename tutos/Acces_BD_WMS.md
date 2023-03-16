# Acc�s au catalogue de donn�es WMS/WFS et � la base de donn�es.


_Avant de commencer: se trouver sur une session windows qui n'est pas partag�e._



- Enregistrer et d�compresser le fichier zip contenant les deux fichiers "service projets.xml" et "service WMS.xml".


- naviguer jusqu'au dossier AppData.

Il se trouve typiquement dans un chemin du type:
> C:\Users\ *[nomdelasession]* \AppData\Roaming

Le fa�on la plus simple de l'atteindre consiste � appuyer sur  _touche windows + R_, 
puis � entrer la commande "%AppData%" dans l'invit� de commande (la touche windows se trouve entre ctrl et alt). [Voir Exemple](#Acces-au-dossier-AppData)

(Ce r�pertoire est masqu� par d�faut, il est aussi possible de naviguer jusqu'� lui, en autorisant
l'affichage des fichiers cach�s dans les options)


- Cr�er un dossier "postgresql" dans le dossier AppData\Roaming s'il n'existe pas
- Copier dans ce dossier tous les fichiers du zip, y compris le fichier masqu� .pg_service.conf
(les remplacer s'ils existent d�j�)

- lancer Qgis

- clic droit sur WMS/WMTS dans l'explorateur, s�lectionner "charger des connexions" 

 - S�lectionner le fichier "service WMS.xml" pr�c�demment enregistr� sur le disque. 
Une fen�tre s'ouvre, clic sur 'S�lectionner tout'. 
Cette op�ration a enrichi l'annuaire des couches WMS avec les catalogues IGN les plus souvent utilis�s.

- clic droit sur Postgis dans l'explorateur. M�me manip que pr�c�demment avec le fichier "service projets.xml" qui ajoute la connexion vers notre base de donn�es au catalogue.




## Illustrations

### Acces au dossier AppData

<img src="./img/appdata.png" alt= �� width="50%" height="50%">
