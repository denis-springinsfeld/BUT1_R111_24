# R111 - TD1 - 2024/2025

## 1. Setup : Installation des outils

### 1.1. Navigateur par defaut: Firefox

Modifier votre navigateur par défaut dans Windows :

- Sélectionnez Démarrer > Paramètres > Applications > applications par défaut. Ouvrir les applications par défaut.
- Sélectionnez **Firefox**.
- En regard de Définir **Firefox** comme navigateur par défaut, sélectionnez Définir par défaut.

### 1.2. VisualCode

- Installer l'extension ['Live server'](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
- Installer l'extension ['Prettier'](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

### 1.3. Répertoire de travail

- Télécharger le répertoire `TD1_start` sur votre bureau :

  > Bouton en haut à droite `Télécharger`> `Download ZIP`

- Ouvrir `Visual Studio Code` et ouvrir votre dossier `Td1_start`.

> Architecture de votre répertoire :

```bash
    TD1_start/
      L css/
      L assets/
        - image1.jpg
        - hero.png
```

## 2. Ma Page HTML

### 2.1. Créer un fichier `index.html`

- Créer un fichier `index.html` à la racine de votre répertoire, celui-ci est vide.

> Nouvelle architecture de votre répertoire :

```bash
    TD1_start/
      L css/
      L assets/
        - image1.jpg
        - Hero.png
      - index.html
```

- `Emmet` (plugin intégré à VSCode), est un outil permettant de simplifier l'écriture du HTML et du CSS.

- Initialiser votre page HTML avec le raccourci **[! + tabulation]** :

> vous obtenez la **structure minimale** d'une page HTML

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

- Utiliser une balise `<h1>` (Titre de niveau 1) et écrire "HELLO HTML".
- [Clic droit] sur votre fichier html > Sélectionner : **Open with Live Server**.
- Votre page doit s'ouvrir dans le navigateur par défaut ici Firefox.

- Ouvrir l'inspecteur d'élément : [Clic droit] sur la page > **Inspecteur d'élément**.

- Utiliser une balise `<p>` (paragraphe) et écrire "CSS is AWESOME".
- Utiliser une balise `<img>` (image) et ajouter une image de votre choix, voir doc [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/img).

### 2.2 CSS

- Ajouter un dossier nommé `css` à votre répertoire `Td1_start`, puis un fichier `style.css`.
- Lier votre fichier `index.html` et votre fichier `style.css` avec la balise `link` (cf CM ou [MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/link)).
- Donner forme à votre page:
  - Regarder sur MDN les propriété `color` et `background` et les appliquer à votre page.
  - Regarder sur MDN la propriété `font-family` et l'appliquer une police sans serif à votre page...

### Liens utiles :

- [MDN](https://developer.mozilla.org/fr/)
- [Wev.dev](https://web.dev/learn/)
