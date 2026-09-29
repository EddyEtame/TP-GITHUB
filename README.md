# Rendu de Eddy Etame Etame

Une capture par étape, dans l'ordre. Terminal entier non rogné, invite visible.
Afficher l'historique en graphe quand c'est pertinent.

## Niveau 1
1. Configuration Git

![Configuration Git](captures/01-configuration.png)

2. Branche de travail

![Branche de travail](captures/02-branche.png)

3. Historique des commits

![Historique des commits](captures/03-historique.png)

4. Pull Request

![Push de la branche](captures/04a-push.png)

![Pull Request #1](captures/04-pull-request.png)

5. Revue croisée

![Revue croisée : ma PR sur le dépôt du binôme](captures/05-revue-croisee.png)

## Niveau 2
6. Secret retiré du suivi

![Secret retiré du suivi](captures/06-secret.png)

7. Conflit résolu (marqueurs avant, graphe après)

![Marqueurs de conflit](captures/07a-conflit-marqueurs.png)

![Graphe après résolution](captures/07b-conflit-graphe.png)

8. Revert du bandeau promo

![Revert du bandeau promo](captures/08-revert.png)

9. Issue fermée par une Pull Request

![Issue fermée par la PR](captures/09-issue-fermee.png)

10. Protection de main et CI au vert

![Push direct sur main refusé](captures/10a-push-refuse.png)

![Règle de protection de main](captures/10c-regle-main.png)

![CI au vert](captures/10e-ci-verte.png)

## Cible mobile
11. Commit distant récupéré et conflit résolu

![Commits du dépôt d'origine récupérés : conflit](captures/11a-upstream-conflit.png)

![Conflit résolu, commits intégrés au graphe](captures/11b-upstream-resolu.png)

Même manipulation avec un commit fait depuis GitHub en vue téléphone :

![Commit distant vu sur mobile](captures/11a-commit-distant-mobile.png)

![Pull et conflit](captures/11b-pull-conflit.png)

![Conflit résolu et poussé](captures/11c-conflit-resolu.png)

## Bonus
12. Petite feature : page 404 personnalisée, sur une branche partie du dépôt d'origine

![Branche du bonus et ses deux commits](captures/12a-bonus-branche.png)

13. Flux complet : Pull Request sur mon fork, CI au vert

![Pull Request du bonus](captures/12b-bonus-pr-fork.png)

14. Pull Request vers le dépôt d'origine

![Pull Request vers tristan-bsb/TP-GITHUB](captures/14-pr-depot-origine.png)

## Trois commits annotés
1. `f0b8a4c` : `git rm --cached` sort `config/secrets.env` du suivi sans le supprimer du disque. `.gitignore` ignore désormais `*.env` (sauf `*.env.example`) et un modèle vide indique les variables à remplir. Le mot de passe reste lisible dans l'historique (`ff28a3f`) : en situation réelle, il faut le changer.
2. `fbbea83` : commit de merge qui résout le conflit entre `feature/titre` et `feature/couleurs`. Les deux branches modifiaient la même ligne `<h1>` ; j'ai gardé les deux intentions : `<h1 class="hero">Bienvenue sur notre site</h1>`.
3. `e24aba7` : `git revert` de `a35a690`. Un nouveau commit annule le bandeau promo sans réécrire l'historique de `main`, ce qui reste sûr sur une branche partagée, contrairement à `git reset`.

#By King_E✨
