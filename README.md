# emn-cohorte2
Brief2

### Actions courantes avec Git et leurs explications :

#### 1. **Initialiser un dépôt Git local**  
   - **Commande** : `git init`  
   - **Explication** : Initialise un dépôt Git dans un répertoire local, créant ainsi un dossier `.git` pour le suivi des versions.

#### 2. **Configurer Git (nom, email, alias)**  
   - **Commande** :  
     - `git config --global user.name "Votre Nom"`  
     - `git config --global user.email "votre@email.com"`  
     - `git config --global alias.co checkout`  
   - **Explication** : Configure les informations d’utilisateur et des alias pour raccourcir certaines commandes.

#### 3. **Ajouter des fichiers au suivi (`git add`)**  
   - **Commande** : `git add <fichier>` ou `git add .`  
   - **Explication** : Ajoute les modifications d’un ou plusieurs fichiers à l’index pour le prochain commit.

#### 4. **Commiter des modifications (`git commit`)**  
   - **Commande** : `git commit -m "Message de commit"`  
   - **Explication** : Enregistre les modifications ajoutées dans l’historique Git avec un message descriptif.

#### 5. **Créer et basculer entre des branches (`git branch`, `git checkout`)**  
   - **Commande** :  
     - `git branch nom_de_branche` (création)  
     - `git checkout nom_de_branche` (changement)  
     - `git switch nom_de_branche` (alternative plus moderne)  
   - **Explication** : Permet de créer des branches pour travailler sur des versions parallèles du projet.

#### 6. **Fusionner des branches (`git merge`)**  
   - **Commande** : `git merge nom_de_branche`  
   - **Explication** : Fusionne une branche dans la branche courante.

#### 7. **Rebaser une branche (`git rebase`)**  
   - **Commande** : `git rebase nom_de_branche`  
   - **Explication** : Applique les commits d’une branche sur une autre de manière linéaire.

#### 8. **Résoudre des conflits de fusion**  
   - **Commande** : Modifier les fichiers conflictuels manuellement, puis  
     - `git add <fichier>`  
     - `git commit -m "Résolution de conflit"`  
   - **Explication** : Se produit lorsque deux branches ont des modifications incompatibles sur un même fichier.

#### 9. **Voir l’état du dépôt (`git status`)**  
   - **Commande** : `git status`  
   - **Explication** : Affiche l’état des fichiers suivis, modifiés et en attente de commit.

#### 10. **Voir l’historique des commits (`git log`)**  
   - **Commande** : `git log`  
   - **Explication** : Affiche l’historique des commits avec leurs détails (auteur, date, message, hash).

#### 11. **Voir les différences entre fichiers (`git diff`)**  
   - **Commande** :  
     - `git diff` (modifications non indexées)  
     - `git diff --staged` (modifications indexées)  
   - **Explication** : Permet de voir les différences entre les fichiers modifiés avant de les commiter.

#### 12. **Annuler des modifications (`git reset`, `git revert`)**  
   - **Commande** :  
     - `git reset HEAD~1` (annule le dernier commit sans supprimer les fichiers)  
     - `git reset --hard HEAD~1` (supprime complètement le dernier commit)  
     - `git revert <commit>` (crée un commit annulant un commit précédent)  
   - **Explication** : Permet d’annuler ou de revenir à un état précédent.

#### 14. **Supprimer un fichier suivi par Git (`git rm`)**  
   - **Commande** : `git rm <fichier>` puis `git commit -m "Suppression du fichier"`  
   - **Explication** : Supprime un fichier du suivi Git et du disque.

#### 15. **Supprimer une branche locale**  
   - **Commande** : `git branch -d nom_de_branche`  
   - **Explication** : Supprime une branche qui n’est plus nécessaire.

#### 16. **Travailler avec des tags (`git tag`)**  
   - **Commande** :  
     - `git tag -a v1.0 -m "Version 1.0"` (création d’un tag annoté)  
     - `git tag` (liste des tags)  
     - `git push origin v1.0` (envoi du tag vers le dépôt distant)  
   - **Explication** : Permet de marquer des versions importantes du projet.

#### 17. **Stasher des modifications en cours (`git stash`)**  
   - **Commande** :  
     - `git stash` (enregistre temporairement les modifications)  
     - `git stash pop` (récupère les modifications enregistrées)  
   - **Explication** : Met de côté des modifications sans les commiter.

#### 18. **Restaurer un état précédent (`git checkout --`, `git restore`)**  
   - **Commande** :  
     - `git checkout -- fichier` (ancienne méthode pour restaurer un fichier)  
     - `git restore fichier` (nouvelle méthode)  
   - **Explication** : Permet d’annuler les modifications locales sur un fichier suivi.

Ces actions couvrent les opérations essentielles pour gérer un projet de développement avec Git.
