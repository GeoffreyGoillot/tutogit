# Le jeu du T-Rex

## Etape 1

Bienvenue dans ce TP où vous apprendrez à manipuler Git.  
Vous pouvez effectuer ce TP à l'aide du terminal ou avec une interface graphique comme GitKraken.

Pour commencer `forker le répo sur votre espace Gitlab`

Ensuite vous pouvez ensuite récupérer le projet en local en faisant un `clone` de votre repo :  
Ouvrez votre terminal dans le dossier de votre choix et tapez les commandes suivantes :

```bash
    git clone <url> dino-game
    cd dino-game/
```

Vous aurez besoin de : 
* node, npm : https://nodejs.org/fr/download/
* yarn : `npm install --global yarn`

## Etape 2

Vous avez maintenant tous les outils pour commencer le TP. Nous allons simuler une situation où 3 très bons développeurs ont travaillés en même temps sur le projet de Dinosaure. 

1. Gustave travaille sur l'hébergement (avec Heroku),
2. Armande travaille sur l'intégration de React dans le projet,
3. Dominique est excellent.e avec React et a déjà commencé.e à intégrer le T-Rex depuis Google.

Chacun à fait sa propre branche depuis le premier commit de master (qui contient entre autre ce fichier `readme.md`).  
Elles sont nommées dans le même ordre, comme ceci:

1. `feature/heroku`
2. `feature/react`
3. `feature/dino`

Vous pouvez choisir de changer de branche pour voir l'état d'avancement de chacun, en tapant ligne par ligne (ne faite pas de copier/coller de l'ensemble!) :  
Attention, le readme va changer, vous pourrez revenir dessus en faisant `git checkout master`

```bash
    git checkout feature/heroku
    git checkout feature/react
    git checkout feature/dino
    git checkout master
```

Après chaque ligne tapée, vous pouvez voir l'arboresence de vos fichiers évoluer. Vous ne devez rencontrer aucun problème pour changer de branche. Si c'est le cas c'est que vous avez déjà modifié quelque chose. 

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
