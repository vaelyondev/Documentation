# Installation de Git

## Télécharger Git

### Windows

Télécharger Git depuis le site officiel :

https://git-scm.com/download/win

Lancer l'installateur puis conserver les options par défaut.

---

## Vérifier l'installation

Ouvrir un terminal (Invite de commandes, PowerShell ou terminal VS Code) puis exécuter :

```bash
git --version
```

Exemple de résultat :

```bash
git version 2.50.1.windows.1
```

Si une version s'affiche, Git est correctement installé.

---

# Configuration de Git

Après l'installation, il est recommandé de configurer son identité Git.

## Configuration globale

La configuration globale est utilisée automatiquement dans tous les dépôts Git du poste.

Définir le nom d'utilisateur :

```bash
git config --global user.name "Votre Nom"
```

Définir l'adresse e-mail :

```bash
git config --global user.email "votre.email@example.com"
```

Vérifier la configuration :

```bash
git config --global --list
```

Exemple :

```bash
user.name=Votre Nom
user.email=votre.email@example.com
```

---

## Emplacement de la configuration globale

Sous Windows, les informations sont enregistrées dans le fichier :

```text
C:\Users\NomUtilisateur\.gitconfig
```

---

## Configuration locale

Une configuration locale s'applique uniquement au dépôt Git dans lequel elle est définie.

Depuis le dossier du projet :

```bash
git config user.name "Nom Projet"
git config user.email "projet@example.com"
```

Vérifier la configuration du dépôt :

```bash
git config --list
```

---

## Priorité des configurations

Git applique les configurations dans l'ordre suivant :

1. Configuration locale
2. Configuration globale
3. Configuration système

Si une valeur existe localement, elle remplace la valeur définie globalement.

---

# Connexion à GitHub

Git peut communiquer avec GitHub de deux façons :

- HTTPS
- SSH

---

# Créer un dépôt Git à partir d'un dossier local

## Méthode HTTPS

## 1. Créer le dépôt sur GitHub

1. Ouvrir GitHub
2. Cliquer sur **New Repository**
3. Donner un nom au dépôt
4. Cliquer sur **Create Repository**
5. Copier l'URL HTTPS du dépôt

Exemple :

```text
https://github.com/utilisateur/mon-projet.git
```

## 2. Ouvrir un terminal dans le dossier du projet

```bash
cd chemin/vers/mon-projet
```

## 3. Initialiser Git

```bash
git init
```

## 4. Associer le dépôt GitHub

```bash
git remote add origin https://github.com/utilisateur/mon-projet.git
```

Vérifier :

```bash
git remote -v
```

## 5. Ajouter les fichiers

```bash
git add .
```

## 6. Créer le premier commit

```bash
git commit -m "premier-commit"
```

## 7. Envoyer le projet sur GitHub

```bash
git push -u origin master
```

Ou si le dépôt utilise `main` :

```bash
git push -u origin main
```

## Workflow quotidien

```bash
git add .
git commit -m "description des modifications"
git push
```

Avec HTTPS, GitHub demandera une authentification lors des premières opérations de push.

---

## Méthode SSH

La méthode SSH permet de ne plus avoir à s'authentifier manuellement à chaque utilisation.

### Générer une clé SSH

Ouvrir Git Bash puis exécuter :

```bash
ssh-keygen -t ed25519 -C "votre.email@example.com"
```

Appuyer sur Entrée pour accepter les emplacements par défaut.

Les fichiers suivants seront créés :

```text
id_ed25519
id_ed25519.pub
```

---

### Afficher la clé publique

Dans Git Bash :

```bash
cat ~/.ssh/id_ed25519.pub
```

Copier l'intégralité du contenu affiché.

---

### Ajouter la clé dans GitHub

1. Ouvrir GitHub
2. Cliquer sur votre photo de profil
3. Settings
4. SSH and GPG Keys
5. New SSH Key
6. Coller la clé publique
7. Valider

---

### Tester la connexion

```bash
ssh -T git@github.com
```

Exemple de résultat :

```text
Hi utilisateur! You've successfully authenticated.
```

---

### Utiliser l'URL SSH du dépôt

Depuis GitHub, cliquer sur **Code** puis sélectionner **SSH**.

Exemple :

```text
git@github.com:utilisateur/mon-projet.git
```

Associer le dépôt local :

```bash
git remote add origin git@github.com:utilisateur/mon-projet.git
```

Vérifier :

```bash
git remote -v
```

---

## Vérifier l'URL du dépôt distant

```bash
git remote -v
```

---

## Modifier l'URL d'un dépôt existant

Passer de HTTPS à SSH :

```bash
git remote set-url origin git@github.com:utilisateur/mon-projet.git
```

Passer de SSH à HTTPS :

```bash
git remote set-url origin https://github.com/utilisateur/mon-projet.git
```

Vérifier :

```bash
git remote -v
```

---

# Vérifier une valeur spécifique

Afficher le nom configuré :

```bash
git config user.name
```

Afficher l'adresse e-mail configurée :

```bash
git config user.email
```

Afficher le nom configuré globalement :

```bash
git config --global user.name
```

Afficher l'adresse e-mail configurée globalement :

```bash
git config --global user.email
```

---

## Modifier une configuration existante

Pour modifier une valeur, il suffit de relancer la commande avec la nouvelle information :

```bash
git config --global user.name "Nouveau Nom"
```

```bash
git config --global user.email "nouvelle.adresse@example.com"
```

---

## Supprimer une configuration

Supprimer le nom d'utilisateur global :

```bash
git config --global --unset user.name
```

Supprimer l'adresse e-mail globale :

```bash
git config --global --unset user.email
```

---

# Résumé

Installation :

```bash
git --version
```

Configuration globale :

```bash
git config --global user.name "Votre Nom"
git config --global user.email "votre.email@example.com"
```

Connexion HTTPS :

```bash
git remote add origin https://github.com/utilisateur/mon-projet.git
```

Connexion SSH :

```bash
ssh-keygen -t ed25519 -C "votre.email@example.com"
git remote add origin git@github.com:utilisateur/mon-projet.git
```

Vérification :

```bash
git remote -v
```