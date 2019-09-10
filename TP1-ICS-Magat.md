# Victor Magat - TP1

## Manuel

1. **which** va récupérer le chemin des fichiers exécutables, à l'aide de la variable **path**, dont les arguments correspondent à ceux donnés dans la commande.
2. Il suffit d'écrire **/option**
3. En pressant la touche **q**
4. A l'aide de la commande `man 6 intro` il est possible d'afficher la première page de la section 6. Elle présente les jeux et petits programmes drôles du système.

## Navigation dans l’arborescence des fichiers

1. `cd /var/log`
2. `cd ..`
3. `cd`
4. `cd -`
5. `cd /root` Nous n'avons pas la permission
6. `sudo cd /root` La commande **cd** n'est pas trouvé car **sudo** exécute seulement des programmes et **cd** est une commande interprété
7. Il faut créer l'arborescence grâce à **touch** pour les fichiers et **mkdir** pour les dossiers
8. Impossible de supprimer Dossier1 avec **rm** car c'est un dossier
9. La commande pour supprimer un fichier est `rmdir Dossier1`
10. Impossible car Dossier2 n'est pas vide
11. Il faut exécuter `rm -r Dossier2`

## Commandes importantes

1. **date**. La commande **time** sert à afficher différentes informations sur les ressources utilisées de la commande exécutée.
2. Les fichiers commençant par un point sont des fichiers cachés
3. La commande **ls** se trouve dans `/usr/bin/ls`. On le sait grâce à la commande **which**
4. Elle exécute la commande `ls -alF` grâce à l'alias.
5. Il faut exécuter `ls /bin`
6. Elle liste les fichiers et répertoires présents dans le chemin spécifié, si il n'y en a pas dans le chemin courant.
7. **pwd** permet d'afficher le chemin du dossier courant
8. Elle écrit dans le fichier **plop** le texte **yo** en remplaçant son contenu.
9. Elle écrit à la suite du fichier **plop** le texte **yo**.
10. Elle affiche des informations sur le contenu et le type de fichier.
11. Cela modifie aussi le fichier **titi**. Cela n'a pas d'impact pour le fichier **titi**.
12. Le fichier **titi** modifie aussi le fichier **tutu** et inversement. Si l'on supprime le fichier **titi**, le fichier **tutu** sera également supprimé.
13. Le raccourci `Ctrl + c` permet d'interrompre le processus.
14. - `head -5 /var/log/syslog`
    - `tail -n 5 /var/log/syslog`
    - `head -n 20 /var/log/syslog | tail -n 11`
15. **dmesg** affiche les messages du noyau, grâce à **less**, on peut se balader dans ces derniers, ligne après ligne.
16. `/etc/passwd` contient des informations concernant les utilisateurs
17. `sort -r /etc/passwd | cut -d : -f 1` permet d'afficher la première colonne triée par ordre alphabétique inverse
18. `grep "/bin/bash" /etc/passwd | wc -l` permet de récupérer le nombre d'utilisateurs
19. `apropos conversion | wc -l` permet d'avoir le nombre de pages de manuel comportant le mot **conversion**
20. `find -name passwd` après s'être placé dans la racine permet de lister tous les fichiers contenant la chaîne **passwd**
21. `find -name passwd >~/list_passwd_files.txt 2>/dev/null` permet de lister les résultats trouvés dans le fichier **list_passwd_files.txt** et d'écrire les erreurs dans le fichier **/dev/null**
22. `grep ll .bashrc` permet de trouver où est défini l'alias **ll**
23. Le fichier **history.log** se trouve à cet endroit `/var/log/apt/history.log`
24. **locate** utilise une base de données indexées listant tous les répertoires dans `/var/lib/mlocate/mlocate.dba`. Le fichier `/etc/cron.daily/mlocate` lance l'indexation chaque jour, c'est pour ça que notre fichier tout juste créé ne peut pas être localisé grâce à la commande.
