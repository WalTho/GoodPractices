# Guide des bonnes pratiques en développement

## Principes essentiels de développement

Afin de garantir un code propre, maintenable et évolutif, nous suivons les principes suivants :

### YAGNI (You Ain't Gonna Need It)
- **Définition** : Ne développez pas de fonctionnalités en anticipant des besoins futurs non confirmés.
- **Pratique** : Concentrez-vous sur les besoins immédiats. Cela évite la surcomplexité et le surdéveloppement.

### DRY (Don't Repeat Yourself)
- **Définition** : Chaque pièce de connaissance ou logique doit se trouver en un seul endroit.
- **Pratique** : Si vous trouvez des portions de code identiques ou similaires, considérez la création d'une fonction ou d'un composant réutilisable.

### KISS (Keep It Simple, Stupid)
- **Définition** : Les solutions simples sont souvent les meilleures.
- **Pratique** : Évitez d'over-engineer. Choisissez la solution la moins compliquée qui satisfait aux exigences.

### SOLID: Principes de conception orientée objet
- **Définition** : C'est un acronyme pour cinq principes qui aident à créer un code orienté objet facile à gérer et à maintenir.
    - **S** - Single Responsibility Principle (SRP) : Une classe ne devrait avoir qu'une seule raison de changer.
    - **O** - Open/Closed Principle : Les classes et les modules doivent être ouverts à l'extension mais fermés à la modification.
    - **L** - Liskov Substitution Principle : Les objets d'une classe mère doivent pouvoir être remplacés par des objets d'une classe fille sans affecter la correctitude du programme.
    - **I** - Interface Segregation Principle : Plusieurs interfaces spécifiques valent mieux qu'une seule interface générale.
    - **D** - Dependency Inversion Principle : Les modules de haut niveau ne devraient pas dépendre des modules de bas niveau. Les deux devraient dépendre des abstractions.

### Composition over Inheritance
- **Définition** : Préférer la composition à l'héritage lors de la construction de classes ou de modules pour maximiser la réutilisabilité et la flexibilité.
- **Pratique** : Plutôt que de créer des hiérarchies complexes basées sur l'héritage, assemblez des comportements plus simples en "composant" des objets.

### Law of Demeter (LoD) ou "Principle of Least Knowledge"
- **Définition** : Un objet ne devrait avoir qu'une connaissance limitée des autres objets avec lesquels il interagit.
- **Pratique** : Cela encourage la faible couplage entre les classes et favorise la modularité.

### Code comments
- **Définition** : Des commentaires pour clarifier le code, pas pour expliquer du "mauvais code".
- **Pratique** : Utilisez des commentaires pour documenter l'intention, les décisions importantes et les comportements complexes. Si vous ressentez le besoin de commenter pour expliquer ce que fait le code, envisagez de réviser votre code.

---

## Introduction à Git & GitHub

### Git : Votre outil de suivi de version

1. **Qu'est-ce que Git?** 
   - Git est comme un grand livre d'historique pour votre projet. Chaque changement apporté est une nouvelle page dans ce livre.
   
2. **Comment l'installer?**
   
   - **Windows**: 
     1. Ouvrez votre navigateur.
     2. Allez sur [ce lien pour télécharger Git](https://git-scm.com/download/win).
     3. Exécutez l'exécutable téléchargé et suivez les étapes.
     
   - **macOS**: 
     1. Ouvrez le terminal.
     2. Si vous avez Homebrew, tapez `brew install git`.
     3. Sinon, allez sur [ce lien pour télécharger Git](https://git-scm.com/download/mac) et suivez les étapes.
     
   - **Linux (Debian/Ubuntu)**:
     1. Ouvrez le terminal.
     2. Tapez `sudo apt-get install git` et appuyez sur Enter.

3. **Configuration initiale**:
   1. Ouvrez le terminal ou la ligne de commande.
   2. Tapez les commandes suivantes, en remplaçant par vos informations:
      ```bash
      git config --global user.name "Votre nom"
      git config --global user.email "votre.email@example.com"
      ```

### GitHub : Votre espace de collaboration

1. **Qu'est-ce que GitHub?**
   - C'est une plateforme qui héberge votre livre (projet) Git pour que d'autres puissent le voir, le lire et y contribuer.
   
2. **Premiers pas avec GitHub**:
   1. Ouvrez votre navigateur.
   2. Allez sur [GitHub](https://github.com/).
   3. Créez un compte ou connectez-vous.
   4. Une fois connecté, vous pouvez créer un nouveau dépôt ou "repository" pour héberger votre projet.

---

## Votre routine GitHub

### Travailler avec des micro-fonctionnalités

1. **Découpage du projet**:
   - Pensez à votre projet comme à un puzzle. Chaque pièce est une micro-fonctionnalité.

2. **Création d'une branche pour chaque pièce (micro-fonctionnalité)**:
   1. Assurez-vous que votre version est à jour:
      ```bash
      git fetch
      git pull
      ```
   2. Créez une nouvelle branche:
      ```bash
      git checkout -b feat/name-of-the-feature
      ```

3. **Travailler, vérifier, intégrer**:
   - Travaillez sur votre pièce.
   - Une fois terminé, vérifiez et testez-le.
   - Intégrez-le au puzzle principal (le projet).

### Comment nommer et sauvegarder vos changements

1. Pour enregistrer un changement:
   1. Ouvrez le terminal ou la ligne de commande dans votre projet.
   2. Ajoutez les fichiers modifiés:
      ```bash
      git add nom_du_fichier  # ou `git add .` pour ajouter tous les changements
      ```
   3. Sauvegardez le changement avec un message descriptif:
      ```bash
      git commit -m "type(sujet): description courte du changement"
      ```
   4. Envoyez vos changements à GitHub:
      ```bash
      git push
      ```

**Note**: Pour les types de messages (`type`), utilisez `feat` pour les nouvelles fonctionnalités, `fix` pour les corrections, `refactor` pour les modifications structurelles et `test` pour les tests.

**Liens utiles**:
- [git-commitizen pour standardiser vos messages](https://github.com/commitizen/cz-cli)
- [Documentation Git pour approfondir vos connaissances](http://git-scm.com/book/fr/v2)
- [Git Cheatsheet pour une référence rapide](https://ndpsoftware.com/git-cheatsheet.html)

---
