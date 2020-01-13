<h3>1/ Créer en ligne de commande un nouveau projet Symfony portant le nom“elevenproject”.</h3>
<p>composer create-project symfony/website-skeleton elevenproject </p>

<h3>2/ Créer un repository public depuis Github portant le nom “eleven”. </h3>
	<ol>
		<li>A partir de ma page GitHub : </li>
		<li>Cliquer sur New.</li>
		<li>Donner le nom “eleven” au repository.</li>
		<li>Cocher la case « Public. »</li>
		<li>Créer le repository.</li>
	</ol>
<h3>3/ Générer une clé SSH pour votre utilisateur linux (sans pass phrase).</h3>
	<ol>
		<li>	Sur le terminal => ssh-keygen - t rsa -b 4096  -C « y.lahjaily@ecole.ipssi.net »</li>
		<li>	Sur le terminal => ssh add < ~/.ssh/id_rsa.pub
	</ol>
			
<h3>4/ Ajouter la clé publique correspondant sur votre compte Github, pour pouvoir pousser sur github sans avoir à saisir l’utilisateur et le mot de passe à chaque fois.</h3>
	<ol>
		<li>	Copier la clé générée : pbcopy < ~/.ssh/id_rsa.pub.
		<li>	 Sur gitHub , aller dans settings > SSH and GPG keys et faites ajouter une clé.
 	</ol>
			
<h3>5/ Commiter et pusher le projet sur le repository distant avec le message “Project initialization” sur master.</h3>
	<ol>
		<li>	git add -p </li>
		<li>	git commit -m « Project initialization » </li>
		<li>	git remote add origin  https://github.com/Ylahjaily/elevenproject.git </li>
		<li>	git push –d origin master </li>
	</ol>
			
<h3> 6/ Tirer une nouvelle branche depuis master que vous appellerez “EB-eleven-branch”</h3>
	<ol>
		<li>git checkout -b  “EB-eleven-branch”</li>
	</ol>
<h3> 7/ Aller dans le dossier “elevenproject/public”
	<ul>
		<li>cd elevenproject/public </li>
	</ul>
<h3>8/ Exporter les 10 premières lignes du fichier “index.php” dans un fichier “extract-file.txt”en ligne de commande</h3>
	<ul>
		<li>head -n 10 index.php >> extract-file.txt  </li>
		<li>On peut aussi le faire avec : </li>
		<li>=>  sed -n -e '1,10p' index.php > extract-file.txt</li>
	</ul>

<h3>9/ Afficher dans le terminal le contenu du fichier créé</h3>
	<ul>	
		<li>cat extract-file.txt</li>
	</ul>

<h3>10/ Remonter d’un niveau depuis le dossier courant</h3>
	<ul>
		<li>cd .. </li> 
	</ul>

<h3>11/ Créer un dossier “elevenlog”</h3>
	<ul>
		<li>mkdir elevenlog<li>
	</ul>
	
<h3>12/ Copier le fichier “extract-file.txt” dans le dossier précédemment créé.
 	<ul>
		<li> cp /Users/citizen99xyz/workspace/elevenproject/public/extract-file.txt /Users/citizen99xyz/workspace/elevenproject/elevenlog </li>
	</ul>

<h3>13/ Déplacer le dossier “elevenlog” dans “app/templates”</h3>
	<ul>
		<li>mv /Users/citizen99xyz/workspace/elevenproject/template/extract-file.txt /Users/citizen99xyz/workspace/elevenproject/elevenlog /Users/citizen99xyz/workspace/elevenproject/template/extract-file.txt /Users/citizen99xyz/workspace/elevenproject/template </li>
	</ul>


<h3>14/Supprimer le fichier “extract-file.txt” se trouvant dans “public”</h3>
	<ul>
		<li>rm extract-file.txt
	</li>
</ul>
<h3>15/ Commiter les modifications apportées dans le dossier “app/templates” et pusher sur github</h3>
	<ul>	<li>git add "app/templates"</li>
		<li>git commit -m "moove elevenlog";</li>
		<li>git push origin “EB-eleven-branch” </li>
	</ul>
<h3>16/ Créer une Pull Request sur Github pour merger vers master</h3>
	<ul>
		<li>Sur Github > Aller dans le repository Elevenproject > Cliquer sur Pull Requests > New Pull Request > sélectionner Master en branche de base et EB-eleven-branch embranche à comparer. </li>
	</ul>
			
