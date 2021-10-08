# Le jeu du T-Rex

## Etape 3

Afin de tester rapidement notre environnement, nous allons intégrer directement le travail d'Armande. Cela nous permettra de tester React, et de lancer notre site internet en local. Ce sera une première base pour faire nos tests avec Heroku et le Dino.

Nous allons donc merger `feature/react` dans `master`. Mais avant tout nous devons tester le travail d'Armande.

```bash
    git checkout feature/react
    yarn # installe les dépendances
    yarn start # Pour tester le code d'Armande
    ctrl+C # pour arrêter le serveur webpack
```

Maintenant le merge: 

```bash
    git checkout master
    git merge feature/react
```

## Etape 4 

Nous pouvons à présent relancer le serveur webpack pour vérifier que notre site fonctionne toujours après le merge. 
Normalement il n'y a eu des conflits dans le readme, mais il ne devrait pas y avoir de bug.

```bash
    git checkout master # Ceci n'est pas nécessaire si vous êtes déjà sur master
    yarn start # Pour tester le code d'Armande
    ctrl+C # pour arrêter le serveur webpack
```

Continuons en allant voir le travail de Gustave `git checkout feature/heroku`.
