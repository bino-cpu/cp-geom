# Readme 
Git bash / Git hub
fjezkfezj,lezmfrel
## Résumé rapide
- [x] Configure ton nom/email
- [x] Génére et ajoute une clé SSH à GitHub
- [x] Clone ton dépôt
- [x] Ajoute/modifie des fichiers
- [x] git add, git commit, git push pour charger sur GitHub

## Breakdowwn

1. Configurer ton identité Git (une fois seulement)
Ouvre Git Bash et configure ton nom et ton email (les mêmes que sur GitHub) :
	```git config --global user.name "Ton Nom"```
	```git config --global user.email "ton.email@example.com"```
2. Vérifier ton identité actuelle
	```git config --global user.name```
	```git config --global user.email```
2. Modifier ton identité
Cela permet de te connecter à GitHub sans taper ton mot de passe à chaque fois. Dans Git Bash :
	```git config --global user.name "Ton Nouveau Nom"```
2. Générer une clé SSH (recommandé)	
Cela permet de te connecter à GitHub sans taper ton mot de passe à chaque fois. Dans Git Bash :
	```ssh-keygen -t ed25519 -C "ton.email@example.com"```
	Après avoir tapé la commande :
		Appuie sur Entrée pour accepter le dossier par défaut (/c/Users/ton_nom/.ssh/id_ed25519).
		Si demandé, indique un mot de passe ou appuie sur Entrée pour ne pas en mettre.

3. Ajouter la clé SSH à ton compte GitHub	
Copie la clé publique :
	```cat ~/.ssh/id_ed25519.pub```
- Copie le texte affiché sur GitHub > Settings > Deploy keys | SSH and GPG keys > New SSH key
- Colle ta clé, donne-lui un nom, puis valide.
4. Se connecter à un dépôt (repository)
	- Pour créer un nouveau dépôt sur GitHub : "New" ou "Nouveau repository".
		- Donne un nom, puis crée-le.
	- Cloner ce dépôt sur ton ordinateur : 
		- Récupère l’URL SSH du dépôt (git@github.com:...)
		- Dans Git Bash 
			```git clone git@github.com:ton-nom-utilisateur/nom-du-repo.git```
			```cd nom-du-repo```
5. Ajouter et charger des fichiers
	1- Ajoute (ou crée) tes fichiers dans le dossier du dépôt
		Par exemple, place monfichier.txt dans ce dossier.
	2- Ajoute les fichiers à Git :		
		```git add monfichier.txt```
	3- Prépare le commit :
		```bash
		git commit -m "Ajout de mon premier fichier"
		```
	4- Envoie (push) les fichiers sur GitHub :
		```
		bash
		git push origin main		
		```
