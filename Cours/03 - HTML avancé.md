









Différentes versions d’HTML
================================

D’HTML 4.01 à HTML 5 en passant par XHTML
-----------------------------------------

HTML a évolué avec le web, sa dernière version est la version 5. Il a changé de version mais aussi parfois de nom, pour devenir l’XHTML, *eXtensible HyperText Markup Language* pour redevenir HTML.

HTML est utilisable dans ses différentes versions, il est juste nécessaire d’indiquer au logiciel chargé de l’afficher la version utilisée dans son document.

La version HTML 4.01 a été longtemps utilisée car les standards n’ont pas évolués rapidement sur ce sujet pendant plusieurs années et il reste encore utilisé (regarder le code source de Google…).

xHTML *eXtensible HyperText Markup Language*, est ce qui a suivi, c’est un HTML à la sauce XML (au autre langage à balise issue du W3C), reprenant les mêmes contraintes et bonnes pratiques.

HTML 5, cette version du langage est toujours en «brouillon» pour le W3C mais commence déjà à être utilisée largement sur le web. Faisant partie d’un ensemble de technologies appelées aussi HTML5 (comprenant aussi CSS3, SVG…), a fait d’HTML un langage encore plus puissant pour définir du contenu et son vocabulaire s’est étendu.


Les balises essentielles d’un document HTML
--------------------------------------------

### doctype

*doctype* (*DOCument TYPE*) est un élément qui permet d’indiquer au navigateur la version d’HTML qui va être utilisée dans le document qu’il est chargé d’afficher et adapte parfois son moteur de rendu en conséquence. (mode quirk par exemple, un mode dégradé permettant une retro-compatibilité du langage.)

Selon la version d’HTML utilisée, cet élément change :

**En HTML 4.01**

	<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">

**En XHTML**

	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">

**En HTML5**

	<!DOCTYPE html>

Certaines balises ont disparu et certaines ont été crées durant la vie de ce langage, en voici les principales.

### html

Le document HTML à proprement dit, il comprend essentiellement les balises *head* et *body*.

### Balise *head*

L’entête du document dans lequel on retrouve ses métas-informations, le titre du document (La balise *title*, affichée dans la barre de titre du navigateur), l’appel aux CSS, aux JS ainsi que d’autres méta-informations. Ces informations ne sont habituellement pas directement visibles dans la page rendue par le navigateur.

### Balise *body*

Le corps à proprement parler du document HTML, son contenu. On y trouve toutes les autres balises.

### Balise *div*

Cette balise n’a aucune valeur sémantique, elle ne sert qu’à regrouper des éléments entre eux de manière à leur donner un style particulier ou à les manipuler en JS.

### Balises de titrage

Dejà vue auparavant, *h1* à *h6*, donnent un plan au document par un sytème de titres et sous-titres.

### Des listes

Ordonnées *ol* ou non ordonnées *ul*, ces listes permettent de regrouper des éléments (*li*) qui ont un lien logique entre-eux.

### Balise de lien

Balise *a*, L’URL est fournie par l’attribut *href*. 
	
	<a href="http://www.apple.com">Le contenu du lien</a>

### Balises sémantiques de texte

Ses balises sont nombreuses, les principales sont

* *em*, une emphase (https://fr.wikipedia.org/wiki/Emphase);
* *strong*, une emphase forte;
* *abbr*, signale une abbréviation dont la signification est fournie par l’atribut *title*;
* *q*, citation simple dans une phrase;
* *cite*, permet de signaler la citation d’un titre d’une œuvre d’art par exemple;

Il existe d’autres balises sémantiques de niveau texte, peu utilisées.


### Balises HTML5

#### section
#### article
#### nav
#### header
#### footer
#### hgroup

### Balises forms

