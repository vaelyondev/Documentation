# Installation de Sass

## 0. Qu'est-ce que Node.js ?
Node.js est un environnement qui permet d’exécuter du JavaScript en dehors du navigateur (côté serveur).
Il est basé sur le moteur V8 de Chrome et sert surtout à créer des applications web, des API ou des outils backend.
Grâce à npm, il donne accès à des milliers de packages pour développer rapidement.

## 1. Prérequis
- Avoir Node.js installé (https://nodejs.org)
- Vérifier avec : `node -v` et `npm -v`

## 2. Installation globale (optionnelle)
```bash
npm install -g sass
```

## 3. Installation locale (recommandée)
```bash
npm install sass --save-dev
```

## 4. Vérifier l'installation
```bash
sass --version
```

## 5. Compiler un fichier Sass
```bash
sass input.scss output.css
```

## 6. Mode surveillance (watch)
```bash
sass --watch input.scss:output.css
```

## 7. Structure simple
```
/project
  ├── index.html
  ├── scss/
  │     └── style.scss
  └── css/
        └── style.css
```

## 8. Exemple de index.html
```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Sass Test</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <h1>Hello Sass</h1>
</body>
</html>
```

## 9. Exemple de script (package.json)
```json
"scripts": {
  "sass": "sass --watch scss:css"
}
```

## 10. Lancer Sass via npm
```bash
npm run sass
```

## 11. Ressources
- https://sass-lang.com/install