# Flash, vidéo… Tout ce qui n’est pas du navigateur

À l'heure actuelle HTML5 permet l’ajout d’objets multimédias comme le son ou la vidéo via des balises appropriées (`<video>` et `<audio>`), mais la plupart des services de distribution de vidéos (Youtube, Dailymotion…) ne proposent que des vidéo lisibles par l’intermédiaire du plug-in Flash.

Les plug-ins sont aussi nombreux que les fonctionnalités qu’il proposent.

## Les plug-ins
Ce sont des extensions installées sur votre système qui viennent compléter les fonctionnalités de vos navigateurs.

Ils permettent comme Flash (le plus connu à l’heure actuelle) par exemple de lire de la vidéo, de faire tourner des jeux, voire même des applications entières.

Leur utilisation se réduit avec l’arrivée des capacités d’HTML5, mais sont encore largement présents.

## Comment mettre en place ces contenus

### Les plugins posent de nombreux problèmes	
- Ce sont souvent des technologies dans des formats dits *propriétaires* (des langages que seul l’éditeur du logiciel connaît);
- Les balises et les attributs utilisables pour ces plug-ins sont différents selon les navigateurs et leur versions;
- Il est nécessaire de détecter le support du plugin par l’utilisation souvent de Javascript;
- Les fichiers importables peuvent poser de gros problèmes d’accessibilité.

### Les balises
En HTML4 la balise *officielle* est `<object>` en HTML5, il est possible d’utiliser les balises `<object>` et `<embed>`.

Les deux balises cohabitent pour conserver la compatibilité avec les anciens navigateurs.

#### La méthode *standard*
Dans l’exemple suivant nous souhaitons intégrer un fichier PDF dans une page HTML.

	<object data="fichiers/exemple.pdf" type="application/pdf" width="400" height="400">
	Télécharger le fichier : <a href="fichiers/exemple.pdf">test.pdf</a>
	</object>

 La balise comporte un attribut `data` permettant d’indiquer la source d’un fichier à afficher, l’attribut type permet d’indiquer le type `mime` du fichier à afficher et aide le navigateur à déterminer le plugin à utiliser.

Le contenu de la balise `<object>` est l’alternative qui sera fournie à l’utilisateur n’ayant pas le plugin nécessaire pour lire ce type de fichier.

Cette méthode standard ne fonctionne malheureusement pas partout… 

#### La méthode améliorée, sans javascript
Le problème de la méthode précédente est que certains navigateurs ne connaissent pas complètement la balise `object`.

Mais la balise `object` permet de fournir une alternative, une solution de remplacement si le navigateur ne parvient pas à afficher, pourquoi ne pas fournir comme alternative la balise que ces navigateurs connaissent…

C’est ce que fait cette méthode :

	<object data="fichiers/exemple.pdf" type="application/pdf" width="100%" height="100%">
	<embed src="fichiers/exemple.pdf" type="application/pdf"  width="100%" height="100%" />
	Télécharger le fichier : <a href="fichiers/exemple.pdf">test.pdf</a>
	</object>

**Les différents cas gérés par cet exemple**

1. La balise `object` est reconnue par le navigateur et l’utilisateur a le plugin : la navigateur affiche le PDF avec la balise `object`;
2. La balise `object` n’est pas reconnue, le navigateur cherche à afficher la balise `embed` avec le plugin adapté et si tel est le cas le PDF est affiché;
3. L’utilisateur n’a pas de lecteur PDF (de plugin) installé, on lui affiche un lien lui permettant de télécharger le fichier.


#### La méthode *la totale* pour Flash

Quand il s’agit d’un fichier PDF le problème est assez simple, l’utilisateur qui n’a pas le plug-in télécharge et consulte le fichier dans un outil adapté.

Mais quand il s’agit d’un fichier Flash, la plupart des utilisateurs n’ont aucun moyen de lire ce type de fichier, il est donc nécessaire de lui fournir les outils nécessaires pour installer le plugin.

Pour cela il existe swfObject, une libraire Javascript qui gère la détection du plugin ainsi que l’affichage des outils nécessaire à l’installation de ce plugin.

- https://code.google.com/p/swfobject/
- Comment l’utiliser : http://www.actionscript-facile.com/documentation-swfobject-afficher-flash-page-html/article1214713.html
- http://www.adobe.com/devnet/flashplayer/articles/swfobject.html

### Insertion de video par les balises HTML5

Afin d’insérer de la video et de l’audio il est aussi possible d’utiliser les balises propres du langage HTML5.

			<video controls="controls" width="640" height="264" poster="http://video-js.zencoder.com/oceans-clip.jpg" preload="auto">
		  <source type="video/mp4" src="http://video-js.zencoder.com/oceans-clip.mp4">
		</video>

La balise `video` permet donc d’insérer de la vidéo… Les balises sources permettent de fournir des alternatives aux différents navigateurs, car tous les navigateurs ne sont pas capables de lire tous les formats video.

**Le support video par les différents navigateurs**

- MP4 / H.264 : Safari (comprenant aussi iPhone/iPad), Chrome
- Ogg / Theora : 	Firefox, Opera, Chrome
- WebM / VP8 : Firefox, Opera, Chrome

- http://docteurhtml5.com/html5/balise-video/
- http://docs.sublimevideo.net/encode-videos-for-the-web 

Mais une librairie Javascript peut vous venir en aide :
- http://videojs.com/

Cette librairie permet l’insertion de vidéos au différents formats et de fournir les alternatives flash aux navigateurs n connaissant pas cette balise ou les formats vidéo fournis.

## Les services externes

La plupart des plateformes de diffusion vidéo proposent des solutions intégrées et simple pour insérer des vidéos. Elles prennent en charge la détection du plugin et rendent cette tache plus simple.

Chaque plateforme propose sa propre solution voire-même plusieurs options sur ce sujet. La plupart du temps ces insertions se font par le biais de la balise `iframe`.

**Exemple Youtube**

	<iframe width="560" height="315" src="http://www.youtube.com/embed/mzPxo7Y6JyA" frameborder="0" allowfullscreen></iframe>

**Exemple Dailymotion**

	<iframe frameborder="0" width="480" height="270" src="http://www.dailymotion.com/embed/video/xuz2rh"></iframe>

La balise `iframe` permet l’insertion de pages externes dans une page, on peut imaginer un navigateur dans un navigateur.

Comme la balise `object`, ce qui est inséré entre la balise ouvrante et la balise fermante est l’alternative affichée si le navigateur ne reconnait pas cette balise.

## Ressources externes
- http://www.alistapart.com/articles/flashembedcagematch/
- http://www.actionscript-facile.com/documentation-swfobject-afficher-flash-page-html/article1214713.html











