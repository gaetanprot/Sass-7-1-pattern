# Sass-7-1-pattern
Sass 7-1 pattern a télécharger pour ses projets avec sass, contien aussi un fichier de config et postCSS et Autoprefixer.

# Cloner le Pattern 7-1

```sh
$ git clone https://github.com/gaetanprot/Sass-7-1-pattern.git
$ cd Sass-7-1-pattern
$ npm install
```

# Installation Sass

```sh
$ npm install sass -g
$ sass --version
```

# Installation Autoprefixer et postCSS

```sh
$ npm install autoprefixer postcss postcss-cli -g 
```

# Installation Bootstrap 

```sh
$ npm install bootstrap
```

# Installation de Jquery 

```sh
$ npm install jquery
```

# Dossier de Base

Le base/ contient ce que nous pourrions appeler le code standard du projet. Vous y trouverez peut-être le fichier de réinitialisation, des règles typographiques et probablement une feuille de style définissant des styles standard pour les éléments HTML couramment utilisés (que j'aime appeler __base.scss).

---

Le layout/ contient tout ce qui participe à la mise en page du site ou de l'application. Ce dossier peut contenir des feuilles de style pour les parties principales du site (en-tête, pied de page, navigation, barre latérale…), le système de grille ou encore des styles CSS pour tous les formulaires.

---

Pour les petits composants, il y a le components/. Il plus axé sur les widgets. Il contient toutes sortes de modules spécifiques comme un curseur, un chargeur, un widget, et en gros tout ce qui va dans ce sens. Il y a généralement beaucoup de fichiers components/ car l'ensemble du site / de l'application doit être principalement composé de minuscules modules.

---

Si vous avez des styles spécifiques à la page, il est préférable de les mettre dans un pages/, dans un fichier nommé d'après la page. Par exemple, il n'est pas rare d'avoir des styles très spécifiques pour la page d'accueil d'où la nécessité d'un _home.scssfichier au format pages/.

---

Sur les grands sites et applications, il n'est pas rare d'avoir des thèmes différents. Il existe certainement différentes manières de traiter les thèmes, mais j'aime personnellement les avoir tous dans un themes/.

---

Le abstracts/ regroupe tous les outils et assistants Sass utilisés dans le projet. Chaque variable globale, fonction, mixin et placeholder doit être placé ici.
La règle de base pour ce dossier est qu'il ne doit pas afficher une seule ligne de CSS lorsqu'il est compilé seul. Ce ne sont que des assistants Sass.

---

Enfin, la plupart des projets auront un vendors/ contenant tous les fichiers CSS des bibliothèques et des frameworks externes - Normalize, Bootstrap, jQueryUI, FancyCarouselSliderjQueryPowered, etc. Les mettre de côté dans le même dossier est une bonne façon de dire «Hé, ce n'est pas de moi, pas de mon code, pas de ma responsabilité».

---

Le fichier principal (généralement étiqueté main.scss) doit être le seul fichier Sass de toute la base de code à ne pas commencer par un trait de soulignement. Ce fichier ne doit contenir que des @importcommentaires.
Les fichiers doivent être importés en fonction du dossier dans lequel ils résident, l'un après l'autre dans l'ordre suivant: