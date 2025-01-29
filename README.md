# emn-cohorte2
Brief2

##  Travail sur un Repository Cloné**
Après avoir cloné un repository avec :

```sh
git clone <URL_du_repository>
```

### **Modification des fichiers**
- Ouvrez le projet dans un éditeur de code (Blocnote, VS Code, Sublime Text, etc.).
- Apportez vos modifications aux fichiers souhaités.

### **Vérifier l’état du dépôt**
Avant d'ajouter des fichiers au suivi de Git, vérifiez l’état du repository :

```sh
git status
```
Cela affiche les fichiers modifiés et les nouveaux fichiers non suivis.

### **Ajouter les fichiers au suivi de Git**
Ajoutez les fichiers modifiés au suivi :

```sh
git add <nom_du_fichier>  # Ajout d’un fichier spécifique
git add .  # Ajout de tous les fichiers modifiés
```

### **Enregistrer les modifications (commit)**
Une fois les fichiers ajoutés, enregistrez les modifications avec un message clair :

```sh
git commit -m "Ajout d'une nouvelle fonctionnalité"
```

### **Envoyer les modifications sur GitHub (push)**
Après le commit, envoyez vos changements sur le repository distant :

```sh
git push origin <nom_de_la_branche>
```

---

## **Gestion des Branches**
### **Création d’une nouvelle branche**
Une branche permet de travailler sur une fonctionnalité sans affecter la branche principale.

```sh
git branch <nom_de_la_branche>
```
ou directement créer et se positionner sur la branche :
```sh
git checkout -b <nom_de_la_branche>
```

### **Changer de branche**
Si vous voulez passer d'une branche à une autre :

```sh
git checkout <nom_de_la_branche>
```

### **Fusionner une branche (merge)**
Une fois le travail terminé, fusionnez la branche avec `main` (ou `master` selon le repo) :

1. Passez sur la branche principale :
   ```sh
   git checkout main
   ```
2. Fusionnez la branche : `<nom_de_la_branche>` sera merger dans main
   ```sh
   git merge <nom_de_la_branche>
   ```

### **Supprimer une branche**
Une fois fusionnée, supprimez la branche locale :

```sh
git branch -d <nom_de_la_branche>
```
Si la branche n'a pas encore été fusionnée et que vous voulez forcer la suppression :
```sh
git branch -D <nom_de_la_branche>
```
Supprimer la branche distante :
```sh
git push origin --delete <nom_de_la_branche>
```

---

## **Contribuer à un Projet Extérieur (Fork, Pull Request)**
Si vous souhaitez contribuer à un projet qui n'est pas le vôtre, voici les étapes :

### **Forker un projet**
1. Rendez-vous sur le repository GitHub.
2. Cliquez sur **"Fork"** (en haut à droite).
3. Un clone du repository est créé sur votre propre compte GitHub.

### **Cloner le fork sur votre machine**
Après le fork, clonez votre copie du projet :

```sh
git clone <URL_du_fork>
```

### **Ajouter une nouvelle branche pour vos modifications**
Cette commande crée et te positionne immédiatement sur la nouvelle branche
```sh
git checkout -b feature-nouvelle-fonctionnalite
```

### **Travailler sur les modifications et les pousser**
Après modification, ajoutez, committez et poussez les changements :

```sh
git add .
git commit -m "Ajout d'une nouvelle fonctionnalité"
git push origin feature-nouvelle-fonctionnalite
```

### **Créer une Pull Request (PR)**
1. Allez sur votre fork sur GitHub.
2. Cliquez sur **"New Pull Request"**.
3. Sélectionnez votre branche et ajoutez une description claire.
4. Soumettez la PR pour qu'elle soit examinée et fusionnée par les mainteneurs du projet.

### **Synchroniser votre fork avec l’original**
Si le repository d'origine a évolué, mettez à jour votre fork :

1. Ajoutez un remote vers l’original :
   ```sh
   git remote add upstream <URL_du_repository_original>
   ```
2. Récupérez les nouvelles modifications :
   ```sh
   git fetch upstream
   ```
3. Mettez à jour votre branche principale :
   ```sh
   git checkout main
   git merge upstream/main
   ```
4. Poussez les mises à jour vers votre fork :
   ```sh
   git push origin main
   ```

---

##  **Bonnes Pratiques Git**
✅ **Utiliser des messages de commit clairs et descriptifs.**  
✅ **Créer des branches pour chaque nouvelle fonctionnalité ou correction.**  
✅ **Pousser régulièrement pour éviter de perdre du travail.**  
✅ **Faire des pull requests détaillées et bien documentées.**  
✅ **Maintenir son fork à jour avec la branche principale du projet d’origine.**  
✅ **Éviter de commit des fichiers inutiles (ajoutez un `.gitignore` si nécessaire).**  




#### **Initialiser un dépôt Git local**  
```sh
git init
```  
   - **Explication** : Initialise un dépôt Git dans un répertoire local, créant ainsi un dossier `.git` pour le suivi des versions.

#### 2. **Configurer Git (nom, email, alias)**  
Configure les informations d’utilisateur et des alias pour raccourcir certaines commandes.   
```sh
git config --global user.name "Votre Nom"
git config --global user.email "votre@email.com"
git config --global alias.co checkout
```

#### **Fusionner des branches (`git merge`)**  
   - **Commande** : `git merge nom_de_branche`  
   - **Explication** : Fusionne une branche dans la branche courante.

#### **Rebaser une branche (`git rebase`)**  
   - **Commande** : `git rebase nom_de_branche`  
   - **Explication** : Applique les commits d’une branche sur une autre de manière linéaire.

#### **Résoudre des conflits de fusion**  
   - **Commande** : Modifier les fichiers conflictuels manuellement, puis  
     - `git add <fichier>`  
     - `git commit -m "Résolution de conflit"`  
   - **Explication** : Se produit lorsque deux branches ont des modifications incompatibles sur un même fichier.

#### **Voir l’état du dépôt (`git status`)**  
   - **Commande** : `git status`  
   - **Explication** : Affiche l’état des fichiers suivis, modifiés et en attente de commit.

#### **Voir l’historique des commits (`git log`)**  
   - **Commande** : `git log`  
   - **Explication** : Affiche l’historique des commits avec leurs détails (auteur, date, message, hash).

#### **Voir les différences entre fichiers (`git diff`)**  
   - **Commande** :  
     - `git diff` (modifications non indexées)  
     - `git diff --staged` (modifications indexées)  
   - **Explication** : Permet de voir les différences entre les fichiers modifiés avant de les commiter.

#### **Annuler des modifications (`git reset`, `git revert`)**  
   - **Commande** :  
     - `git reset HEAD~1` (annule le dernier commit sans supprimer les fichiers)  
     - `git reset --hard HEAD~1` (supprime complètement le dernier commit)  
     - `git revert <commit>` (crée un commit annulant un commit précédent)  
   - **Explication** : Permet d’annuler ou de revenir à un état précédent.

#### **Supprimer un fichier suivi par Git (`git rm`)**  
   - **Commande** : `git rm <fichier>` puis `git commit -m "Suppression du fichier"`  
   - **Explication** : Supprime un fichier du suivi Git et du disque.

#### **Supprimer une branche locale**  
   - **Commande** : `git branch -d nom_de_branche`  
   - **Explication** : Supprime une branche qui n’est plus nécessaire.

#### **Travailler avec des tags (`git tag`)**  
   - **Commande** :  
     - `git tag -a v1.0 -m "Version 1.0"` (création d’un tag annoté)  
     - `git tag` (liste des tags)  
     - `git push origin v1.0` (envoi du tag vers le dépôt distant)  
   - **Explication** : Permet de marquer des versions importantes du projet.

#### **Stasher des modifications en cours (`git stash`)**  
   - **Commande** :  
     - `git stash` (enregistre temporairement les modifications)  
     - `git stash pop` (récupère les modifications enregistrées)  
   - **Explication** : Met de côté des modifications sans les commiter.

#### **Restaurer un état précédent (`git checkout --`, `git restore`)**  
   ancienne méthode pour restaurer un fichier
   ```sh
   git checkout -- fichier
   ```
   nouvelle méthode
   ```sh
   git restore fichier
   ```
   - **Explication** : Permet d’annuler les modifications locales sur un fichier suivi.

Voici les différentes étapes pour travailler efficacement avec **Git et GitHub** après avoir cloné un repository, en passant par la gestion des branches, les bonnes pratiques, et la contribution à un projet extérieur.  

---



---

### **Conclusion**
Maîtriser Git et GitHub permet de travailler efficacement en équipe et de contribuer à des projets open source. En suivant ces étapes, vous serez capable de gérer des versions de code, de collaborer avec d'autres développeurs, et d'intégrer de nouvelles fonctionnalités dans des projets en toute fluidité. 🚀
