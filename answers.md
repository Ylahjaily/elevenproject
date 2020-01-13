1/ Créer en ligne de commande un nouveau projet Symfony portant le nom“elevenproject”.
composer create-project symfony/website-skeleton elevenproject

2/ Créer un repository public depuis Github portant le nom “eleven”.
	A partir de ma page GitHub : 
	1.	Cliquer sur New.
	2.	Donner le nom “eleven” au repository.
	3. 	Cocher la case « Public »
	4.	Créer le repository

 3/ Générer une clé SSH pour votre utilisateur linux (sans pass phrase).
	1.	Sur le terminal => ssh-keygen - t rsa -b 4096  -C « y.lahjaily@ecole.ipssi.net »
	2.	Sur le terminal => ssh add < ~/.ssh/id_rsa.pub

4/ Ajouter la clé publique correspondant sur votre compte Github, pour pouvoir pousser sur github sans avoir à saisir l’utilisateur et le mot de passe à chaque fois.
	1.	Copier la clé générée : pbcopy < ~/.ssh/id_rsa.pub.
	2.	4. Dans gitHub , aller dans settings > SSH and GPG keys et faites ajouter une clé.
  
5/ Commiter et pusher le projet sur le repository distant avec le message “Project initialization” sur master.

	1.	git add -p
	2.	git commit -m « Project initialization »
	3.	git remote add origin  https://github.com/Ylahjaily/elevenproject.git
	4.	git push –d origin master

6/ Tirer une nouvelle branche depuis master que vous appellerez “EB-eleven-branch”
	•	git checkout -b  “EB-eleven-branch”

7/ Aller dans le dossier “elevenproject/public”
	•	cd elevenproject/public

8/ Exporter les 10 premières lignes du fichier “index.php” dans un fichier “extract-file.txt”en ligne de commande
	•	head -n 10 index.php >> extract-file.txt  
	. 	On peut aussi le faire avec :
		=>  sed -n -e '1,10p' index.php > extract-file.txt


9/ Afficher dans le terminal le contenu du fichier créé
	•	 cat extract-file.txt

10/ Remonter d’un niveau depuis le dossier courant
	•	cd ..

11/ Créer un dossier “elevenlog”
	•	mkdir elevenog

12/ Copier le fichier “extract-file.txt” dans le dossier précédemment créé.
- 	cp /Users/citizen99xyz/workspace/elevenproject/public/extract-file.txt /Users/citizen99xyz/workspace/elevenproject/elevenlog   
  (chemin absolu)

13/ Déplacer le dossier “elevenlog” dans “app/templates”
	•	mv /Users/citizen99xyz/workspace/elevenproject/template/extract-file.txt /Users/citizen99xyz/workspace/elevenproject/elevenlog /Users/citizen99xyz/workspace/elevenproject/template/extract-file.txt /Users/citizen99xyz/workspace/elevenproject/template 
 (chemin absolu)

14/Supprimer le fichier “extract-file.txt” se trouvant dans “public”
	•	rm extract-file.txt

15/ Commiter les modifications apportées dans le dossier “app/templates” et pusher sur github
	1.	git add . 
	2.	git commit -m “moove elevenlog”;
	3.	git push origin “EB-eleven-branch”

16/ Créer une Pull Request sur Github pour merger vers master
	1. Sur Github > Aller dans le repository Elevenproject > Cliquer sur Pull Requests > New Pull Request > sélectionner Master en branche de base et EB-eleven-branch embranche à comparer

17/ Revenir sur la branche master du projet
	•	git checkout master

18/ Créer le ficher “ELEVEN.md” à la racine du projet
	•	touch eleven.md

19/ L’ouvrir avec vim, ajouter la ligne “ELEVEN DT - TEST” en tête de fichier

	1.	vim eleven.md => ouverture du fichier dans l’éditeur vim.
	2.	i => passage au mode insertion.
	3.	ajouter la ligne “ELEVEN DT - TEST” en tête de fichier
	4.	echap => retour au mode interactif.
	5.	 :wq => enregistre les modification du fichier et quitte vim.

20/ Commiter le fichier sur master et pusher sur github
	1.	git add -p
	2.	git commit -m « added text to Eleven.md »
	3.	git pull https://github.com/Ylahjaily/elevenproject.git master
	4.	git push origin master

21/ Créer une nouvelle branche: “EB-eleven-other-branch” depuis master
	•	git checkout -b EB-eleven-other-branch

22/ Ouvrir le fichier “ELEVEN.md” avec vim, modifier la première ligne en “ELEVEN DT -BRANCH”.
	1.	Vim eleven.md 
	2.	i =>passage au mode insertion
	3.	remplacer la ligne “ELEVEN DT - TEST” en tête de fichier par « ELEVEN DT - BRANCH »
	4.	echap => retour au mode interactif 
	5.	 :wq => enregistre les modification du fichier et quitte vim

23/ Commiter les informations et pusher sur github
	1.	git add -p
	2.	git commit -m « added text to Eleven.md »
	3.	git push origin EB-eleven-other-branch

24/ Revenir sur la branche master.
	•	Git checkout master

25/ Ouvrir le fichier “ELEVEN.md” avec vim, modifier la première ligne en “ELEVEN DT -MASTER”
	1.	Vim eleven.md 
	2.	i =>passage au mode insertion
	3.	modifier la première ligne en “ELEVEN DT -MASTER”
	4.	echap => retour au mode interactif 
	5.	 :wq => enregistre les modification du fichier et quitte vim


26/ Commiter et pusher sur github
	1.	git add -p
	2.	git commit -m “ modified Eleven.md “ 
	3.	git push -d origin master


27/28 Faire un rebase de la branche “EB-eleven-other-branch” sur master.
	1.	git checkout EB-eleven-other-branch
	2.	git rebase master
	3.	vim eleven.md > on passe au mode insertion pour gérer le conflit et garder le contenu qui est dur la branche Master.
	4.	git add .
	5 .	git rebase —skip


	9. Commiter et créer une pull request sur github
	1.	git add -p
	2.	git commit -m « message » 
	3.	git pull https://github.com/Ylahjaily/elevenproject.git EB-eleven-other-branch 
	4.	git push origin EB-eleven-other-branch 
	5.	Aller sur GitHub > repo elevenproject > Pull requests > Base : Master , comparer à EB-eleven-other-branch > confirmer

	30. Commiter ce dossier ainsi que ces images sur master et pusher sur github
	1.	git add . ; git commit -m « V1 » 
	2.	git pull https://github.com/Ylahjaily/elevenproject.git master
