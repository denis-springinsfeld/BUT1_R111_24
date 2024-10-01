# TP1 : L'élément a comme Button

Installer les plugins suivants :

- Live Server
- Prettier
- Markdown Preview Enhanced

Parmétrer Firefox comme navigateur par défault.

## Exercice 1 : Basic Button

### 1.1/ Mise en place Html

L'élément HTML `<a>` (pour ancre ou anchor en anglais), avec son attribut `href`, crée un lien hypertexte vers des pages web, des fichiers, des adresses e-mail, des emplacements se trouvant dans la même page, ou tout ce qu'une URL peut adresser.

https://developer.mozilla.org/fr/docs/Web/HTML/Element/a

💻 Ajouter une ancre à votre page.

#### ◼︎ Créer un lien vers une URL absolue

💻 Ajouter un url à votre attribut `href` pour créer un lien vers la page de Mozilla.

##### \_ Créer des liens vers des URL relatives

💻 Ajouter un fichier `page2.html` à votre répertoire de travail.
Ajouter un url à votre attribut `href` pour créer un lien vers la `page2.html` de votre répertoire.

##### \_ Créer un lien vers un élément de la même page

💻 Ajouter un paragraphe `<p>` après votre ancre.
Utiliser Emmet pour créer du texte de substitution [lorem1000 + tab].
Créer un élément avec un identifiant : `rubrique-down`

```html
<!-- Rubrique à relier -->
<h2 id="rubrique-down">Section plus bas</h2>
```

Ajouter l'url `#rubrique` à l'attribut `href` de votre ancre.

💻 Même exercice avec un lien vers le haut de la page.

💻 Dans le fichier `style.css`, au sélecteur d'élément `htm` ajoutez la propriété `scroll-behavior: smooth;`.
Que pouvez vous observer ?

```css
html {
  scroll-behavior: smooth;
}
```

### 1.2/ Les Styles CSS

Commentez tous votre travail `<!-- -->`.

💻 Ajouter un nouveau lien à votre page html `'basic button'` contenant un attribut de **classe `'btn'`**.

**Remarque sur l'ordre des déclarations**
Les déclarations au sein d'une règle CSS sont ordonnées de façon à faire apparaître les propriétés importantes en tête de liste.

Voici l'ordre dans lequel nous déclarons nos propriétés :

- **Propriété display** : tout ce qui affecte le rendu par défaut de l’élément
- **Positionnement** : tout ce qui détermine la position de l’élément
- **Modèle de boîte** : tout ce qui influe sur les dimensions de l’élément
- **Typographie** : tout ce qui détermine les caractéristiques de la police de caractères
- **Effets Viusels & Graphiques**
- **Transformations et transitions**

#### ◼︎ Styles

💻 Compléter le fichier `style.css`, aidez vous du site [mdn](https://developer.mozilla.org/fr/).

#### ◼︎ Styles d'état

À l'heure actuelle, le seul retour visuel qu'un utilisateur reçoit lorsqu'il tente d'interagir avec les boutons est le passage du curseur à la variante "pointeur".

Il existe trois états, effectuez une recherche sur mdn.

`:hover`

`:focus`

`:active`

Ce sont des `pseudo-classe` qui permettent de définir le style d'un élément en fonction de son état.

Une transition pourra être ajoutée dans le bloc de déclaration de la classe `.btn` (en dehors de la règle `:hover`) pour être appliquée à la fois sur le 'over' en entrée et sur le 'out' en sortie.

💻 Ajouter un état `:hover`et un état `:active`à votre bouton.

---

## Exercice 2 : Basic Button + Custom Properties

💻 Modifier votre code de l'exercice 1, en utilisant des variables CSS

Les **propriétés personnalisées CSS** (custom properties en anglais, aussi parfois appelés variables CSS) sont des entités définies par les développeurs ou les utilisateurs d'une page Web, contenant des valeurs spécifiques utilisables à travers le document.

- Elles sont initialisées avec des propriétés personnalisées par exemple :
  `--main-color: hsl(0 0% 0%);`
- et accessibles en utilisant la notation spécifique `var()` par exemple :
  `color: var(--main-color);`

Des sites et applications web complexes peuvent avoir des feuilles de style où de nombreuses valeurs sont répétées. Les propriétés personnalisées permettent de stocker une valeur à un endroit puis de réutiliser cette valeur (on factorise ainsi le code) et facilite les modifications.

https://developer.mozilla.org/fr/docs/Web/CSS/Using_CSS_custom_properties

https://css-tricks.com/a-complete-guide-to-custom-properties/

---

## Exercice 3 : Variantes de style et méthode BEM

https://getbem.com/introduction/

BEM : Bloc - Element - MODIFIER

En utilisant le convention d'écriture BEM, nous allons créer un petit bouton avec `la classe button--small` en réduisant simplement la taille de la police. Puisque nous avons défini la marge interne en unité relative `em`, celle-ci se redimensionne proportionnellement à cette taille. Et `min-width` et `min-height` veilleront à ce que le bouton reste une zone tactile suffisamment grande.

```css
.button--small {
  font-size: 1.15rem;
}
```

💻 Proposez différentes variantes de vos boutons : petit, grand, max width, bords arrondis...

---

## Exercice 4 : Avec ou sans Icône

Il existe différentes solution pour intégrer une image en SVG :

- avec l'élément img

  Comme tous les formats d'image, les fichiers SVG peuvent être affichés à l'aide d'éléments img.
  Parce que le SVG est externe, son contenu ne peut pas être modifié en CSS.

- directement inline dans votre html
  Ici votre SVG peut être modifié en CSS.

```svg
    <svg viewBox="0 0 24 24" width="24" height="24">
    <!-- paths, shapes, etc. -->
    </svg>
```

💻 Ajouter l'image SVG (dossier assets) à votre bouton en utilisant les deux méthodes.
Avec la méthode inline, ajouter à la balise les deux attribut suivant :
`fill="currentColor"` et `class="btn__icon"`.
Renseignez-vous sur le mot-clé `currentColor`.

---

## Exercice 5 : Cascade & variables css

Utilisation de la cascade avec les variables CSS.

```css
body {
  --background: hsl(0 0% 100%);
}
.sidebar {
  --background: hsl(0 0% 50%));
}
.module {
  background: var(--background);
}
```

```html
<body> <!-- --background: white -->

  <main>
    <div class="module">
      I will have a white background.
    </div>
  <main>

  <aside class="sidebar"> <!-- --background: gray -->
    <div class="module">
      I will have a gray background.
    </div>
  </aside>

</body>
```

💻 Modifier votre code pour utiliser la cascade, en contextualisant vos variables css :

Exemple :

```css
  --clr-bg: var(--clr-light);
  --clr-fg: var(--clr-dark);
  --clr-border: var(--clr-dark);
  ...
```

## Plus

https://css-tricks.com/a-complete-guide-to-links-and-buttons/

https://moderncss.dev/css-button-styling-guide/
