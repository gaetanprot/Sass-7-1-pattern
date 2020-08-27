### Sass-7-1-pattern
Sass 7-1 pattern a télécharger pour ses projets avec sass, contien aussi un fichier de config et postCSS et Autoprefixer.

# Installation Sass

``
$ npm install sass -g
$ sass --version
``

# Installation Autoprefixer et postCSS

``
$ npm install autoprefixer postcss postcss-cli -g 
``

# Installation Bootstrap 

``
$ npm install bootstrap
``

# Installation de Jquery 

``
$ npm install jquery
``

### Dossier de Base

Le base/ contient ce que nous pourrions appeler le code standard du projet. Vous y trouverez peut-être le fichier de réinitialisation, des règles typographiques et probablement une feuille de style définissant des styles standard pour les éléments HTML couramment utilisés (que j'aime appeler __base.scss).

Le layout/dossier contient tout ce qui participe à la mise en page du site ou de l'application. Ce dossier peut contenir des feuilles de style pour les parties principales du site (en-tête, pied de page, navigation, barre latérale…), le système de grille ou encore des styles CSS pour tous les formulaires.

Pour les petits composants, il y a le components/dossier. Tout en layout/est macro (définition du wireframe global), components/est plus axé sur les widgets. Il contient toutes sortes de modules spécifiques comme un curseur, un chargeur, un widget, et en gros tout ce qui va dans ce sens. Il y a généralement beaucoup de fichiers components/car l'ensemble du site / de l'application doit être principalement composé de minuscules modules.

Si vous avez des styles spécifiques à la page, il est préférable de les mettre dans un pages/dossier, dans un fichier nommé d'après la page. Par exemple, il n'est pas rare d'avoir des styles très spécifiques pour la page d'accueil d'où la nécessité d'un _home.scssfichier au format pages/.

Sur les grands sites et applications, il n'est pas rare d'avoir des thèmes différents. Il existe certainement différentes manières de traiter les thèmes, mais j'aime personnellement les avoir tous dans un themes/dossier.

Le abstracts/dossier regroupe tous les outils et assistants Sass utilisés dans le projet. Chaque variable globale, fonction, mixin et espace réservé doit être placé ici.
La règle de base pour ce dossier est qu'il ne doit pas afficher une seule ligne de CSS lorsqu'il est compilé seul. Ce ne sont que des assistants Sass.

Lorsque vous travaillez sur un très gros projet avec de nombreux utilitaires abstraits, il peut être intéressant de les regrouper par sujet plutôt que par type, par exemple typographie (__typography.scss), thématisation (__theming.scss), etc. Chaque fichier contient tous les helpers associés: variables, fonctions , mixins et espaces réservés. Cela peut faciliter la navigation et la maintenance du code, en particulier lorsque les fichiers deviennent très longs.

Enfin, la plupart des projets auront un vendors/dossier contenant tous les fichiers CSS des bibliothèques et des frameworks externes - Normalize, Bootstrap, jQueryUI, FancyCarouselSliderjQueryPowered, etc. Les mettre de côté dans le même dossier est une bonne façon de dire «Hé, ce n'est pas de moi, pas de mon code, pas de ma responsabilité».

Le fichier principal (généralement étiqueté main.scss) doit être le seul fichier Sass de toute la base de code à ne pas commencer par un trait de soulignement. Ce fichier ne doit contenir que des @importcommentaires.
Les fichiers doivent être importés en fonction du dossier dans lequel ils résident, l'un après l'autre dans l'ordre suivant: