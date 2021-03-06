# Eric's MagicaVoxel Shaders
<a href="../README.md">Return</a>

**TRANSLATED BY <a href="http://moiscript.weebly.com/magicavoxel.html">PILOU</a> - AUTHORIZED REPRODUCE**

## Installation
Installez ces shaders en copiant les fichiers du répertoire shader de ce projet dans le répertoire shader de votre installation MagicaVoxel.

## Les shaders
### Catalogue
* <a href="#terrain-generator">Terrain generator</a>
* <a href="#flow">Flow</a>
* <a href="#flow2">Flow2</a>
* <a href="#project">Project</a>
* <a href="#life-game">Life game</a>
* <a href="#cube-filling">Cube filling</a>
* <a href="#flood">Flood</a>
### TERRAIN GENERATOR
<a href="#catalogue">Retour au catalogue</a>
* Nom de fichier: `tergen.txt`
* Utilisation de la ligne de commande: `xs tergen [seed] [altitude] 
[noise-scale] [voxel-color] <void-voxel-color> <vertical-shifting> <x-shifting> <y-shifting>`
* Ligne de commande: `xs tergen 19260817 40 90 1 -1 10 -50 -10`
* Edition minimale: `xs tergen 19260817 40 90 1`
>1. Il est recommandé de régler la taille de la scène sur 126x126x126x126 pour obtenir la meilleure vue.
>2. Réglez la couleur void-voxel sur -1 pour ne pas supprimer la scène originale.
>3. En utilisant le xyz-shifting du shader et le nouveau système global de MagicaVoxel 0.99.x, vous pourrez créer une grande carte du terrain. (fig. 3)
* Aperçu de l'image:

  <img src="../img/tg.png" width="250px"><img src="../img/tg1.png" width="250px"><img src="../img/tg2.png" width="250px">
### FLOW
<a href="#catalogue">Retour au catalogue</a>
> Ce shader imite la mécanique de l'écoulement de l'eau dans la nature.
* Nom de fichier: `flow.txt`
* Utilisation de la ligne de commande: `xs flow [color-index]`
* Ligne de commande: `xs flow 1`
>Les voxels avec un index donné sont source d'eau, le shader ne les créerait pas automatiquement, vous devez les attacher en premier.
* Aperçu de l'image:

  <img src="../img/flowShader.png">
### FLOW2
<a href="#catalogue">Retour au catalogue</a>
>Contrairement au shader classique, ce shader offre une solution pour les zones d'eau fermées.(fig.2)
* Nom de fichier: `flow2.txt`
* Utilisation de la ligne de commande: `xs flow2 [color-index]`
* Ligne de commande: `xs flow2 1`
>Les voxels avec un index donné sont source d'eau, le shader ne les créerait pas automatiquement, vous devez les attacher en premier.
* Aperçu de l'image:

  <img width="250px" src="../img/flow2_1.png">
  <img width="250px" src="../img/flow2_2.png">
### PROJECT
<a href="#catalogue">Retour au catalogue</a>
* Nom de fichier : project.txt
* ​Utilisation de la ligne de commande​ : xs project[altitude du plan xy] 
* Ligne de commande d'exemple : xs project 64 (64 étant l'altitude Z d'un plan XY de voxels couleurs dans la matrice active)
>Toutes les couleurs d'une altitude donnée vont être projettées sur les volumes existants de la matrice active!
* Aperçu de l'image:

  <img width="250px" src="../img/pro.png">
  <img width="250px" src="../img/pro1.png">
  <img width="250px" src="../img/pro2.gif">
### LIFE GAME
<a href="#catalogue">Retour au catalogue</a>
* Nom de fichier: `lifegame.txt`
* Utilisation de la ligne de commande: `xs lifegame [color-index]`
* Ligne de commande: `xs lifegame 1`
> Conçu pour le plan X-Y. Utilisez une seule couleur dans votre scène, ou le shader la détruira.
* Aperçu de l'image:

  <img src="../img/l1.png" width="250px">
  <img src="../img/l2.png" width="250px">
  <img src="../img/l3.png" width="250px">
### CUBE FILLING
<a href="#catalogue">Retour au catalogue</a>
* Nom de fichier: `cubefill.txt`
* Utilisation de la ligne de commandes:
  1. `xs cubefill [mode (0 for filling, 1 for frame)] [point1_X] [point1_Y] [point1_Z] [point2_X] [point2_Y] [point2_Z] [voxel color]`
  2. `xs cubefill [mode (0 for filling, 1 for frame)] [pointX] [pointY] [pointZ] [length of a side] [voxel color]`
* Ligne de commande:
  1. `xs cubefill 1 1 1 1 7 2 2 216` - Dessine le cadre du bord d'un cuboïde rouge entre les coordonnées (1,1,1) et (7,2,2).
  2. `xs cubefill 0 50 50 50 10 216` -  Prendre les coordonnées (50,50,50) comme centre, créer un cube rouge avec une longueur latérale de 10 unités.
* Aperçu de l'image:

  <img src="../img/cf.png" width="250px">


