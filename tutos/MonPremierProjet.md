# Mon Premier projet

_Vous avez re�u des la confirmation du SI que vous �tes autoris� � utiliser la [base de donn�es](./README.md#base-de-donnees) du parc ? Voil� comment faire !_


_Ce tutoriel contient les �tapes pour la consultation d'un [projet Qgis](./README.md#projet "projet Qgis contient un ensemble de couches,
les informations permettant de les repr�senter, ainsi que l'ensemble des param�tres conditionnant la r�alisation de g�otraitements.") existant, ainsi que les possibles op�rations � r�aliser pour en faciliter la visualisation._

> Sc�nario: On vous a demand� d'�tablir pour certaines zones la pr�sence ou l'absence d'une esp�ce v�g�tale donn�e. 
> 
> Pour cela, vous devez consulter un [projet Qgis](./README.md#projet "projet Qgis contient un ensemble de couches,
les informations permettant de les repr�senter, ainsi que l'ensemble des param�tres conditionnant la r�alisation de g�otraitements."), faire vos relev�s terrains, puis entrer les r�sultats en modifiant une couche existante.


## Acc�s � la [base de donn�es](./README.md#base-de-donnees)
_Cette partie reprend le processus d�crit dans [ce tutoriel](./Acces_BD.md)._
### 1. V�rifier que vous avez bien acc�s � la base de donn�es par Qgis. 

Pour cela vous pouvez t�l�charger le projet � [ce lien](./ressources/PremierProjet.qgz) et tenter de le lancer. Si les [couches](./README.md#couche "Dans un projet Qgis, une couche est une repr�sentation de donn�es spatialis�e") s'affichent bien, vous pouvez continuer,
sinon contacter le SI. 


### 2. Charger l'ensemble des connexions

Vous devez avoir re�u un fichier zip permettant le param�trage de la connexion de la part du service informatique.

Enregistrer, et d�compresser si n�cessaire, le fichier "service projets.xml".

D�placer ce fichier dans un dossier o� il sera facile � retrouver.
 
> Exemple: C:\Users\VotreNom\Documents\QgisXML


Une fois Qgis lanc�, vous pouvez ouvrir le gestionnaire de sources de donn�es (Onglet "Couche>Gestionnaire de source de donn�es" ou Ctrl+L).

<img src="./img/gestionnaire_sources.png" alt= �� width="50%" height="50%"> 


- Cliquer sur PostgreSQL dans la barre de gauche

<img src="./img/gestionnaire_sources_pg.png" alt= �� width="50%" height="50%"> 

- Cliquer sur "charger" et retrouver le fichier "service projets.xml" que vous venez de copier


- V�rifier que la connexion "Service projets" est disponible, et se connecter

_La liste des [tables et sch�mas](./README.md#schema) accessibles devraient appara�tre._



_NB: Le gestionnaire de donn�es est le moyen � privil�gier pour importer des donn�es au projet courant. (Les autres fa�ons d'ajouter des couches peuvent cr�er des probl�mes en appliquant des param�tres d'import par d�faut)_

_Cette �tape visait � v�rifier la connexion � la base de donn�es. Maintenant nous allons charger un [projet](./README.md#projet), qui regroupe des donn�es et leur repr�sentation._

### 3. Charger le projet d'int�r�t

Pour cela, cliquer sur l'onglet "Projet" en haut � gauche de la fen�tre Qgis: Projet>Ouvrir Depuis>PostgreSQL

<img src="./img/charger_projet.png" alt= �� width="50%" height="50%"> 

Vous aurez ensuite acc�s � la liste des serveurs disponibles. 
Pour ce tutoriel, il s'agit du projet "Mon premier projet" dans le sch�ma "tutos".


## Visualisation des donn�es du projet
_Vous avez bien r�ussi � charger le projet "MonPremierProjet" et en voyez le contenu. Nous allons maintenant passer en revue 
les moyens de naviguer dans le projet et observer les donn�es._

0. Enregistrer le projet en local 

Vous pouvez � tout moment "enregistrer sous" un projet qui est enregistr� sur le serveur. 
Cela en cr�e une copie qui ne sera plus accessible � personne d'autre que vous, 
mais vous pourrez ensuite le modifier sans risque de perdre le travail de vos coll�gues.


1. Afficher/masquer des couches

_Dans Qgis, la position de la plupart des �l�ments est personnalisable, et il arrive qu'on les modifie par accident. 
Si �a arrive, cas on pourra les retrouver dans l'onglet "Vue", et v�rifier que le panneau ou la barre d'outils concern�e est bien visible._


<img src="./img/vue_panneaux_barres.png" alt= �� width="30%" height="30%"> 

A gauche de chaque couche se trouve une petite boite qui peut �tre coch�e ou d�coch�e. 
Cette boite permet d'afficher ou de masquer chaque couche, ou �l�ment de symbologie d'une couche.




2. Les propri�t�s

Double cliquer sur une couche, ou faire "clic droit > Propri�t�s" en affiche les propri�t�s. 

_**Le d�tail de la table attributaire n'est pas visible dans les propri�t�s.**_

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

Par exemple, en cliquant sur le symbole filtre de "area" ou en faisant clic droit > Filtre sur cette couche vous voyez l'expression suivante :
```sql
"name"='coeur' OR "id_type"=4
```

qui signifie: 
"Ne charge que les entit�s pour lesquelles la colonne "name" contient la cha�ne de caract�res 'coeur' 
ou bien celles pour lesquelles la colonne 'id_type' contient la valeur 4.
"



_Certaines couches du serveur sont charg�es par d�faut avec des filtres. Il est tout � fait possible de les modifier pour acc�der � d'autres donn�es, 
ou de restreindre encore le filtre propos� le temps de la consultation du projet. Dans ce cas, veillez cependant � ne pas enregistrer vos modifications sur un projet partag�._

_Les projets devraient �tre con�us de fa�on � ce que vous n'ayez pas � manipuler les filtres. N�anmoins, vous �tes encourag�s � apprendre � les utiliser.
Les filtres emploient une syntaxe SQL et un [tutoriel](lienavenir) d�di� sera cr��._

<!--
_Les filtres sont aussi visibles en dans les propri�t�s d'une couche, � l'onglet "Source". Ce n'est pas tr�s intuitif...._  
--> 

4. La table attributaire

Les couches au format [vecteur](./README.md#vecteur "En g�omatique, un vecteur est l'un des deux modes principaux de repr�sentation des donn�es spatiales. 
") contiennent une [table attributaire](), donnant des informations sur les donn�es qu'elles contiennent. 
Vous pouvez visualiser cette table en cliquant droit sur la couche puis sur "Ouvrir la table d'attributs".

<img src="./img/ouvrir_latable_attribut.png" alt= �� width="15%" height="50%"> 


Il existe deux fa�ons de repr�senter la table attributaire. Une vue "Table" et une vue "Formulaire". On peut basculer de l'une � 
l'autre en cliquant sur l'icone correspondante en bas � droite de la fen�tre. 



<img src="./img/tableattributaire.png" alt= �� width="15%" height="50%">  <img src="./img/tableattributaire_form.png" alt= �� width="15%" height="50%"> 

_A gauche, la table atributaire en format table. A droite,en format formulaire. Le mode table permet de visualiser d'un coup d'oeil l'ensemble des entit�s et attributs simultan�ment.
Le mode formulaire permet de visualiser et les entit�s une � une, la liste des entit�s apparaissant sur la gauche._






## Editer d'une couche

_On se concentrera sur les couches au format [vecteur](bonjourcestunlien.xml). Toutes les couches pr�sentes dans le projet tuto sont dans ce format. 
Il existe des m�thodes pour modifier les [rasters](autrelien), mais nous ne les aborderons pas ici._

Editer une couche Qgis modifie le fichier de source des donn�es. Il est donc important rester prudent et garder une copie des donn�es d'origine quand c'est possible. 
Pour r�aliser des modifications ou cr�er une nouvelle entit�, il faut d'abord activer le mode Edition pour la couche d'int�r�t. Cela peut se faire de plusieurs fa�ons: 

|<img src="./img/mode_edition.png" alt= ��  height="75%"> |  <img src="./img/modeedition_parcouche.png" alt= �� width="75%" > |  <img src="./img/mode_tableattributaire.png" alt= ��  width="75%"> |
|:--:|:--:|:--:|:--:|
|Dans la barre d'outils Qgis |En passant par un clic droit sur la couche|depuis la fen�tre de la table attributaire|

Dans tous les cas, cliquer sur le petit crayon activera le mode �dition pour la couche s�lectionn�e. On pourra alors y apporter des modifications de diff�rentes fa�on.
Ces modifications ne seront toutefois enregistr�es et effectives qu'� la sortie du mode �dition (en cliquant � nouveau sur le crayon). Si le logiciel crash, ou qu'on ne confirme 
pas les changements � la sortie du mode �dition, les changements seront perdus et les donn�es d'origine seront conserv�es. 

1. Modification de la table attributaire

Une fois en mode Edition, on peut modifier directement la table attributaire � la fa�on d'un tableur. 


2. Cr�ation d'entit�s/Modification de g�om�trie

En mode �dition, on peut aussi �diter directement la g�om�trie d'une entit�, ou en cr�er de nouvelles. 

|<img src="./img/outil_sommet.png" alt= ��  width="75%"> |<img src="./img/ajouter_entite.png" alt= ��  height="50%"> |
|:--:|:--:|
|l'outil sommet permet de modifier la g�om�trie de points/lignes/polygones existants| Ajouter une entit� permet de cr�er de nouvelles entit�s|


La cr�ation d'une nouvelle entit� se fait par une succession de clics gauches, et est finalis�e par un clic droit.
A la finalisation de chaque entit�, une fen�tre s'ouvre proposant d'entrer les attributs connus. 

<img src="./img/nouvelle_entite.png" alt= ��  width="40%"> 

Un "id" ou "fid" correspondant � l'identifiant unique de chaque entit� peut �tre g�n�r� automatiquement. 
Il n'est pas n�cessaire d'entrer les autres attributs pour que la nouvelle enttit� soit sauvegard�e. 


<!--
### Autoriser le chargement des projets

<img src="./img/editerconnexion_chargerprojets.png" alt= �� width="50%" height="50%">  -->

## Changer le mode de repr�sentation d'une couche

Dans couche on appelle le mode de repr�sentation des donn�es d'une couche la "symbologie" (exemple: des aplats de couleurs, cercles noirs pour des points, lignes vertes etc...)
Elle peut �tre modifi�e de fa�on pr�cise pour chaque couche en passant par les propri�t�s d'une couche, � l'onglet symbologie.

Les outils de symbologie dans Qgis sont tr�s puissants, et permettent de repr�senter les informations d'une couche de fa�on synth�tique.
On d�crit ici les modes de repr�sentation les plus commun�ment utilis�s:
- Symbole unique

Mode de repr�sentation le plus simple. On d�finit un symbole qui sera appliqu� de mani�re uniforme � toutes les entit�s, sans prendre en compte leurs attributs

- Cat�goris�

Permet de repr�senter des diff�rences qualitatives entre les entit�s. C'est-�-dire qu'un de leurs attributs permet de les diff�rencier.
> Par exemple: pour des polygones repr�sentant l'occupation des sols, le nom de ces cat�gories (for�t, culture, b�ti etc...).

- Gradu�

Permet de repr�senter des diff�rences quantitatives entre des entit�s.
> Par exemple: pour des points repr�sentant des villes, on peut faire varier leur taille pour repr�senter leur population. 


_Dans ce tutoriel nous n'irons pas plus loin sur la symbologie, mais un autre tutoriel lui sera d�di�e. Nous vous invitons � faire des essais, tout en prenant soin 
de ne pas �craser la symbologie d'un projet partag�._


## Exporter une carte au format image

_Attention, de nombreux projets du Parc contiennent des donn�es qu'il n'est pas possible de diffuser librement. 
Il est donc fortement sugg�rer de n'employer les exports que pour des utilisations internes._

1. Export simple

Il est possible de r�aliser des exports directement depuis le menu de Qgis. A l'onglet Projet > Importer/exporter > Exporter au format Image
Cette fa�on de faire ne permet que d'exporter le contenu du canevas

<img src="./img/export_format_image.png" alt= ��  width="40%"> 

Cet outil fait apparaitre un menu permettant de choisir l'emprise de l'export: 

<img src="./img/menu_export.png" alt= ��  width="40%"> 

On peut ainsi facilement exporter au format image la vue de la carte visible � l'�cran. 


2. Mises en page

Qgis permet de r�aliser des mises en pages de cartes plus complexes. Pour les r�aliser, il faut passer par l'outil de mise en page de Qgis.

<img src="./img/mise_en_page.png" alt= ��  width="40%"> 

Si une mise en page a d�j� �t� cr��e pour le projet en question, vous la trouverez ou bien dans le menu "Projet > Mise en page" ou bien
dans le Gestionnaire de mises en page.

Il est aussi possible de cr�er une nouvelle mise en page. 

Dans tous les cas, � l'ouverture d'une mise en page, une nouvelle fen�tre s'ouvre. 

