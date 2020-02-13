# Prise en main de l’interpréteur de commandes
1. which renvoie le chemin des fichiers qui es exécuté dans l'environnement courant
2. On chercher un terme  avec  */option*
3. on quitte le man avec *Q*
4. la section 6 du man  decris les jeux  *man 6 intro*

# Navigation dans l’arborescence des fichiers
1. * cd  /var/log
2. * cd ./ 
3. * cd ../ 
4. * cd - 
5. On n'a pas la permission  pour (cd root)  
6. sudo c'est poour etre en mode admin et pouvoir avoir la permission 
7. Pour crée un dossier *MKdir* un fichier (nano)
8. impossible car nous sommes pas dans le dossier 
9. la commande qui suprime un dossier (rmdir)
10. seule pour le dossier vide que la commande (rmdir) s'exécute
11. Supprimer un dossier et son contenue  (rm -r)

# Commandes importantes
1. Pour afficher la date  la commande  (date) , la commande *time* sert  a determine rle temps d'execution de certains commande
2. (ls) liste les fichiers present dans le fichier  et *la* liste en plus tout les fichiers (.) abréviation des *ls -a 
3. le programme ls se situe dans  (/usr/bin/ls) pour le trouver *which ls
4. (ll) commande liste les fichiers et leurs droits  ,non pas de rentrer de manuel car un allias
5. pour afficher les contenus du dossier /bin : (ls /bin)
6. (ls) permet de lister le contenue d'un dossier
7. la commande  (pwd)
8. la commande (echo 'yo' > plop) crée un ficher avec un contenu *yo* le taper 2fois permet de remplacer la ligne  déja existant
9. (echo 'yo' >> plop) crée le fichier avec comme contenu *yo* le taper 2fois ajoute dans le contenu de plop  un second *yo*dans le fichier 
10. la commande (file) permet de connaitre le type de fichier 
11. lorsqu'on crée un lien entre deux fichier quand on change le contenu de l'un l'autre change mais lorsqu'on supprime un e lien se rompe mais que le fichier supprimer disparait.
12.  la commande (ln -s titi tutu) crée un lien symbolique, meme  effet que la question 11 mais dans ce cas lorsqu'on supprime  titi , le  fichier n'est plus accessible (broken symbolic link )
13. les accourcis clavier permettent d’interrompre (ctrl +s)  et reprendre le défilement à l’écran (ctrl + Q)
14. les 5 premières lignes du fichier/var/log/syslog 
  * head /var/log/syslog -n 5
   * (sed -n "10,20 p" /var/log/syslog) les lignes 10 à 20
  * (tail /var/log/syslog -n 15 )  les 15 derniers
  15. la commande (dmesg | less )  affiche le kernel ring buffer avec moins d'info 
  16. passwd est un fichier de texte qui contient la liste des comptes sur le système, ainsi que des informations utiles sur ces comptes, comme l'identification de l'utilisateur, du groupe, le répertoire personnel, le shell, etc.  Il doit y avoir, dans le fichier des mots de passe, une ligne par utilisateur, avec le format suivant : account:passwd:UID:GID:GECOS:directory:shell 

  
