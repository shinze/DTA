<style>
body {font-size: 8pt}
</style>

# Les éléments de formulaire
## Description

Le formulaire d’une page HTML permet à l’utilisateur de saisir des données et de les envoyer à un serveur qui en fera le traitement. Un formulaire web ressemble à son équivalent papier, il peut comporter des boutons, des cases à cocher, des sélecteurs, des zones de saisie texte…

Un formulaire peut être utilisé par exemple pour renseigner une boutique en ligne avec ses nom, adresse, code postal, numéro de carte bleue ou encore permettre de saisir un texte que vous souhaitez rechercher dans un site.

## Structure et balises d’un formulaire

Ces champs de formulaires se saisissent dans un élément `<form>`.

	<form action="" method="get">
	… Le contenu du formulaire
	</form>

### Les différents types d’éléments de formulaire

Chaque champ de formulaire (sauf les éléments boutons) est associé à un label `<label></label>`. Ce label permet d’indiquer le type d’information attendue ou la valeur d’un champ.

L’association d’un label et d’un champ de formulaire se fait par  l’utilisation de la paire d’attributs _for_ et _id_ comportant la même valeur.

**Exemple**

	<label for="nom">Votre nom</label>
	<input type="text" id="nom" value="" />

<hr>
<label for="nom">Votre nom</label>
<input type="text" id="nom" value="" />
<hr>

Dans l’exemple précédent le _label_ indique à l’utilisateur qu’il doit saisir son nom. Le label est associée au champ car les attributs _for_ et _id_ partagent la même valeur.


#### Le champ texte court

Il permet la saisie d’un texte tenant sur une ligne, comme un identifiant, un code postal…
	
**Exemple**

	<label for="name">Votre nom de famille</label>
	<input type="text" value="" id="name" />

<hr>
<label for="name">Votre nom de famille</label>
<input type="text" value="" id="name" />
<hr>

#### Mot de passe

C’est un champ texte particulier dans lequel le contenu saisi n’est affiché que par une série de points;

	<label for="motdepasse">Votre mot de passe</label>
	<input type="password" value="" id="motdepasse" />

<hr>
<label for="motdepasse">Votre mot de passe</label>
<input type="password" value="motdepasse"  id="motdepasse" />
<hr>

#### La zone de texte

Elle permet la saisie d’un texte long tenant sur  plusieurs paragraphes, comme un commentaire ou le contenu d’un email par exemple;

	<label for="comment">Votre commentaire</label>
	<textarea id="comment"></textarea>

<hr>
<label for="comment">Votre commentaire</label>
<textarea id="comment"></textarea>
<hr>

#### Case à cocher

La case à cocher sert à sélectionner ou à indiquer une ou plusieurs options dans une série donnée;

	<h2>Votre parfum préféré</h2>
	<input type="checkbox" value="Chocolat" id="chocolat"/>
	<label for="chocolat">Chocolat</label>
	<input type="checkbox" value="Vanille" id="vanille"/>
	<label for="vanille">Vanille</label>

<hr>
<h2>Votre parfum préféré</h2>
<input type="checkbox" value="Chocolat" id="chocolat"/>
<label for="chocolat">Chocolat</label>
<input type="checkbox" value="Vanille" id="vanille"/>
<label for="vanille">Vanille</label>
<hr>

Il est possible comme dans l’exemple précédent de mettre le _label_ après le champ.

#### Bouton radio

Le bouton radio permet la sélection d’une seule option parmi des choix multiples;

	<h2>Aimez-vous les glaces</h2>
	<input type="radio" value="Oui" id="da" name="like" /><label id="da">Oui</label>
	<input type="radio" value="Non" id="niet" name="like" /><label id="niet">Non</label>

<hr>
<h2>Aimez-vous les glaces</h2>
<input type="radio" value="Oui" id="da" name="like" /><label id="da">Oui</label>
<input type="radio" value="Non" id="niet" name="like" /><label id="niet">Non</label>
<hr>

L’attribut _name_ identique permet d’indiquer que ces boutons radio partagent la même question et font donc partie du mêm groupe.


#### Fichier

Permet à l’utilisateur de parcourir son disque dur pour ajouter et envoyer un fichier lors de la saisie du formulaire;

