Title:  HTML et CSS avec une pincée de javascript
Author: Gaëtan Ark
Email: gaetan.ark@gmail.com
Web: http://www.lespolypodes.com

# HTML, CSS et une pincée de javascript
## Histoire courte
### Le web est mort

**Le web est mort hier et renaît tous les jours** il est en perpétuelle évolution, c’est un média jeune et plein d’énergie et peu de chose restent figée dans le marbre si ce ne sont quelques principes et bonnes pratiques.

**Les navigateurs** (les logiciels permettant d’accéder au web) sont en évolution régulière, les mises à jour deviennent même invisibles à l’utilisateur.
**Les terminaux** sont en pleine révolution avec les plateformes mobiles, des tablettes… des frigos ?

La plupart de ces évolutions se font pour le bien de l’utilisateur, mais surtout pour le bien des acteurs de l’industrie qui ils y voient la possibilité de s’imposer.

### Des premiers jours chaotiques

Les premiers jours du web ont été chaotiques, chacun voulait se l’approprier, le garder pour lui tout seul, égoïstement.

Chacun développait sa propre manière de faire du web, un Internet basé sur ce principe n’avait pas de futur.

Il fallait alors imaginer un web dont chacun pourrait bénéficier, quelque soit son ordinateur, son navigateur, ses capacités physiques.

