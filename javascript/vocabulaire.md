# Vocabulaire JavaScript

Ce document regroupe les principaux termes utilisés en JavaScript et dans le développement web.

## DOM (Document Object Model)

Le **DOM** est la représentation d'une page HTML sous forme d'objets.

Lorsque le navigateur charge une page HTML, il transforme chaque balise en un objet JavaScript.

Exemple :

```html
<body>
    <h1>Bonjour</h1>
    <p>Bienvenue.</p>
</body>
```

Le navigateur crée une structure similaire à celle-ci :

```
Document
│
└── body
    ├── h1
    └── p
```

Grâce au DOM, JavaScript peut :

- sélectionner des éléments ;
- modifier leur contenu ;
- modifier leur style ;
- créer de nouveaux éléments ;
- supprimer des éléments.

---

## Document

`document` représente la page HTML actuellement chargée.

Exemple :

```javascript
document.querySelector("h1");
```

Cette instruction recherche le premier élément `<h1>` de la page.

---

## Élément

Un élément est une balise HTML représentée sous forme d'objet JavaScript.

Exemple :

```html
<p>Bonjour</p>
```

Cette balise devient un élément du DOM.

---

## Nœud (Node)

Un **nœud** est un élément de la structure du DOM.

Les balises HTML, le document et même les textes sont des nœuds.

Tous les éléments HTML sont des nœuds, mais tous les nœuds ne sont pas forcément des éléments HTML.

---

## Sélecteur

Un sélecteur permet de retrouver un ou plusieurs éléments dans une page.

Exemples :

```javascript
document.querySelector(".menu");
```

```javascript
document.querySelector("#header");
```

```javascript
document.querySelector("img");
```

Les sélecteurs utilisent la même syntaxe que les sélecteurs CSS.

---

## Objet

Un objet est une structure qui regroupe plusieurs informations.

Exemple :

```javascript
const voiture = {
    marque: "Peugeot",
    couleur: "Rouge"
};
```

---

## Propriété

Une propriété est une information appartenant à un objet.

Exemple :

```javascript
voiture.marque
```

`marque` est une propriété.

---

## Méthode

Une méthode est une fonction appartenant à un objet.

Exemple :

```javascript
document.querySelector(".menu");
```

`querySelector()` est une méthode de l'objet `document`.

Autre exemple :

```javascript
element.classList.add("active");
```

`add()` est une méthode de `classList`.

---

## Fonction

Une fonction est un bloc de code réutilisable.

Exemple :

```javascript
function direBonjour() {
    console.log("Bonjour");
}
```

Une fonction est exécutée lorsqu'elle est appelée.

---

## Variable

Une variable permet de stocker une valeur qui peut être modifiée.

```javascript
let compteur = 0;
```

---

## Constante

Une constante permet de stocker une valeur qui ne peut pas être réaffectée.

```javascript
const nom = "Antoine";
```

---

## Tableau (Array)

Un tableau permet de stocker plusieurs valeurs dans une seule variable.

```javascript
const couleurs = [
    "Rouge",
    "Vert",
    "Bleu"
];
```

---

## Indice

Chaque élément d'un tableau possède un indice.

Les indices commencent toujours à **0**.

```javascript
couleurs[0]
```

---

## Événement (Event)

Un événement correspond à une action effectuée par l'utilisateur ou par le navigateur.

Exemples :

- clic ;
- appui sur une touche ;
- déplacement de la souris ;
- chargement de la page.

---

## Écouteur d'événement (Event Listener)

Un écouteur d'événement attend qu'un événement se produise.

Exemple :

```javascript
button.addEventListener("click", maFonction);
```

La fonction `maFonction` est exécutée lorsque le bouton est cliqué.

---

## API

Une **API** (*Application Programming Interface*) est un ensemble de fonctionnalités mises à disposition par un logiciel.

Le navigateur fournit plusieurs API utilisables en JavaScript.

Exemples :

- DOM API
- Fetch API
- Local Storage API
- Clipboard API

---

## Console

La console est un outil de développement intégré au navigateur.

Elle permet notamment :

- d'afficher des messages ;
- de tester du code ;
- de consulter les erreurs JavaScript.

Exemple :

```javascript
console.log("Bonjour");
```

---

## Instruction

Une instruction est une ligne de code exécutée par JavaScript.

Exemple :

```javascript
let age = 25;
```

---

## Expression

Une expression est un morceau de code qui produit une valeur.

Exemples :

```javascript
2 + 3
```

```javascript
slides.length
```

```javascript
nom.toUpperCase()
```

---

## Syntaxe

La syntaxe correspond aux règles d'écriture du langage JavaScript.

Une erreur de syntaxe empêche le script de s'exécuter correctement.

---

## À retenir

Avant de commencer à programmer, il est important de distinguer quelques notions :

- Le **DOM** représente la page HTML.
- `document` représente cette page en JavaScript.
- Un **élément** correspond à une balise HTML.
- Un **objet** contient des propriétés et des méthodes.
- Une **propriété** est une information.
- Une **méthode** est une fonction appartenant à un objet.
- Un **événement** est une action détectée par JavaScript.
- Une **API** fournit des fonctionnalités prêtes à être utilisées.