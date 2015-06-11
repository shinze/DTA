## HTML 5

HTML5 est la dernière version de HTML, il est le successeur de HTML 4.01. Il corrige la plupart des difficultés rencontrées avec sa version 4.01 et permet de faire évoluer le web vers les applications web ce que ne permettait pas son ancêtre.
HTML 5, comme HTML 4, existe aussi dans une version XML (XHTML 5).

La spécification n’est pas encore validée mais le W3C encourage les auteurs (vous) à utiliser le langage.

## Les principales différences HTML 4.01 vs. HTML 5

### Simplification de la déclaration de doctype 

**Exemples de doctype HTML 4 et XHTML**

	<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">

	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">

**En HTML5**

`<!DOCTYPE html>` ou `<!doctype html>`

Beaucoup plus simple à utiliser, plus aucune référence à une DTD quelconque, le langage se simplifie.

### Simplification des informations d’encodage

Le processus de détection de l’encodage a légèrement changé, mais la déclaration au sein du document s’est largement simplifiée.

**En HTML 4**

	<meta http-equiv="Content-Type" content="text/html;charset=utf-8" />

**En HTML5**

	<meta charset="UTF-8" />

### La structure HTML 5, le document de base

	<!doctype html>
	<html>
		<head>
			<meta charset="UTF-8">
			<title>Le titre</title>
		</head>
		<body>
		</body>
	</html>

## De nouvelles balises

HTML5 permet de réaliser des documents ayant plus de sens.

* `section` définit les sections d’un document HTML, et peut être utilisé en association avec les titre afin de fournir une structure de document plus dense;
* `article` représente une partie de contenu comme un billet de blog ou un article de journal;
* `aside` permet de signaler du contenu qui aurait un lien avec le reste de la page;
* `hgroup` permet de signaler l’entête d’une section et peut contenir les titres h1, h2… h6
* `header` utilisé pour signaler l’entete d’un document ou l’entête d’une section;
* `footer` représente un pied pour un document ou pour une section, peut contenir la signature ou le nom de l’auteur par exemple.
* `nav` pour les outils de navigation principaux d’un document;
* `figure` utilisable pour des éléments de contenu autonomes, comme des images, de la video, des illustrations;
* `figcaption` fournit une légende aux éléments ajoutés à `figure`
* `audio` et `video` permettent l’insertion de contenus *multimédias*
* `time` permettant de donner une information liée à l’heure, à la date;
* `canvas` permet le rendu de graphismes dynamiques comme des jeux ou des graphs dynamiques.

Cette liste n’est pas exhaustive, mais regroupe les principales balises sémantiques venant s’ajouter aux balises d’HTML 4.

## Les formulaires

Les formulaires évoluent et l’élément `input` évolue largement avec l’ajout de nouveaux types (tel, search, url, email, datetime, date, month, week, time, datetime-local, number, range et color) permettant à cet élément de saisir et de comprendre de nouveaux types de données.

Il est maintenant possible de rendre un `input` obligatoire à la saisie et le navigateur offre même une interface aux erreurs de saisies.


## Les modèles de contenus

En HTML 4 les blocs étaient dits de type *block (bloc)* (ex. `body`) ou *inline (en ligne)* (ex. `img`, `em`, `span`…), ainsi il était possible d’insérer des éléments *inline* dans des éléments *bloc* mais pas le contraire.

Le problème essentiel étant une confusion avec le modèle visuel utilisé en CSS.

HTML 5 le nombre de ces éléments a été augmenté afin de donner encore plus de finesse au langage.

Les nouveaux types d’éléments sont les suivants :

