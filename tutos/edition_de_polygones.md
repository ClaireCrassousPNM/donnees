# Edition de polygones.

<!--Ce tutorial d�taille les �tapes permettant de configurer l'acc�s au catalogue de donn�es WMS/WFS du Parc national du Mercantour.
Il exige d'avoir re�u au pr�alable un fichier zip du service informatique du Parc. --> 

## Avant de commencer

 - _Vous d�sirez modifier la forme ou les attributs d'un fichier au format vecteur (.gpkg/.shp)_

 -_Vous avez les autorisations pour modifier ce fichier dans la base de donn�es/ Ou bien Ce fichier se trouve bien en local ([Comment v�rifier?]())_
 
 
## Edition de Polygones


- Activer le mode �dition (2 fa�ons possibles).
	- En s�lectionnant la couche � modifier, puis en cliquant sur l'ic�ne de crayon dans la barre d'outils en haut de l'�cran  
<img src="./img/mode_edition.png" alt= �� width="50%" height="50%"> 
	- Ou bien, en faisant un clic droit sur la couche � modifier, puis en cliquant sur  l'ic�ne crayon "Basculer en mode �dition"
<img src="./img/modeedition_parcouche.png" alt= �� width="50%" height="50%"> 

- Une fois dans ce mode, un crayon apparait au dessus du symbole de la couche
<img src="./img/couche_en_cours_edition.png" alt= �� width="50%" height="50%"> 


- .. et de de nombreux outils deviennent accessibles dans la barre d'outil. Ces outils sont regroup�s dans les barres d'outils "Num�risation" et "Num�risation avanc�e", 
visibles en faisant un clic droit sur une des barres d'outils en haut de l'�cran, ou bien dans la barre de menu "Vue > Barres d'outils > ..."

<img src="./img/barre_doutils_numerisation.png" alt= �� width="50%" height="50%"> 

_A partir de l�, un grand nombre d'op�rations sont disponibles, nous ne d�crirons que les plus simples._

### Cr�er une nouvelle entit�

- Proche de l'icone de crayon, dans la barre d'outils, se trouve l'ic�ne "Ajouter une entit�"

<img src="./img/edition_ajouter_une_entite.png" alt= �� width="50%" height="50%"> 

- Apr�s avoir cliqu� dessus, votre curseur change, et vous pouvez directement ajouter des points qui formeront, suivant le type de g�om�trie que votre couche contient
	- une entit� 
	- une partie de ligne ou de polygone
- Un clic gauche vous permet d'ajouter un point, un clic droit termine la saisie d'une entit� sans en rajouter de nouveau (_donc pour faire un rectangle, il faut 4 clics gauches + 1 clic droit_)
- A chaque fin de saisie, une boite de dialogue s'ouvre, permettant d'entrer manuellement les attributs de l'entit�. Dans la plupart des cas, vous n'�tes pas oblig� d'entrer
quoi que ce soit, et pouvez simplement cliquer sur OK pour continuer la saisie. Pour certaines couches il sera n�cessaire d'entrer manuellement un id avant de pouvoir continuer � saisir des entit�s.

<img src="./img/nouvelle_entite.png" alt= �� width="50%" height="50%"> 



### Modifier la g�om�trie d'une entit� existante

- L'outil sommet, disponible dans la barre d'outil num�risation � droite de l'outil d'ajout d'entit� permet d'ajouter, supprimer, ou cr�er de nouveaux sommets.
<img src="./img/outil_sommet.png" alt= �� width="50%" height="50%"> 
- Une fois l'outil sommet s�lectionn�, on peut s�lectionner n'importe quel sommet en cliquant dessus. Les sommets de chaque polygone sont visibles sous la forme de petits cercles rouges

<img src="./img/edition_modif_de_sommets.png" alt= �� width="50%" height="50%"> 

- Apr�s avoir s�lectionn� un sommet avec l'outil sommet, il est possible de le supprimer en appuyant sur la touche "Suppr" du clavier. 
- On peut aussi le d�placer, en cliquant � nouveau avec le clic gauche � un autre endroit apr�s avoir s�lectionn� un sommet. 

- Enfin, il est possible de cr�er de nouveaux sommets dans un polygone en cliquant tr�s pr�cis�ment sur la croix qui apparait en faisant passer le curseur entre deux sommets. 
<img src="./img/edition_nouveau_sommet.png" alt= �� width="50%" height="50%"> 

En combinant le d�placement, la modification, et la cr�ation de sommets, il est possible de changer compl�tement la forme d'un polygone.

_Tant que les modifications n'ont pas �t� enregistr�es, elles ne sont pas d�finitives; _


### Modifier les attributs d'une entit�

- Une fois activ� l'outil �dition, il est possible de simplement �diter � la main les cases de la table attributaire. On peut activer le mode �dition depuis la barre d'outils de la table attributaire.
<img src="./img/mode_tableattributaire.png" alt= �� width="50%" height="50%"> 


