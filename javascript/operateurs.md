# Les opérateurs JavaScript

Les opérateurs permettent d'effectuer des opérations sur des valeurs ou des variables.

Ils sont utilisés pour affecter une valeur, effectuer des calculs, comparer des valeurs ou encore modifier une variable.

## L'opérateur d'affectation (`=`)

L'opérateur `=` permet d'affecter une valeur à une variable.

```javascript
let age = 25;
```

La valeur `25` est affectée à la variable `age`.

L'opérateur `=` ne compare pas deux valeurs.

## Les opérateurs de comparaison

Les opérateurs de comparaison permettent de vérifier si deux valeurs sont égales ou différentes.

Le résultat d'une comparaison est toujours un booléen :

- `true`
- `false`

### Égalité simple (`==`)

L'opérateur `==` compare uniquement les valeurs.

Si les types sont différents, JavaScript tente de les convertir automatiquement avant la comparaison.

```javascript
5 == "5";
```

Résultat :

```javascript
true
```

Dans cet exemple, la chaîne de caractères `"5"` est convertie en nombre avant la comparaison.

L'utilisation de `==` est aujourd'hui déconseillée, car les conversions automatiques peuvent produire des résultats inattendus.

### Égalité stricte (`===`)

L'opérateur `===` compare la valeur **et** le type.

```javascript
5 === "5";
```

Résultat :

```javascript
false
```

Dans cet exemple :

- `5` est un nombre (`Number`)
- `"5"` est une chaîne de caractères (`String`)

Les valeurs se ressemblent, mais leur type est différent.

L'opérateur `===` est celui qui est le plus utilisé en JavaScript moderne.

### Différence (`!=`)

L'opérateur `!=` vérifie que deux valeurs sont différentes.

Comme `==`, il effectue une conversion automatique des types.

```javascript
5 != "5";
```

Résultat :

```javascript
false
```

### Différence stricte (`!==`)

L'opérateur `!==` compare la valeur et le type.

```javascript
5 !== "5";
```

Résultat :

```javascript
true
```

## Les opérateurs de comparaison numériques

### Supérieur (`>`)

```javascript
10 > 5;
```

Résultat :

```javascript
true
```

### Inférieur (`<`)

```javascript
5 < 10;
```

Résultat :

```javascript
true
```

### Supérieur ou égal (`>=`)

```javascript
10 >= 10;
```

Résultat :

```javascript
true
```

### Inférieur ou égal (`<=`)

```javascript
5 <= 3;
```

Résultat :

```javascript
false
```

## Les opérateurs arithmétiques

### Addition (`+`)

```javascript
5 + 3;
```

Résultat :

```javascript
8
```

L'opérateur `+` permet également de concaténer des chaînes de caractères.

```javascript
"Bonjour " + "Antoine";
```

Résultat :

```javascript
"Bonjour Antoine"
```

### Soustraction (`-`)

```javascript
10 - 3;
```

Résultat :

```javascript
7
```

### Multiplication (`*`)

```javascript
5 * 4;
```

Résultat :

```javascript
20
```

### Division (`/`)

```javascript
20 / 5;
```

Résultat :

```javascript
4
```

### Modulo (`%`)

Le modulo retourne le reste d'une division.

```javascript
10 % 3;
```

Résultat :

```javascript
1
```

Car :

```
10 ÷ 3 = 3
Reste = 1
```

Le modulo est souvent utilisé pour vérifier si un nombre est pair ou impair.

```javascript
8 % 2;
```

Résultat :

```javascript
0
```

## Les opérateurs d'incrémentation et de décrémentation

### Incrémentation (`++`)

L'opérateur `++` augmente une variable de `1`.

```javascript
let compteur = 0;

compteur++;
```

Résultat :

```javascript
1
```

Cette écriture est équivalente à :

```javascript
compteur = compteur + 1;
```

### Décrémentation (`--`)

L'opérateur `--` diminue une variable de `1`.

```javascript
let compteur = 5;

compteur--;
```

Résultat :

```javascript
4
```

Cette écriture est équivalente à :

```javascript
compteur = compteur - 1;
```

## Les opérateurs d'affectation composés

Ces opérateurs permettent de modifier une variable en utilisant une écriture plus courte.

### Addition (`+=`)

```javascript
let score = 10;

score += 5;
```

Équivalent à :

```javascript
score = score + 5;
```

Résultat :

```javascript
15
```

### Soustraction (`-=`)

```javascript
let vies = 10;

vies -= 2;
```

Équivalent à :

```javascript
vies = vies - 2;
```

Résultat :

```javascript
8
```

### Multiplication (`*=`)

```javascript
let points = 4;

points *= 3;
```

Équivalent à :

```javascript
points = points * 3;
```

Résultat :

```javascript
12
```

### Division (`/=`)

```javascript
let distance = 20;

distance /= 4;
```

Équivalent à :

```javascript
distance = distance / 4;
```

Résultat :

```javascript
5
```

## Les opérateurs logiques

### ET logique (`&&`)

L'opérateur `&&` retourne `true` uniquement si toutes les conditions sont vraies.

```javascript
age >= 18 && permis === true;
```

### OU logique (`||`)

L'opérateur `||` retourne `true` si au moins une des conditions est vraie.

```javascript
jour === "samedi" || jour === "dimanche";
```

### NON logique (`!`)

L'opérateur `!` inverse une valeur booléenne.

```javascript
let actif = true;

!actif;
```

Résultat :

```javascript
false
```

## Tableau récapitulatif

| Opérateur | Description |
|-----------|-------------|
| `=` | Affecte une valeur |
| `==` | Compare les valeurs uniquement |
| `===` | Compare la valeur et le type |
| `!=` | Vérifie une différence de valeur |
| `!==` | Vérifie une différence de valeur ou de type |
| `>` | Supérieur à |
| `<` | Inférieur à |
| `>=` | Supérieur ou égal à |
| `<=` | Inférieur ou égal à |
| `+` | Addition ou concaténation |
| `-` | Soustraction |
| `*` | Multiplication |
| `/` | Division |
| `%` | Reste d'une division (modulo) |
| `++` | Ajoute 1 |
| `--` | Retire 1 |
| `+=` | Addition puis affectation |
| `-=` | Soustraction puis affectation |
| `*=` | Multiplication puis affectation |
| `/=` | Division puis affectation |
| `&&` | ET logique |
| `||` | OU logique |
| `!` | NON logique |

## À retenir

- `=` affecte une valeur à une variable.
- `==` compare uniquement les valeurs.
- `===` compare la valeur et le type. Son utilisation est recommandée.
- `++` et `--` permettent d'ajouter ou de retirer `1`.
- Les opérateurs `+=`, `-=`, `*=`, `/=` sont des écritures simplifiées permettant de modifier directement une variable.
- Les opérateurs logiques permettent de combiner plusieurs conditions.