Un jolie rêve et **[Tim Berners Lee](https://fr.wikipedia.org/wiki/Tim_Berners-Lee)** l’a fait avec un idée merveilleuse : **les standards**, des langages communs utilisables par les navigateurs, les serveurs, les éditeurs de contenus… Tous les acteurs de l’industrie du web.

En 1994, il crée le *W3C*, le [world wide web consortium](http://www.w3.org/), une communauté internationale en charge de développer les lignes de conduite des technologies et des langages utilisés sur le web actuellement et dans le futur.

Cette communauté regroupe des utilisateurs, des chercheurs et des industriels(Apple, Microsoft, Nokia, Google, Adobe… [La liste complète](http://www.w3.org/Consortium/Member/List )).

Le web aurait un tout autre visage si cette initiative n’avait pas été prise, le W3C a fait évoluer le web, ses outils et ses usages et maintiendra un web pérenne.

## Le trio HTML, CSS et Javascript

HTML, CSS et Javascript sont des langages issus des standards par le W3C et servent à créer **des interfaces utilisateurs**.

Vous allez pouvoir maîtriser **les trois aspects d’une page web**:

* Sa **structure** de la page avec HTML;
* Sa **présentation** avec les CSS;
* Le **comportement** avec Javascript.

Au début du web ce trio était mélangé au sein de la page même mais de **bonnes pratiques** sont apparues et ces trois aspects de la page web sont maintenants indépendants les uns des autres.

### Séparation forme et contenu

La séparation de la forme et du contenu est **le point** important dans la conception web actuelle et permet d’améliorer les points suivants :

* Meilleure accessibilité des contenus, un utilisateur peut consulter ce site avec une *revue d’écran* (un outil lisant à voix haute les contenus web) sans pour autant perdre d’informations;
* Portabilité améliorée, il est plus simple de cette manière de porter un site sur différents supports et terminaux;
* Facilité de maintenance, le web et les usages évoluent régulièrement. Un site doit pouvoir suivre cette évolution facilement.
* Réduction du temps de latence et d’attente pour l’utilisateur en ayant un code efficace et optimisé.

Parmi les autres points notables il y a aussi une meilleure indexation par les moteurs de recherche.

## Dans langages *client*

Ce sont des langages dit *client* c’est à dire exécutés et affichés par le navigateur, contrairement au langages *serveur* qui sont eux réservés au… serveur (PHP, ASP, Ruby…).

Le web est encore essentiellement basé sur cette logique client-serveur, un navigateur se connecte à un serveur et va l’interroger, le serveur lui répond et le client affiche le résultat de cette requête.


## HTML, *HyperText Markup Language*
### Définition

HTML est un langage sémantique servant à structurer de l'information, essentiellement textuelle, de lui donner du sens et n’utilise pour cela que deux types d’informations, des **balises** et des **attributs**.
Ce langage est lu et restitué par des terminaux utilisant un navigateur (Firefox, Safari, Chrome…).

### Les balises
Une balise sert à délimiter des parties de contenus d’un document HTML et s’écrit de la manière suivante. Cette balise est la balise ouvrante. 

	<article>

Afin de créer un élément HTML il est nécessaire de lui adjoindre un balise fermante de cette manière.

	<article>Contenu de la balise</article>

Cet ensemble, une balise ouvrante et fermante (souvent avec du contenu) crée ce que l’on appelle **un élément** c’est un objet HTML ayant ou non du contenu.
Un élément peut, selon les balises utilisée être un titre, une image, un lien, un paragraphe… HTML dans sa dernière version donne un large éventail de balises permettant un structuration *sémantique* du contenu.

Les balises peuvent s’imbriquer et donner un arbre de contenu.

#### Les balises sans contenu
Certaines balises sont dites vides car elles ne contiennent rien… Par exemple la balise permettant de faire les retours chariot n’a pas de contenu propre. C’est une balise *auto-fermante* et se saisit de la manière suivante :

	<br />

### Les attributs
Afin de fournir des informations complémentaires, chaque élément peut avoir un ou plusieurs attributs.

	<a href="http://www.apple.com">Le contenu du lien</a>

Dans l’exemple précédent la balise ``<a> ``, un lien, à un attribut ``href`` dont la valeur, indiquée entre guillemets est une *URL (Universal Ressource Locator)*, l’adresse d’un site.
L’utilisateur cliquant sur ce lien sera alors dirigé vers l’adresse indiquée.

### Quelques balises
Les balises que nous allons voir sont les balises les plus utilisées en HTML toutes versions confondues.

#### Titres
Les titres (*header*) ont jusqu’à 6 niveaux et se saisissent ainsi :

	<h1>Ici un titre de niveau 1</h1>
	<h2>Le sous-titre de niveau 2</h2>
	<h3>…</h3>

Les titres donnent le **plan principal du document** HTML. L’ordre dans lequel ils apparaissent a leur importance, un ``<h3>`` ne devrait pas être précédé d’un ``<h1 >`` mais d’un ``<h2>`` afin de respecter la lecture hierarchique et logique du document.s
	
#### Listes
Il existe plusieurs types de liste en HTML, la plus utilisée est la  liste sans ordre ``<ul>`` (*Unordered List*) et elle contient des éléments de liste ``<li>`` (*List Item*).
	
	<ul>
		<li>Element de la liste</li>
		<li>Autre élément de la liste</li>
		<li>Encore un autre élément de la liste</li>
	</ul>

L’exemple idéal de contenu pour ce type de liste est une liste de course, c’est un groupe d’élément dont l’ordre n’a pas d’importance. Souvent utilisées pour les éléments de navigation.

#### Le lien
Le lien est le web… Il est surtout un élément qui permet à un auteur de lier un contenu, un site, à sa page :

	<a href="http://www.apple.com">Le contenu du lien</a>

 En cliquant ce lien l’utilisateur est dirigé vers l’URL (*Universal Ressource Locator*) indiquée dans l’attribut ``href``.

#### Les images
La balise pour indiquer une image fait partie des balises qui n’ont pas de contenu, c’est une balise auto-fermée. C’est une balise pour laquelle l’attribut ``alt``est obligatoire.

	<img src="images/logo.png" alt="Le logo" />

L’adresse de l’image est indiquée dans l’attribut ``src`` elle se trouve dans le dossier « images » situé au même niveau que la page.

Si cette dernière n’est pas chargée ou si mes capacités physiques ne me permettent pas de la voir, L‘attribut ``alt`` sert à être affiché comme **alternative à l’image**.

#### Un paragraphe

Un paragraphe est une idée développée sur plusieurs lignes, peut comporter plusieurs phrases et s’indique comme ça en HTML

	<p>Le paragraphe ne sert pas à indiquer des retours chariot mais à structurer un document.</p>

###Exercice pratique de la sémantique HTML de base
* Intégration HTML d’une page simple, on vous fournit le fichier suivant : http://cl.ly/JMLT;
* Lancez DreamWeaver et intégrons cette page ensemble;


