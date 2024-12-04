## Structure

```plaintext
src/
├── app/                # Dossier de l'application Next.js (pages et routes)
├── components/         # Composants UI réutilisables
├── containers/         # UI pour les sections de page
├── contexts/           # Gestion de l'état global
├── database/           # Configurations de la base de données
├── hooks/              # Hooks personnalisés
├── libs/               # Variables constantes et fonctions utilitaires
├── styles/             # Styles globaux et spécifiques aux composants
├── types/              # Définition des types TypeScript
```

## Git

### Préfixes de Commit

**`build`** :

- Utilisé pour les changements qui affectent le système de build ou les dépendances externes (par exemple, ajout/modification d'un outil de build, modification de `webpack`, etc.).
- **Exemple** : `build: mise à jour de la configuration de webpack`.

**`chore`** :

- Pour les tâches de maintenance qui ne modifient ni le code de production, ni les fonctionnalités (par exemple, mise à jour des dépendances, modification de la configuration).
- **Exemple** : `chore: mise à jour des dépendances npm`.

**`ci`** :

- Pour les changements liés à la configuration de l'intégration continue (CI), comme les fichiers de configuration pour des outils comme GitHub Actions, Travis CI, CircleCI, etc.
- **Exemple** : `ci: ajout de la configuration GitHub Actions`.

**`docs`** :

- Utilisé pour les changements qui affectent la documentation du projet (par exemple, mise à jour du README, ajout de commentaires dans le code).
- **Exemple** : `docs: mise à jour du README pour la configuration de l'environnement`.

**`feat`** :

- Pour l'ajout de nouvelles fonctionnalités ou améliorations majeures du produit.
- **Exemple** : `feat: ajout d'une fonctionnalité de recherche dans l'application`.

**`fix`** :

- Utilisé pour des corrections de bugs ou des modifications qui corrigent un comportement incorrect ou une erreur dans l'application.
- **Exemple** : `fix: correction du bug de chargement de la page`.

**`perf`** :

- Pour des modifications visant à améliorer les performances de l'application (par exemple, amélioration de la vitesse d'exécution, réduction de l'utilisation de la mémoire).
- **Exemple** : `perf: optimisation du rendu des pages pour de meilleures performances`.

**`refactor`** :

- Utilisé pour des modifications qui améliorent la structure interne du code sans changer son comportement (par exemple, refactorisation de fonctions, réorganisation de fichiers).
- **Exemple** : `refactor: refactorisation du code du module de paiement`.

**`revert`** :

- Pour revenir en arrière et annuler un commit précédent (par exemple, annuler une fonctionnalité ajoutée ou une modification qui a introduit des erreurs).
- **Exemple** : `revert: annulation de la modification du formulaire de connexion`.

**`style`** :

- Utilisé pour des modifications de style de code qui n'affectent pas le comportement du programme (par exemple, des corrections de formatage, des changements de noms de variables, l'alignement du code).
- **Exemple** : `style: correction de l'indentation et des espaces dans le fichier `index.js``.

**`test`** :

- Pour les changements liés aux tests, comme l'ajout de nouveaux tests ou la correction de tests existants.
- **Exemple** : `test: ajout de tests unitaires pour la fonction de tri`.

---

### Préfixes de Branches Git et Bonnes Pratiques de Workflow

### 1. **`feature/`** :

- Utilisé pour les branches de développement de nouvelles fonctionnalités.
- **Exemple** : `feature/ajout-recherche` ou `feature/nouvelle-interface-utilisateur`.

### 2. **`bugfix/`** :

- Utilisé pour les branches visant à corriger un bug ou un problème spécifique dans le code.
- **Exemple** : `bugfix/correction-connexion` ou `bugfix/erreur-affichage`.

### 3. **`hotfix/`** :

- Utilisé pour des corrections urgentes à apporter à la branche `main`, généralement en production.
- **Exemple** : `hotfix/correction-securite` ou `hotfix/bug-production`.

### 4. **`release/`** :

- Utilisé pour préparer une nouvelle version du produit. Cette branche permet de finaliser la mise en production, de corriger des bugs mineurs ou d'ajouter des dernières modifications avant la sortie de la version.
- **Exemple** : `release/v1.2.0` ou `release/v2.0.0`.

### 5. **`stage`** :

- C'est la branche principale de développement. Toutes les nouvelles fonctionnalités, correctifs et améliorations sont intégrés ici avant d'être fusionnés dans `main` pour la mise en production.

### 6. **`main`** :

- C'est la branche stable du projet, celle qui est déployée en production.
- Ne faites des commits dans `main` que pour des versions finales ou des corrections urgentes.

### 7. **`chore/`** :

- Utilisé pour les tâches de maintenance, comme les mises à jour de dépendances ou la configuration des outils.
- **Exemple** : `chore/mise-a-jour-dependances` ou `chore/ajout-configure-eslint`.

---

## Bonnes Pratiques pour les Workflows Git

- **Créer une branche avant de travailler** : Toujours créer une branche spécifique avant de commencer à travailler sur une nouvelle fonctionnalité ou une correction de bug. Ne travaillez pas directement dans `main` ou `stage`.

- **Nommer les branches de manière descriptive** : Utilisez des noms de branches explicites qui décrivent la tâche que vous effectuez (par exemple, `feature/ajout-paiement` ou `bugfix/correction-erreur-formulaire`).

- **Faire des commits fréquents** : Faites des commits réguliers pour chaque petite unité de travail achevée. Ne laissez pas trop de changements s'accumuler dans un seul commit.

- **Gardez les commits clairs et précis** : Rédigez des messages de commit explicites qui décrivent ce qui a été modifié et pourquoi.

- **Revue de code** : Toujours effectuer une revue de code avant de fusionner les branches. Assurez-vous que les autres membres de l'équipe ont vérifié votre code pour éviter les erreurs et améliorer la qualité du projet.
