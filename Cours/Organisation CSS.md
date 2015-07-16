# Mieux organiser son travail

## De la méthode
Vous pouvez organiser votre travail comme vous le souhaitez mais ça ira mieux pour vous comme ça.

1. L’HTLM, coder les parties principales de votre site;
2. Passer aux CSS;
3. Itération bloc par bloc pour améliorer l’ensemble. Le code CSS et HTML.

## De l’organisation des CSS
Un fichier CSS se doit d’être un fichier *maintenable*, essayez d’en faire quelque chose de simple et pour cela les outils que vous allez avoir sont les commentaires et la structure (l’ordre) de votre code.
Essayez la consistence dans votre code, c’est votre style. Par exemple si vous commentez et nommez vos éléments en anglais, conservez cette logique sur la longueur de votre fichier.

### Commentez votre code
Un commentaire sert de point de repère dans un premier temps, il permet de comprendre la structure et l’organisation d’un fichier CSS en marquant les différentes sections du document.

Mais ce commentaire est aussi un outil qui permet de documenter votre code sur les parties les moins «limpides» de ce code, ce qui n’est pas évident.

Vous devez imaginer lorsque vous codez que ces commentaires seront lus par quelqu’un d’autre et qu’il doit comprendre ce que vous avez souhaité faire.

Le commentaire est pour *les autres* mais aussi pour vous lorsque vous allez reprendre votre projet dans quelques semaines/mois/années…

Exemple de commentaires utiles :

    /* ================= Resets ====================

     * Surcharge des styles par défaut du navigateur
     * afin de rendre les styles cohérents sur tous les
     * navigateurs
     */

    /* Modification du 'box-model' :
     * Info : paulirish.com/2012/box-sizing-border-box-ftw/
     */

    *,
    *:after,
    *:before {}

    /* Styles génériques pour les balises */
    body {}
    h1,…,h6 {}
	
	
	
	
    /* ================= Mon bouton play ====================

    * Le bouton play est utilisé sur la page lorem upsum
    *
    * Exemple de structure :
    * -------------------------------------
    * <div id="play-button">
    *   <a href="#"><span></span></a>
    * </div>
    */

    #play-button {}
    #play-button a {}
    #play-button span {}

### De la structure
L’ordre des sélecteurs en CSS a une grande importance pour la cascade de vos styles mais aussi pour améliorer la lecture et la compréhension de votre code.

Un principe général à appliquer : **Du plus générique au plus spécifique**.

Cette règle prévaut sur l’organisation générale de votre fichier mais aussi sur l’organisation locale de vos sélecteurs.

Un **MAUVAIS** exemple :

	#play-button a {}
	h1  {}
	#play-button span  {}
	div  {}
	#play-button  {}
	body  {}


Dans cet exemple la lecture de l’information n’est pas fluide, l’ordre des éléments et leur zone d’application ne sont pas en relation.

Voici l’exemple corrigé, dans un premier temps une organisation très générique puis ensuite le bouton play qui est spécifique et enfin le détails de ce bouton :

	/* Tags */
	body  {}
	div  {}
	h1  {}

	/* Bouton play */
	#play-button  {}
	#play-button a {}
	#play-button span  {}

## Quelques idées, notions complémentaires

Quelques idées que vous pouvez utiliser en complément: 

### Listez vos couleurs en entête de votre fichier CSS

    /* ================= Couleurs utilisées ====================
    # Gris foncé (texte): #333333
    # Bleu foncé (entetes, liens) #000066
    # Bleu moyen (entete) #333399
    # Bleu clair (navigation du haut) #CCCCFF
    # Gris moyen: #666666
    # */

### Évitez les noms de class ou d’id non sémantiques

Nommer vos éléments sur leur fonctions et non sur leur aspect visuel.

	/* un MAUVAIS exemple */
	.lien-rouge {}
	#navigation-haute {}

	/* Un meilleur exemple */
	.lien-important {}
	#navigation-principale {}

### Donnez de l’ordre à vos déclaration de lien pour ne pas avoir de surprise (LoVe/HAte : LVHA)

	/* Mes liens sont ordonnés :
	Merci : http://meyerweb.com/eric/css/link-specificity.html */
	a:link {}
	a:visited {}
	a:hover {}
	a:active {}

### Debug rapide
Cela vous permet de voir rapidement l’emplacement de vos éléments et d’éventuellement mieux comprendre votre problème.

* {outline: 1px solid blue }


### Privilégiez l’utilisation des classes

Réutilisable, moins conflictuelles