* Méta-données (ex. `scripts`, `link` `meta`, `title`) les éléments ajoutant de l’information en complément du document principal;
* Contenus du flux (ex. `span`, `div`) la plupart des balises utilisées dans le corps du document;
* Éléments de sections (ex. `article`, `aside`, `nav`, `section`) qui peuvent contenir des `header` et des `footer`;
* Éléments d’entête (ex. `h1 … h6` et `hgroup`);
* Contenus texte (ex. `p`, `a`, `em`), le texte du document;
* Les éléments embarqués, les `img`, `iframe`, `svg` des contenus étant importés dans le document;
* Les contenus interactifs (ex. `a`,`button`,`input`), tous les éléments qui ont un dispositif d’activation (comme une vidéo sur laquelle on doit cliquer pour la lancer).

Mieux comprendre les différents types fournit par HTML 5 : http://www.whatwg.org/specs/web-apps/current-work/multipage/elements.html#content-categories

## Les API

Parmi les nouveautés essentielles apportées à HTML, il n’y a pas que la partie qu’est le code, il y a aussi l’ajout de nouvelles API (un interface simplifiant l’accès des auteurs par du code à différents types d’informations).

Ces API permettent par exemple la création d’applications `offline`, de stocker des données sur le navigateur de l’utilisateur. De connaître la géolocalisation de l’utilisateur, d’imprimer le document, de glisser-déposer des éléments de la page, de connecter deux utilisateurs directement sans passer par un serveur (en mode P2P, peer to peer).

Le langage Javascript se retrouve donc étendu de nouvelles fonctionnalités beaucoup plus larges.


## Le support dans les navigateurs, comment l'utiliser dans IE

La plupart des navigateurs modernes peuvent utiliser ces nouveautés, encore avec quelques petites différences. Les éditeurs avancent dans de nouvelles versions implémentant ces nouvelles fonctionnalités dès qu’elles sont mises à disposition par les groupes de travail du associés au W3C.

### Le petit problème

Le petit problème est nommé la nouveauté, les anciens navigateurs ainsi que les dernières versions d’Internet Explorer ne supportent pas ces nouveaux éléments.

Il est assez simple, avec l’aide de quelques libraires (https://github.com/aFarkas/html5shiv/, http://www.modernizr.com) de leur faire reconnaître et de pouvoir utiliser HTML5.

Le langage sera reconnu, les structures d’informations seront présentes mais ces anciens navigateurs ne pourront pas directement implémenter des fonctionnalités qu’apportent le langage comme pour les formulaires par exemple.

Il sera sans doute nécessaire alors de trouver des solutions existantes avec HTML4 ou des alternatives en javasscript, ce que l’on nomme des *polyfills*, des librairies simples comblant ces manques (http://html5please.com/).


## Références et lectures

* http://dev.w3.org/html5/html4-differences/, les différences entre HTML4 et 5, document technique.
* http://www.alistapart.com/articles/previewofhtml5
* http://diveintohtml5.info, un livre entier à propos d’HTML5, à ne pas manquer.
* http://html5doctor.com, une ressource à propos des balises d’HTML et leur sémantique.
* http://developers.whatwg.org, une ressource pour les développeurs HTML 5.
* http://www.abookapart.com/products/html5-for-web-designers, un livre pour débuter avec HTML 5, très simple mais suffisant pour commencer.
* http://www.alsacreations.com/article/lire/750-HTML5-nouveautes.html, article d’une étudiante à propos d’HTML 5.
* http://miageprojet2.unice.fr/Intranet_de_Michel_Buffa/Option_web_2.0_Master_1_informatique_2011/HTML5, une liste de ressources sur le sujet.

## Des outils
* http://html5boilerplate.com, un outil permettant de débuter un projet HTML 5 rapidement.
* http://html5please.com/, une liste des nouveautés, de leur implémentation et des *polyfills* correspondants.
* http://modernizr.com/, une librairie permettant facilement de détecter les capacités des anciens navigateurs.
* https://github.com/aFarkas/html5shiv/blob/master/readme.md, une petite librairie JS permettant aux anciens navigateurs de reconnaitre les nouvelles balises HTML 5

## Cheat sheets

* http://adactio.com/extras/pocketbooks/html5/
* http://www.inmotionhosting.com/infographics/_img/html5_cheat_sheet_tags.png