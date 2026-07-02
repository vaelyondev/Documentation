# Les tableaux d'objets

Le code suivant déclare une constante nommée `slides` :

```javascript
const slides = [
	{
		"image": "slide1.jpg",
		"tagLine": "Impressions tous formats <span>en boutique et en ligne</span>"
	},
	{
		"image": "slide2.jpg",
		"tagLine": "Tirages haute définition grand format <span>pour vos bureaux et events</span>"
	},
	{
		"image": "slide3.jpg",
		"tagLine": "Grand choix de couleurs <span>de CMJN aux pantones</span>"
	},
	{
		"image": "slide4.png",
		"tagLine": "Autocollants <span>avec découpe laser sur mesure</span>"
	}
];
```

Cette structure est appelée un **tableau d'objets**.

- Les crochets `[]` représentent un tableau.
- Les accolades `{}` représentent un objet.
- Chaque objet contient les informations d'une diapositive.

## Le tableau

Un tableau (*Array*) permet de stocker plusieurs valeurs dans une seule variable.

Exemple :

```javascript
const fruits = [
    "Pomme",
    "Banane",
    "Orange"
];
```

Ce tableau contient trois éléments.

Les éléments d'un tableau sont numérotés à partir de **0**.

| Indice | Valeur |
| -----: | ------ |
|      0 | Pomme  |
|      1 | Banane |
|      2 | Orange |

Pour accéder à un élément :

```javascript
fruits[0];
```

Résultat :

```javascript
"Pomme"
```

## L'objet

Un objet permet de regrouper plusieurs informations concernant un même élément.

Exemple :

```javascript
const voiture = {
    marque: "Peugeot",
    modele: "208",
    couleur: "Rouge"
};
```

Cet objet possède trois propriétés :

- `marque`
- `modele`
- `couleur`

Chaque propriété est associée à une valeur.

| Propriété | Valeur  |
| --------- | ------- |
| marque    | Peugeot |
| modele    | 208     |
| couleur   | Rouge   |

Pour accéder à une propriété :

```javascript
voiture.marque;
```

Résultat :

```javascript
"Peugeot"
```

## Un tableau d'objets

Dans le projet du carrousel, le tableau `slides` contient plusieurs objets.

Chaque objet représente une diapositive.

```
slides
│
├── Objet 0
│     ├── image : "slide1.jpg"
│     └── tagLine : "Impressions..."
│
├── Objet 1
│     ├── image : "slide2.jpg"
│     └── tagLine : "Tirages..."
│
├── Objet 2
│     ├── image : "slide3.jpg"
│     └── tagLine : "Grand choix..."
│
└── Objet 3
      ├── image : "slide4.png"
      └── tagLine : "Autocollants..."
```

Chaque objet possède les mêmes propriétés :

- `image`
- `tagLine`

Cette structure permet de regrouper toutes les informations d'une diapositive dans un seul élément.

## Les indices

Les objets sont stockés dans le tableau selon leur indice.

| Indice | Diapositive |
| -----: | ----------- |
|      0 | Première    |
|      1 | Deuxième    |
|      2 | Troisième   |
|      3 | Quatrième   |

Pour accéder au premier objet :

```javascript
slides[0];
```

Pour accéder au troisième objet :

```javascript
slides[2];
```

## Accéder à une propriété d'un objet

L'accès à une propriété s'effectue avec l'opérateur `.`.

Exemple :

```javascript
slides[0].image;
```

Décomposition :

- `slides` → le tableau.
- `[0]` → le premier objet du tableau.
- `.image` → la propriété `image` de cet objet.

Résultat :

```javascript
"slide1.jpg"
```

Autre exemple :

```javascript
slides[2].tagLine;
```

Résultat :

```javascript
"Grand choix de couleurs <span>de CMJN aux pantones</span>"
```

## Utilisation dans le projet

La variable `currentSlide` contient l'indice de la diapositive affichée.

```javascript
let currentSlide = 0;
```

Pour afficher l'image :

```javascript
bannerImage.src = slides[currentSlide].image;
```

Décomposition :

1. `currentSlide` contient un indice.
2. `slides[currentSlide]` récupère l'objet correspondant.
3. `.image` récupère le nom de l'image.

Si `currentSlide` vaut `0` :

```javascript
slides[0].image;
```

Résultat :

```javascript
"slide1.jpg"
```

Si `currentSlide` vaut `2` :

```javascript
slides[2].image;
```

Résultat :

```javascript
"slide3.jpg"
```

Le même principe est utilisé pour afficher le texte :

```javascript
bannerText.innerHTML = slides[currentSlide].tagLine;
```

## Schéma de lecture

```
slides[currentSlide].image
│
├── slides
│     Tableau
│
├── [currentSlide]
│     Objet situé à l'indice contenu dans currentSlide
│
└── .image
      Propriété de cet objet
```

## À retenir

- Les crochets `[]` représentent un tableau.
- Les accolades `{}` représentent un objet.
- Un tableau peut contenir plusieurs objets.
- Les indices d'un tableau commencent à **0**.
- L'accès à un élément d'un tableau s'effectue avec `tableau[indice]`.
- L'accès à une propriété d'un objet s'effectue avec `objet.propriete`.
- Pour accéder à une propriété d'un objet contenu dans un tableau, on combine les deux syntaxes :

```javascript
tableau[indice].propriete
```

Exemple :

```javascript
slides[1].tagLine;
```

Cette instruction récupère la propriété `tagLine` du deuxième objet contenu dans le tableau `slides`.