1. **Expliquez, en quelques phrases, la structure actuelle du projet Git après toutes les opérations (branches, merges, commits).**
    - Vous pouvez illustrer avec `git log --graph`.
    On as crée chaqu'un une branch avec notre nom et moi j'ai crée une autre branch avec un head détaché nommé detached.
    il y a eu une erreur de conflit lors du merge avec la branch Im-Savannah aprés une modiff du fichier et un add puis un commit tout est rentré dans l'ordre.
|\  Merge: 3846527 97cc768
| | Author: Azbot-git <l.cohen@myskolae.fr>
| | Date:   Thu Nov 13 16:26:21 2025 +0100
| |
| |     feat/<Cohen-Lenny>:<Modification du fichier aprés le merge avec la branch Im-Savannah aprés le confit du au meme nom de fichier conservation des deux texte (une fusion)>
| |
| * commit 97cc7688133620eb09d66ae2d231102132e15533
| | Author: sav94paris <im.savannah.pro@gmail.com>
| | Date:   Thu Nov 13 15:49:53 2025 +0100
| |
| |     ajout de mon ficher tp.md(sav)
| |
* | commit 3846527f9ca80d41ed57c1adf3ac219420cf19ff
|/  Author: Azbot-git <l.cohen@myskolae.fr>
|   Date:   Thu Nov 13 15:54:19 2025 +0100
|
|       feat/<Lenny-Cohen>: <création et ajout du fichier tp.md>
|
* commit 58b17f6963231234186910ca7cde1dcf772ed3cc (master)
| Author: Sarah Schlegel <sschlegel@myges.fr>
| Date:   Wed Nov 12 22:01:27 2025 +0100
|
|     Instructions TP Final
|
*   commit 767f380a5bb96234debe23e6eb9cc6e3ccda2e43
|\  Merge: a8be53b e2dd662
| | Author: Sarah Schlegel <sschlegel@myges.fr>
| | Date:   Wed May 25 18:39:15 2022 +0200
| |
| |     Merge pull request #1 from SarahSch19/develop
| |
| |     Develop
| |
| * commit e2dd662105fc79019d30214aafda841ba5d612d8
| | Author: Sarah <sschlegel@myges.fr>
| | Date:   Wed Oct 27 03:54:18 2021 +0900
| |
| |     init empty grid
| |
| * commit 6640250a07f2a8bdd4546ac8ef730dcd539f77f5
| | Author: Sarah <sschlegel@myges.fr>
| | Date:   Wed Oct 27 03:49:07 2021 +0900
| |
| |     next round done
| |
| * commit 8d0152e8af5ac897bce88ac64927e026eea6659a
| | Author: Sarah <sschlegel@myges.fr>
| | Date:   Wed Oct 27 03:00:50 2021 +0900
| |
| |     comment previous code
| |
| * commit 912ff4b94c56d36126c294bd2560830914f753f1
| | Author: Sarah <sschlegel@myges.fr>
| | Date:   Tue Oct 19 04:53:00 2021 +0900
| |
| |     comments for 19.10.2021
| |
| * commit 36daa99b64747d67a164d634fd775353ab176ae1
| | Author: Sarah <sschlegel@myges.fr>
| | Date:   Tue Oct 19 04:42:18 2021 +0900
| |
| |     19/10/2021 grid and cells setup
| |
| * commit c6b95deaf1916b5a71f51ebd06b1f558158ee379
| | Author: Sarah <sschlegel@myges.fr>
| | Date:   Tue Oct 19 02:28:21 2021 +0900
| |
| |     develop setup
| |
| * commit 23f5d1dd678001b6039d09dfc8622e03eeed3ee0
|/  Author: Sarah <sschlegel@myges.fr>
|   Date:   Mon Oct 18 18:33:52 2021 +0900
|
|       update gitignore
|
* commit a8be53b1ef762a800bffd9124949a32acd9479a2
  Author: SarahSch19 <grepo.sarah19@gmail.com>
  Date:   Mon Oct 18 16:14:54 2021 +0900

      Initial commit



2. **Quelle est la différence entre `git fetch` et `git pull` ?**
    - git fetch récupéré toute les mise a jours du dépot distant san modifier la branche local.
    - git pull permet de récupéré fair un git fetch  suivie d'uin git merge.
3. **Expliquez la différence entre `git reset` et `git revert`.**
git reset modifie l’historique local en se déplaçant à un commit précédent.
git revert, au contraire, crée un nouveau commit qui annule un commit passé, sans changer l’historique.

Si plusieurs personnes travaillent sur le même dépôt, utiliser git reset --hard peut réécrire l’historique partagé et casser le travail des autres.
Dans ce cas, il vaut toujours mieux utiliser git revert car il n’efface aucun commit, il annule seulement les changements.