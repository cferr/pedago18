# Comprendre les processeurs... sans processeur

Je vais me baser sur le Little Man Computer : voir
https://fr.wikipedia.org/wiki/Little_man_computer

Ce processeur a un jeu d'instructions qui me semble plus pragmatique que le 
CARDIAC, avec plusieurs types de branchement dont des conditionnels. 

Le manuel du CARDIAC contient un certain nombre d'exemples pour ceux qui ne
sont pas déjà aguerris avec les processeurs, mais il contient 40 pages à lire
bien attentivement. En une heure ou deux, ça ne tient pas... et on ne peut
pas raisonnablement demander aux élèves de se lire 40 pages à la maison avant
de revenir le lendemain pour jouer au CARDIAC. Le LMC fonctionne sur le même
principe, donc demande pas mal de lecture.

Le but de l'opération, à mon sens, est que les élèves comprennent qu'un 
processeur est une petite puce qui avance pas à pas dans un programme, qui est
décomposé en petites instructions élementaires. On comprendra aussi 
l'interaction avec la mémoire et éventuellement les périphériques.

Un certain nombre de choses doivent être simplifiées pour ne pas avoir ce
problème. Je propose de :

 - supprimer le décodage des instructions, et les écrire en assembleur. On peut
   ainsi étendre le jeu d'instructions et ajouter une multiplication par
   exemple. 
 - ajouter une table de conversion entre valeurs numériques et caractères ASCII
   ou bien, mieux, permettre l'insertion de lettres dans la mémoire. On stocke
   indifféremment des caractères et des nombres dans la mémoire, autrement dit
   on type les valeurs en mémoire et on les représente de manière 
   human-friendly. 
 - utiliser une file de deux registres plutôt qu'un accumulateur unique. Ainsi
   on pourra avoir une boucle dont on incrémente l'indice sans stocker / 
   recharger celui-ci depuis la mémoire.
 - éventuellement ajouter des interruptions : un des élèves joue les 
   interrupteurs (souris par exemple) et écrit une valeur en mémoire de temps en
   temps. Le concept d'interruption peut être amusant à aborder car il explique
   comment l'évolution du programme peut changer en fonction de l'action de
   l'utilisateur, par exemple, sur la souris. Mais ce ne serait qu'un bonus.

J'envisage de reproduire ce processeur sous une forme papier, qui peut se
matérialiser soit par un carton à la Cardiac, soit par des tableaux représentant
la file de registres, les instructions (avec une petite gommette qu'on bouge 
pour faire le rôle du PC) et la mémoire. 

Petite anecdote : à l'EPFL, le cours d'archi avancée comprenait un DM dont le
but était de simuler un Itanium. On avait des tableaux pour les stations de
réservation, le réordonnanceur, on utilisait les prédicats... Et on avançait
en dupliquant la page en cours et en modifiant les états en lisant le gros pavé
expliquant l'ISA. Ce format me paraît intéressant mais risque d'être gourmand 
en papier.

