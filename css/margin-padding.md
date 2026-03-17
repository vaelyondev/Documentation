# Margin et Padding en CSS

## Introduction
En CSS, `margin` et `padding` sont utilisés pour gérer les espacements autour des éléments.

## Padding (espacement interne)
Le `padding` correspond à l’espace entre le contenu et la bordure de l’élément.

### Exemple
```css
div {
  padding: 20px;
}
```

## Margin (espacement externe)
Le `margin` correspond à l’espace entre l’élément et les autres éléments autour.

### Exemple
```css
div {
  margin: 20px;
}
```

## Différence simple
- `padding` = espace à l’intérieur de l’élément
- `margin` = espace à l’extérieur de l’élément

## Raccourcis
```css
margin: 10px 20px 10px 20px; /* haut droite bas gauche */
padding: 10px 20px; /* haut/bas droite/gauche */
```

## Cas particulier
- `margin: auto` permet de centrer un élément horizontalement (souvent avec une largeur définie)

## Conclusion
Utiliser correctement `margin` et `padding` permet de mieux organiser et espacer les éléments sur une page web.