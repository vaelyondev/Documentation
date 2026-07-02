# Comprendre un script JavaScript

Le script suivant crée automatiquement les points de navigation d'un carrousel.

```javascript
const dots = document.querySelector(".dots");

for (let i = 0; i < slides.length; i++) {
	const dot = document.createElement("div");

	dot.classList.add("dot");

	if (i === 0) {
		dot.classList.add("dot_selected");
	}

	dots.appendChild(dot);
}
```

## Vue d'ensemble

Le script effectue les opérations suivantes :

1. Sélectionne l'élément HTML qui contiendra les points.
2. Parcourt le tableau `slides`.
3. Crée un nouvel élément `<div>` pour chaque diapositive.
4. Ajoute la classe CSS `dot`.
5. Sélectionne le premier point.
6. Ajoute chaque point dans le conteneur HTML.

## Sélection d'un élément du DOM

```javascript
const dots = document.querySelector(".dots");
```

### Décomposition

- `document` représente la page HTML.
- `querySelector()` recherche un élément dans cette page.
- `".dots"` est un sélecteur CSS qui désigne l'élément ayant la classe `dots`.
- `const dots` stocke cet élément dans une constante.

Si le HTML contient :

```html
<div class="dots"></div>
```

Alors `dots` contient une référence vers cette balise.

## La boucle `for`

```javascript
for (let i = 0; i < slides.length; i++) {
```

Cette boucle s'exécute une fois pour chaque élément du tableau `slides`.

Elle se compose de trois parties.

### 1. Initialisation

```javascript
let i = 0;
```

La variable `i` est créée et vaut `0`.

Elle représente l'indice courant du tableau.

### 2. Condition

```javascript
i < slides.length
```

La boucle continue tant que `i` est inférieur au nombre d'éléments du tableau.

Si le tableau contient quatre éléments :

```javascript
slides.length // 4
```

Les valeurs successives de `i` seront :

| Passage | Valeur de `i` |
| ------: | :-----------: |
|       1 |       0       |
|       2 |       1       |
|       3 |       2       |
|       4 |       3       |

Lorsque `i` vaut `4`, la condition devient fausse et la boucle s'arrête.

### 3. Incrémentation

```javascript
i++
```

À la fin de chaque passage, la valeur de `i` augmente de 1.

Cette écriture est équivalente à :

```javascript
i = i + 1;
```

## Création d'un élément HTML

```javascript
const dot = document.createElement("div");
```

La méthode `createElement()` crée un nouvel élément HTML.

Ici, un nouvel élément `<div>` est créé à chaque passage dans la boucle.

Cet élément n'est pas encore affiché dans la page.

## Ajout d'une classe CSS

```javascript
dot.classList.add("dot");
```

La propriété `classList` permet de manipuler les classes CSS d'un élément.

La méthode `add()` ajoute une classe.

Après cette instruction, l'élément devient :

```html
<div class="dot"></div>
```

## Condition `if`

```javascript
if (i === 0) {
```

Cette condition vérifie si la variable `i` vaut exactement `0`.

L'opérateur `===` compare deux valeurs en vérifiant également leur type.

La condition n'est vraie qu'au premier passage dans la boucle.

## Sélection du premier point

```javascript
dot.classList.add("dot_selected");
```

Cette instruction ajoute une deuxième classe CSS uniquement au premier point.

Le premier élément devient :

```html
<div class="dot dot_selected"></div>
```

Les autres éléments restent :

```html
<div class="dot"></div>
```

## Ajout dans le DOM

```javascript
dots.appendChild(dot);
```

La méthode `appendChild()` ajoute un élément HTML comme enfant d'un autre élément.

À chaque passage dans la boucle, le nouveau point est ajouté dans le conteneur `dots`.

Avant la boucle :

```html
<div class="dots"></div>
```

Après quatre passages :

```html
<div class="dots">
	<div class="dot dot_selected"></div>
	<div class="dot"></div>
	<div class="dot"></div>
	<div class="dot"></div>
</div>
```

## Fonctionnement du script

Si le tableau `slides` contient quatre diapositives :

```text
Passage 1 → création du point 1 (sélectionné)
Passage 2 → création du point 2
Passage 3 → création du point 3
Passage 4 → création du point 4
```

À la fin de l'exécution, le nombre de points affichés correspond exactement au nombre de diapositives présentes dans le tableau.

## Notions utilisées

Ce script met en œuvre plusieurs concepts fondamentaux de JavaScript :

- Déclaration de constantes (`const`)
- Variables (`let`)
- Boucle `for`
- Conditions (`if`)
- Opérateur de comparaison (`===`)
- Tableau (`slides`)
- Propriété (`length`)
- DOM (`document`)
- Sélection d'un élément (`querySelector()`)
- Création d'un élément (`createElement()`)
- Manipulation des classes CSS (`classList.add()`)
- Ajout d'un élément dans le DOM (`appendChild()`)