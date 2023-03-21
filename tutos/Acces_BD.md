# Acc�s au catalogue de donn�es WMS/WFS et � la base de donn�es.


_Avant de commencer: se trouver sur une session windows qui n'est pas partag�e._



- Enregistrer et d�compresser le fichier zip contenant les deux fichiers "service projets.xml"


- naviguer jusqu'au dossier AppData.

Il se trouve typiquement dans un chemin ressemblant �:
```
C:\Users\ *[nomdelasession]* \AppData\Roaming
```
Le fa�on la plus simple de l'atteindre consiste � appuyer sur  _touche windows + R_, 
puis � entrer la commande "%AppData%" dans l'invit� de commande (la touche windows se trouve entre ctrl et alt). [Exemple](#Acces-au-dossier-AppData)

(Ce r�pertoire est masqu� par d�faut, il est aussi possible de naviguer jusqu'� lui, en autorisant
l'affichage des fichiers cach�s dans les options)


- Cr�er un dossier "postgresql" dans le dossier AppData\Roaming s'il n'existe pas
- Copier dans ce dossier tous les fichiers du zip, y compris le fichier masqu� .pg_service.conf
(les remplacer s'ils existent d�j�)

- lancer Qgis

- clic droit sur Postgis dans l'explorateur. M�me manipulation que pr�c�demment avec le fichier "service projets.xml" qui ajoute la connexion vers notre base de donn�es.




## Illustrations

### Acc�s au dossier AppData

<img src="./img/appdata.png" alt= �� width="50%" height="50%">
