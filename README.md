# Projet site web d'un restaurant: Japan House
> https://cindy-buchet.github.io/restaurant-css-framework/

Ce projet a été réalisé pendant ma formation BeCode à Charleroi du 15 au 20 mai 2019. C'est le dernier projet de la prairie. La prairie est le premier mois effectué à la formation, où nous prenons en main le HTML/CSS (l'intégration).

**SOMMAIRE**

* [Mission](#Mission)
* [Les demandes](#Les-demandes)
* [Choix de design](#Choix-de-design)
    * [Typographies](#Typographies)
        * [Tailles de typographies](#Tailles-de-typographies)
    * [Couleurs](#Couleurs)
    * [Mise en place des éléments](#Mise-en-place-des-éléments)
* [Le code](#Le-code)
* [Difficultées rencontrées](#Difficultées-rencontrées)
* [Mon avis sur ce projet](#Mon-avis-sur-ce-projet)


## Mission

La mission était de réaliser la vitrine d'un restaurant. Nous devions inventer tout de A à Z. Penser au design: les mises en places des éléments, les choix de couleurs, de typographies, ... Et enfin, le coder !

## Les demandes

Nous ne pouvions pas tout choisir de nous-même, nous avons eu des consignes à respecter ! 
1. Le site devait être responsive (adapté pour tout les écrans)
2. Faire 5 pages accessibles via le menu (navbar) : Accueil, Carte, Photos, Restaurants et Contact.
3. Sur chaque page, nous avions des consignes:
    1* **Accueil** : 
        * Un composant Jumbotron
        * Deux panneaux / panels de news
    * **Carte** :
        * Menu sous forme de liste groupée avec badges
    * **Photos** : 
        * Une galerie photos avec au minimum 10 photos et une pagination (3 photos par page)
    * **Restaurants** :
        * L'adresse, un plan d'accès et les heures d'ouverture d'au moins deux restaurants
    * **Contact** :
        * Un formulaire de contact avec: nom, prénom, e-mail, liste déroulante, champ de texte et un bouton d'envoi avec du Glyphicon

## Choix de design

Avant de commencer à coder, j'ai préféré faire des ébauches sur papier pour avoir une idée de ce que j'allais mettre en place sur le site. Où tel et tel élément allaient être placés.

Voici un [exemple](https://image.noelshack.com/fichiers/2019/21/1/1558359307-60708161-2445777315485120-229780776105803776-n.jpg) de mon croquis de mon accueil. J'avais déjà réfléchi où j'allais mettre le "jumbotron" et les "panels" pour les news. 

Je préfère avoir une idée d'où je vais mettre mes éléments avant de coder car autrement je suis vite perdue. C'est le même pour les typographies et couleurs, j'aime savoir en avance ce que je vais prendre.

### Typographies
J'ai choisi en tout trois typographies:
```
h1{
    font-family: 'Kristi', cursive ;
}
h2, h3{
    font-family: 'Libre Franklin', sans-serif;
}
body{
    font-family: 'Nunito Sans', sans-serif;
}
```
Habituellement, je travaille seulement avec deux typographies sans-serif car c'est plus simple à la lecture selon moi. Mais ici, j'ai décidé de mettre une typographie cursive sur mon titre principal. C'est beaucoup vu dans des sites de restaurant.

#### Tailles de typographies
```
body {
  font-size: 100%;
  line-height: 1.6;
  font-size: 1em;
}

h1 {
  font-size: 2.5em;
}

h2 {
  font-size: 2em;
}

h3 {
  font-size: 1.5em;
}
```
Par défaut, j'ai laissé la taille des typographies à 100% et 1em, ce qui équivaut à 16px.

J'ai augmenté la taille de mes typographies x1.5. Donc mon plus petit titre (h3) est de 1.5 em, ensuite le deuxième titre (h2) est à 2em et enfin le titre principal (h1) est à 2.5em. 

Ca laisse une cohérence entre chaque titre, pour ne pas passer d'une taille de 16px à 18px à 26px, qui est incohérent. 

J'ai aussi mit un espacement de 1.6 entre chaque ligne de phrases (la line-height).
### Couleurs
```
$redlight: #FA5032;
$reddark: #E32322;
$orange: #E35B22;
$black: #131313;
$white:#ffffff;
```
J'ai configuré 5 couleurs en tout. C'est les seuls couleurs que j'utilise dans mon site.

Le 'redlight' est surtout utilisé pour les petits éléments comme border, les boutons, ...

Le 'reddark' est utilisé pour les titres.

Le 'orange' est utilisé pour les onglets dans le menu.

Et enfin le dark est utilisé pour la couleur des textes, c'est une couleur noir mais un tout petit peu plus clair et le white est utilisé comme couleur de fond du site.

### Mise en place des éléments
J'ai gardé le même système de colonnes sur toutes mes pages: soit une div qui prend toute la longueur, soit la page est divisé en deux ou trois colonnes égales entre elles. Ca évite de partir sur des colonnes différentes (par exemple une section avec une colonne qui fait 1/4 et l'autre 3/4 et partir après sur une section de 2/5 et 2/5 et 1/5). Je préfère quand mon site est bien structuré.

## Le code
J'ai travaillé avec SASS (Oh SASS, mon grand ami!). J'ai configuré mon SASS pour pouvoir créer plusieurs fichiers SCSS et ainsi travailler plus proprement en me retrouvant plus facilement car quand on a plusieurs pages, on se trouve facilement avec pleins de ligne css et vive le bordel après... J'ai configuré SASS pour qu'il me génère tout mon code sur un seul fichier css. Quel magie ce SASS.

Et comme demandé dans l'exercice, j'ai travaillé avec Bootstrap. Je trouve Bootstrap très pratique surtout pour ce qui concerne le responsive grâce au système de colonnes qui adapte tout seul le responsive. Ca évite de passer par des media queries où on se prend très facilement la tête. En plus, Bootstrap a déjà des trucs qui se font tout seul comme la navbar adapté en responsive, les panels, ...

## Difficultées rencontrées
Etant donné que j'avais déjà fait ma VCard avec Bootstrap, je savais déjà un peu comment ça fonctionnait. Mais grâce à ce projet, j'ai pu découvrir que Bootstrap proposait autre chose que le système de colonnes. 

Adoptez Bootstrap, ça changera votre vie!

Une des difficultés que j'ai rencontré, c'est qu'une fois que je bougeais le css d'une div dans une page, quand j'allais dans une autre je voyais des bugs qu'il n'y avait pas avant. Alors, pour régler ce soucis, j'ai mit une class qui englobe toute la partie que je voulais modifier et grâce au SASS, j'ai pu travailler plus proprement. Maintenant, je sais comment éviter ces problèmes à l'avenir!

J'ai aussi galéré à faire les paginations sans devoir passer par du JavaScript, mais après plusieurs heures de recherches (comment perdre du temps) j'ai enfin trouvé une solution: la nav.

## Mon avis sur ce projet

Comme dit ci-dessus, j'adore Bootstrap! Faire ce projet, ça m'a vraiment plu car j'ai pu découvrir de nouvelles fonctionnalitées que je ne connaisssais pas. 

En plus, à pars les 2/3 contraintes, on était vraiment libre de faire ce qu'on voulait dans le site, alors on apprécie plus facilement ce qu'on fait vu qu'on peut prendre ce qu'on aime (A pars que ça donnait faim de voir des sushis et ramens partout).


![Soulagée](https://i.giphy.com/media/JMV7IKoqzxlrW/giphy.webp)