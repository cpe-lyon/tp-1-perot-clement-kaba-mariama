# Prise en main de l’interpréteur de commandes
1. which renvoie le chemin des fichiers qui est exécuté dans l'environnement courant.
2. On chercher un terme  avec  */option*
3. On quitte le man avec *Q*
4. La section 6 du man  decris les jeux  *man 6 intro*

# Navigation dans l’arborescence des fichiers
1. cd  /var/log
2. cd ./ 
3. cd ../ 
4. cd - 
5. On n'a pas la permission pour (cd root)  
6. sudo c'est poour etre en mode administrateur et pouvoir avoir certaine permission.
7. Pour crée un dossier *MKdir* un fichier (nano)
8. Impossible car nous sommes pas dans le dossier 
9. La commande qui supprime un dossier (rmdir)
10. La commande ne s'éxecute que sur les dossiers vides (rmdir) 
11. Supprimer un dossier et son contenue  (rm -r)

# Commandes importantes
1. Pour afficher l'heure on peut utiliser la commande (date) qui affiche toutes les informations du jour et un cut pour ne laisser que le temps, la commande *time* sert à determiner le temps d'execution de certaines commande, on l'utilise dans des script par exemple pour ovtenir son temps d'execution.
2. (ls) liste les fichiers present dans le fichier  et (la) liste en plus tout les fichiers (.) et cachés, abréviation des *ls -a 
3. Le programme ls se situe dans (/usr/bin/ls) pour le trouver *which ls
4. (ll) liste les fichiers et leurs droits,il n'y a pas d'entrer de manuel car c'est un allias.
5. Pour afficher les contenus du dossier /bin : (ls /bin)
6. (ls) permet de lister le contenue d'un dossier
7. la commande (pwd)
8. la commande (echo 'yo' > plop) crée un ficher avec un contenu *yo* , le taper 2 fois permet de remplacer la ligne  déja existant
9. (echo 'yo' >> plop) crée le fichier avec comme contenu *yo* le taper 2 fois ajoute dans le contenu de plop  un second *yo* dans le fichier.
10. La commande (file) permet de connaitre le type de l'objet passer en argument.
11. Lorsqu'on crée un lien entre deux fichier, quand on change le contenu de l'un l'autre change mais lorsque l'on supprime un fichier le lien est rompu et l'autre fichier devient simplement une copie de l'autre.
12. La commande (ln -s titi tutu) crée un lien symbolique, meme  effet que la question 11 mais dans ce cas lorsqu'on supprime  titi , le  fichier n'est plus accessible (broken symbolic link).
13. les accourcis clavier permettent d’interrompre (ctrl +s) et reprendre le défilement à l’écran (ctrl + Q).
14. les 5 premières lignes du fichier/var/log/syslog 
  * head /var/log/syslog -n 5
  * (sed -n "10,20 p" /var/log/syslog) les lignes 10 à 20
  * (tail /var/log/syslog -n 15 ) les 15 derniers
 15. la commande (dmesg | less ) affiche le kernel ring buffer avec moins d'informations.
 16. passwd est un fichier de texte qui contient la liste des comptes sur le système, ainsi que des informations utiles sur ces comptes, comme l'identification de l'utilisateur, du groupe, le répertoire personnel, le shell, etc. Il doit y avoir, dans le fichier des mots de passe, une ligne par utilisateur, avec le format suivant : * account:passwd:UID:GID:GECOS:directory:shell 
17. Aﬀichez seulement la première colonne triée par ordre alphabétique inverse
*  cat /etc/passwd|cut d: -f1  | sort -r
18. la commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine
  * cat /etc/passwd | awk -F: '{print $ 1}'
19. Combien de pages de manuel comportent le mot-cléconversiondans leur description
  * man -k conservation | wc -l 
20. la commande (find), recherchez tous les fichiers se nommantpasswdprésents sur la machine
  * sudo find -name passwd |wc -l
21. find -name passwd |wc -l  1> ~/list_passwd_files.txt 2> /dev/null
22. Il se situe dans ce fichier .bashrc
23.
24. Non il n'apparait pas car locate se base sur une base de données qu'il faut synchroniser pour pouvoir voir le fichier qui vient d'être créé.

# Exercice 4. Personnalisation du shell
