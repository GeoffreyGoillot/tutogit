# Le jeu du T-Rex


## Etape 8

Tout est prêt pour fonctionner, il ne reste plus qu'à intégrer le code de Dominique. 

* Vous pouvez tout tester en local sur la branche de dominique à l'aide d'un rebase avant de merger
* Vous pouvez merger en local directement sur master et tester après.

Méthode avec le rebase:

```bash
    git checkout feature/dino
    git rebase master
```

Méthode avec le merge:

```bash
    git checkout master
    git merge feature/dino
```

Vous voilà prêt pour tester, vous pouvez faire au choix:

* `git push heroku feature/dino:master` ou `git push heroku master` selon que vous aillez fait un `rebase` ou un `merge` pour tester en ligne.
* `yarn start` pour tester en local.

## Etape 9 

1. Mergez dans `master` si ce n'est pas fait à l'étape 6.
2. Nous allons récupérer un commit qui nous intéresse et qui contient un message pour finir le TP : 

```bash
    git cherry-pick f1b63cc
```

Cette commande permet de récupérer un ou plusieurs commits de n'importe quelle branche et de les appliquer dans l'ordre à votre branche courante.
