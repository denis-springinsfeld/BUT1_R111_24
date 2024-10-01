# TP2 : Images & Background Image

## Exercice 1 : Images

### ◼︎ Partie HTML

💻 Ajoutez à l'aide de l'élément <img>, une image à votre fichier 'index.html' de départ. Testez les attributs 'src', 'alt', 'width' et 'height'.

💡 [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/img)

Vous pouvez testez les différents **placeholder d'images** disponibles sur le web :

    https://unsplash.com/fr
    http://picsum.photos
    https://www.pexels.com
    https://i.pravatar.cc/{size}
    https://doodleipsum.com
    ...

    exemple :
    https://picsum.photos/480/320/?random
    https://source.unsplash.com/800x600/?design,graphic=1
    https://source.unsplash.com/800x600/?landscape

### ◼︎ Partie CSS

Il est possible de modifier les dimensions, le comportement des images à l'aide de CSS.
Appliquez les propriétés CSS suivantes à votre image :

- width
- height
- aspect-ratio
- max-width
- object-fit
- object-position
- border-radius

💻 Importez quelques images et testez les différentes propriétés CSS.

💻 Que se passe-t-il si vous donnez une dimension à votre image sans respectez pas le ratio de l'image ?
Quel est la propriété CSS qui permet de conserver retrouver une image non déformée ?

---

## Exercice 2 : Avatars

### ◼︎ Partie HTML

💻 Ajouter un composant **avatar** à votre page.
Donner un attribut de classe à ce composant en utilisant la méthodologie BEM (Bloc Element Modifier).

    COMPOSANT AVATAR :
        BLOCK
            .avatar (une simple div)
        ELEMENT
            .avatar__image (une balise img)
        MODIFIERS
            .avatar--small
            .avatar--large...

💻 Vous allez créer collection d'avatars, trouver une balise HTML permettant de représenter une liste d'éléments sans ordre particulier.

Ajouter des attributs de classe en utilisant la **méthodologie BEM** (cf. style.css).

```css
# COMPOSANT LISTE
    BLOCK
        .avatarList
    ELEMENT
        .avatarList__item


```

### ◼︎ Partie CSS

💻 Compléter le fichier style.css, aidez-vous du site [mdn](https://developer.mozilla.org/fr/).

---

## Exercice 2 : Background-images: Hero Header

### ◼︎ Partie HTML

Le **hero header** est un bandeau large en haut de page d’accueil d’un site web ou d’un blog. Le web design parle de bannière web.

💻 Ajouter une balise permettant de créer un élément qui représente du contenu introductif, ainsi qu'un titre.
Donner un attribut de classe à ces deux éléments en utilisant la méthodologie BEM (Bloc Element Modifier).
Nommer ces deux classes : `'hero-header'` et `'hero-header__heading'`.

💡 [BEM](https://getbem.com/introduction/)

### ◼︎ Partie CSS

💻 Compléter le fichier style.css, aidez-vous du site [mdn](https://developer.mozilla.org/fr/).

---

### Rappel

**Remarque sur l'ordre des déclarations**
Les déclarations au sein d'une règle CSS sont ordonnées de façon à faire apparaître les propriétés importantes en tête de liste.

Voici l'ordre dans lequel nous déclarons nos propriétés :

- **Propriété display** : tout ce qui affecte le rendu par défaut de l’élément
- **Positionnement** : tout ce qui détermine la position de l’élément
- **Modèle de boîte** : tout ce qui influe sur les dimensions de l’élément
- **Typographie** : tout ce qui détermine les caractéristiques de la police de caractères
- **Effets Viusels & Graphiques**
- **Transformations et transitions**
