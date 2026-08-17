````md
# Mémo JavaScript

## Les symboles

### `()`

Les parenthèses servent principalement à :

- appeler une fonction ;
- mettre les paramètres d'une fonction ;
- mettre une condition.

```javascript
maFonction();

function bonjour(nom) {
    // ...
}

if (age >= 18) {
    // ...
}
````

**À retenir :** `()` → fonctions et conditions

---

### `[]`

Les crochets servent principalement à créer un **tableau** et à accéder à ses éléments.

```javascript
const fruits = ["Pomme", "Banane", "Orange"];

fruits[0];
```

`fruits[0]` récupère le premier élément du tableau.

**À retenir :** `[]` → tableaux

---

### `{}`

Les accolades servent principalement à créer un **objet** et à délimiter un bloc de code.

```javascript
const voiture = {
    marque: "Peugeot",
    modele: "208"
};
```

Elles sont également utilisées avec les fonctions, les conditions et les boucles :

```javascript
if (age >= 18) {
    console.log("Majeur");
}
```

**À retenir :** `{}` → objets et blocs de code

---

# Petit vocabulaire

### Variable

Une valeur que l'on stocke sous un nom.

```javascript
let age = 25;
```

**`age` = variable**

---

### Constante

Une valeur qui ne peut pas être réassignée.

```javascript
const nom = "Antoine";
```

**`nom` = constante**

---

### Fonction

Un bloc de code que l'on peut appeler.

```javascript
function bonjour() {
    console.log("Bonjour");
}
```

**`bonjour()` = fonction**

---

### Paramètre

Une information qu'une fonction peut recevoir.

```javascript
function bonjour(nom) {
    console.log(nom);
}
```

**`nom` = paramètre**

---

### Argument

La valeur donnée à un paramètre lorsqu'on appelle la fonction.

```javascript
bonjour("Antoine");
```

**`"Antoine"` = argument**

---

### Objet

Un ensemble d'informations regroupées.

```javascript
const voiture = {
    marque: "Peugeot",
    couleur: "Rouge"
};
```

**`voiture` = objet**

---

### Propriété

Une information contenue dans un objet.

```javascript
voiture.marque;
```

**`marque` = propriété**

---

### Méthode

Une fonction appartenant à un objet.

```javascript
console.log("Bonjour");
```

**`log()` = méthode de `console`**

---

### Tableau

Une liste de valeurs.

```javascript
const fruits = ["Pomme", "Banane", "Orange"];
```

**`fruits` = tableau**

---

### Indice

La position d'un élément dans un tableau.

```javascript
fruits[0];
```

**`0` = indice**

Les indices commencent toujours à `0`.

---

### Condition

Une vérification qui peut être vraie ou fausse.

```javascript
if (age >= 18) {
    // ...
}
```

**`age >= 18` = condition**

---

### Boucle

Du code qui est répété plusieurs fois.

```javascript
for (let i = 0; i < 5; i++) {
    // ...
}
```

**`for` = boucle**

---

### Opérateur

Un symbole qui permet d'effectuer une opération.

```javascript
age + 1;
```

**`+` = opérateur**

```javascript
age === 18;
```

**`===` = opérateur**

---

## Résumé

```text
() → fonctions / conditions

[] → tableaux

{} → objets / blocs de code

variable → valeur stockée sous un nom

fonction → bloc de code réutilisable

paramètre → information reçue par une fonction

argument → valeur envoyée à une fonction

objet → ensemble d'informations

propriété → information d'un objet

méthode → fonction d'un objet

tableau → liste de valeurs

indice → position dans un tableau

condition → vérification

boucle → répétition

opérateur → symbole qui effectue une opération
```

```
```