<h3>17/ Revenir sur la branche master du projet</h3>
	<ul>
		</li>git checkout master</li>
	</ul>

<h3>18/ Créer le ficher “ELEVEN.md” à la racine du projet</h3>
	<ul>	
		<li>touch eleven.md</li>	
	</ul>
	
<h3>19/ L’ouvrir avec vim, ajouter la ligne “ELEVEN DT - TEST” en tête de fichier</h3>

	1.	vim eleven.md => ouverture du fichier dans l’éditeur vim.
	2.	i => passage au mode insertion.
	3.	ajouter la ligne “ELEVEN DT - TEST” en tête de fichier
	4.	echap => retour au mode interactif.
	5.	 :wq => enregistre les modification du fichier et quitte vim.

<h3>20/ Commiter le fichier sur master et pusher sur github</h3>
	<ol>
		<li>git add -p</li>
		<li>git commit -m « added text to Eleven.md »</li>
		<li>git pull https://github.com/Ylahjaily/elevenproject.git master</li>
		<li>git push origin master
	</ol>

<h3>21/ Créer une nouvelle branche: “EB-eleven-other-branch” depuis master</h3>
	<ul>
		<li>git checkout -b EB-eleven-other-branch</li>
	</ul>

<h3>22/ Ouvrir le fichier “ELEVEN.md” avec vim, modifier la première ligne en “ELEVEN DT -BRANCH”.</h3>
	<ol>
		<li>	Vim eleven.md </li>
		<li>	i =>passage au mode insertion </li>
		<li>	remplacer la ligne “ELEVEN DT - TEST” en tête de fichier par « ELEVEN DT - BRANCH »</li>
		<li>	echap => retour au mode interactif </li>
		<li>	 :wq => enregistre les modification du fichier et quitte vim</li>
	</ol>
	
<h3>23/ Commiter les informations et pusher sur github</h3>
	<ol>
		<li>	git add -p </li>
		<li>	git commit -m « added text to Eleven.md »</li>
		<li>	git push origin EB-eleven-other-branch</li>
	</ol>
	
<h3>24/ Revenir sur la branche master.</h3>
	<ol>
		<li>Git checkout master</li>
	</ol>

<h3>25/ Ouvrir le fichier “ELEVEN.md” avec vim, modifier la première ligne en “ELEVEN DT -MASTER”</h3>
	<ol>
		<li>	Vim eleven.md </li>
		<li>	i =>passage au mode insertion </li>
		<li>	modifier la première ligne en “ELEVEN DT -MASTER” </li>
		<li>	echap => retour au mode interactif </li>
		<li>	 :wq => enregistre les modification du fichier et quitte vim </li>
	</ol>

<h3>26/ Commiter et pusher sur github</h3>
	<ol>
		<li>git add -p</li>
		<li>2.	git commit -m “ modified Eleven.md “ </li>
		<li>3.	git push -d origin master</li>
	</ol>

<h3>27/28 Faire un rebase de la branche “EB-eleven-other-branch” sur master.</h3>
	<ol>
		<li>	git checkout EB-eleven-other-branch </li>
		<li>	git rebase master </li>
		<li>	vim eleven.md > on passe au mode insertion pour gérer le conflit et garder le contenu qui est dur la branche Master. </li>
		<li>	git add . </li>
		<li>	git rebase —skip </li>
	</ol>

<h3>29. Commiter et créer une pull request sur github</h3>
	<ol>
		<li>	git add -p </li>
		<li>	git commit -m « message » </li>
		<li>	git pull https://github.com/Ylahjaily/elevenproject.git EB-eleven-other-branch </li>
		<li>	git push origin EB-eleven-other-branch </li>
		<li>	Aller sur GitHub > repo elevenproject > Pull requests > Base : Master , comparer à EB-eleven-other-branch > confirmer </li>
	</ol>

<h3>30. Commiter ce dossier ainsi que ces images sur master et pusher sur github</h3>
	<ol>
		<li>	git add . ; git commit -m « V1 » </li>
		<li>	git pull https://github.com/Ylahjaily/elevenproject.git master </li>
	</ol>
