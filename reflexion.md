Reflexion – Phase 6
Structure actuelle du projet Git
Après toutes les opérations du TP, le projet contient plusieurs branches correspondant aux trois élèves : 
la branche de l’élève 1 (Cohen-Lenny)
ma branche personnelle (Im-Savannah)
la branche de l’élève 3 (branch/Willey-Arbaut)
la branche principale (master)

Des merges ont été effectués : 
L’élève 1 a effectué un merge sans fast-forward de ma branche.
J’ai réalisé un merge avec fast-forward de la branche de l’élève 3.
L’élève 3 a réalisé des rebase sur les branches des élèves 1 et 2.

Il y a également un commit de revert sur ma branche, correspondant à l'annulation du commit de création du fichier tp.md de l’élève 1.
L’historique contient donc : des commits individuels, des merges, un revert, et un rebase effectué par l’élève 3.

---

Différence entre git fetch et git pull
git fetch récupère toutes les mises à jour du dépôt distant sans modifier la branche locale.
Il met simplement à jour les références origin/....

git pull fait un git fetch suivi d’un git merge, ce qui modifie directement la branche locale.

Exemple :
Si je veux vérifier ce que mes coéquipiers ont pushé sans risquer un merge automatique, j'utilise git fetch.
Si je veux directement mettre ma branche à jour avec les dernières modifications du serveur, j’utilise git pull.

---

Différence entre git reset et git revert
git reset modifie l’historique local en se déplaçant à un commit précédent.
git revert, au contraire, crée un nouveau commit qui annule un commit passé, sans changer l’historique.

Situation où reset est risqué :
Si plusieurs personnes travaillent sur le même dépôt, utiliser git reset --hard peut réécrire l’historique partagé et casser le travail des autres.
Dans ce cas, il vaut toujours mieux utiliser git revert car il n’efface aucun commit, il annule seulement les changements.
