# GoodPractices
## Principes et bonnes pratiques

Dans le développement, nous adhérons aux bonnes pratiques et principes suivants pour garantir un code propre, maintenable et évolutif :


### YAGNI (You Ain't Gonna Need It)

Ce principe consiste à éviter d'ajouter des fonctionnalités ou du code en prévision de besoins futurs.
Nous nous concentrons uniquement sur les fonctionnalités et les exigences actuelles du projet pour éviter la complexité et le gaspillage de temps inutiles.


### DRY (Don't Repeat Yourself)

DRY est un principe fondamental de développement qui vise à réduire la répétition du code.
Nous nous efforçons de créer des composants et des fonctions réutilisables pour éviter de dupliquer des parties similaires du code dans différentes parties de l'application.


### KISS (Keep It Simple, Stupid)

Ce principe encourage à garder les choses simples et à éviter les solutions complexes ou inutiles.
Nous cherchons à rendre notre code clair et facile à comprendre pour les autres développeurs qui travaillent sur le projet.


## Git & GitHub

### Qu'est-ce que Git?

**Git** est un système de gestion de versions décentralisé qui permet à plusieurs personnes de travailler sur un même projet sans se gêner mutuellement. Chaque développeur travaille sur sa propre copie et peut fusionner ses modifications avec le reste du projet à sa convenance.

**Avantages de Git** :
- Suivi des modifications : chaque changement est associé à un "commit" avec un message descriptif.
- Gestion des branches : on peut créer des branches pour développer des fonctionnalités en parallèle.
- Résolution des conflits : Git offre des outils pour fusionner des modifications conflictuelles.

### Qu'est-ce que GitHub?

**GitHub** est une plateforme d'hébergement de code qui utilise Git pour le versionnement. Elle propose une interface web pour les dépôts Git, avec des fonctionnalités additionnelles :
- Gestion des bugs et demandes d'amélioration avec les "issues".
- Contribution à d'autres projets via les "pull requests".
- Outils pour l'intégration continue.

### Comment installer Git?

- **Windows** : [Téléchargez l'exécutable](https://git-scm.com/download/win) et suivez les étapes d'installation.
- **macOS** : Utilisez Homebrew (`brew install git`) ou [téléchargez l'exécutable](https://git-scm.com/download/mac).
- **Linux (Debian/Ubuntu)** : Dans le terminal, tapez `sudo apt-get install git`.

**Après l'installation**, configurez votre identité Git :
```bash
git config --global user.name "Votre nom"
git config --global user.email "votre.email@example.com"
```

---

## Routine & Conventions Github 

Nous privilégions le travail en **micro-features** offrant une meilleure organisation, une réduction des conflits et une amélioration de la qualité du code.

### Qu'est-ce que le travail en micro-features ?

Le principe est le suivant :

1. **Découpage du projet** : Division en petites fonctionnalités distinctes.
2. **Branches dédiées** : Une branche spécifique pour chaque micro-feature.
3. **Travail en équipe** : Chaque développeur travaille sur une micro-feature différente.
4. **Révisions et tests** : Avant d'intégrer une micro-feature, elle est soumise à une revue et des tests.
5. **Intégration continue** : Chaque micro-feature est intégrée et testée automatiquement avant d'être fusionnée.
6. **Flexibilité** : Facilité d'expérimentation et d'itération.

### Avant de créer une branche ou un commit

Toujours synchroniser votre copie locale avec la branche de développement :
```bash
git fetch
git pull
```

### Nommer branches et commits

Pour un nouveau sujet, créez une nouvelle branche :

```bash
git checkout -b feat/name-of-the-branch
```
Les noms sont en anglais, en minuscule, et le "type" peut varier (`feat`, `fix`, `refactor`, `test`).

Pour créer un commit :
```bash
git add <file-name>   # ou `git add .` pour tous les fichiers
git commit -m "feat(topic): description"
git push
```

**Liens utiles**:
- [git-commitizen](https://github.com/commitizen/cz-cli)
- [Documentation Git](http://git-scm.com/book/fr/v2)
- [Git Cheatsheet](https://ndpsoftware.com/git-cheatsheet.html)