**Exemple**

	<label for="photo">Envoyez-nous votre photo de glace</label>
	<input type="file" value="" id="photo" />

<hr>
<label for="photo">Envoyez-nous votre photo de glace</label>
<input type="file" value="" id="photo" />
<hr>

#### Sélecteur

Une liste déroulante dans lequel l’utilisateur peut sélectionner un ou plusieurs valeurs. Ce type de champ permet aussi le regroupement de données dans plusieurs catégories;

**Exemple**

	<label for="country">Votre pays d’origine</label>
	<select id="country">
		<option>France</option>
		<option>Espagne</option>
		<option>Angleterre</option>
	</select>

<hr>
<label for="country">Votre pays d’origine</label>
<select id="country">
<option>France</option>
<option>Espagne</option>
<option>Angleterre</option>
</select>
<hr>

Avec des groupes :

	<label for="country">Votre pays d’origine</label>
	<select id="country">
		<optgroup label="Europe">
		<option>France</option>
		<option>Espagne</option>
		<option>Angleterre</option>
		</optgroup>

		<optgroup label="États-unis">
		<option>Oregon</option>
		<option>Texas</option>
		<option>New-York</option>
		</optgroup>
	</select>

Le label sert de valeur de regroupement pour l’utilisateur (et sera affiché comme tel).
	
#### Les boutons

Les boutons permettent essentiellement de valider les formulaires mais d’autres types existent.

Un bouton de validation de formulaire.

**Exemple**

	<input type="submit" value="Enregistrer" />

<input type="submit" value="Enregistrer" />


Un bouton de remise à zéro.

	<input type="reset" value="Effacer le données" />

![Alt text](formulaire.GIF)

### L’organisation d’un formulaire

Il est nécessaire dans le cas de formulaires complexes d’organiser les données à saisir.

Pour cela il est possible de créer des sections au sein d’un formulaire complexe par le biais des balises _fieldset_ et _legend_.

Le _fieldset_ permettant de regrouper des champs de manière logique, la balise _legend_ servant de titre à cette section.

**Exemple**

	<form>
		<fieldset>
			<legend>Adresse de facturation</legend>
			… Les champs pour l’adresse de facturation …
		</fieldset>
		<fieldset>
			<legend>Adresse de livraison</legend>
			… Les champs pour l’adresse de livraison …
		</fieldset>
	</form>

<hr>
<form>
<fieldset>
<legend>Adresse de facturation</legend>
… Les champs pour l’adresse de facturation …
</fieldset>
<fieldset>
<legend>Adresse de livraison</legend>
… Les champs pour l’adresse de livraison …
</fieldset>
</form>
<hr>

Visuellement par défaut le navigateur créera un groupe (le _fieldset_) précédé d’un titre (la _legend_).

### Les nouveaux types de formulaire HTML5

Les formulaires vus précédemment sont les éléments disponibles en HTML dans sa version 4.01 ou XHTML.

HTML5 ajoute de nouveaux champs permettant de saisir d’autres types d’informations, en voici quelques-uns.

#### Les dates

Permet d’afficher un sélecteur de date sous forme de calendrier.

	<label for="anniv">Votre date d’anniversaire</label>
	<input type="date" id="anniv" />

#### Champ couleur

Donne à l’utilisateur la possibilité de spécifier une couleur par le biais d’un sélecteur de couleur dépendant du système d’exploitation.

	<label for="coulpref">Votre couleur préférée</label>
	<input type="color" id="coulpref" />

Ces champs ne sont pas encore disponibles dans tous les navigateurs.


**Pour en savoir plus sur les formulaires HTML**

* Les intégristes : http://www.lesintegristes.net/2009/02/03/concevoir-un-formulaire-html-qui-tient-la-route/
* Les labels : http://www.alsacreations.com/astuce/lire/6-utiliser-element-label-input-formulaires.html
* http://fr.wikibooks.org/wiki/Le_langage_HTML/Formulaires

**Pour en savoir plus sur les champs HTML5**

* Excellente ressource : http://www.pompage.net/traduction/formulaires-html5;
* Un example : http://yaccessibilityblog.com/examples/forms/html5-form.html.

