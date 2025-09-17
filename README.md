# cp-geom
maquette
1. Configurer ton identité Git (une fois seulement)
	git config --global user.name "Ton Nom"
	git config --global user.email "ton.email@example.com"
2. Vérifier ton identité actuelle
	git config --global user.name
	git config --global user.email

2. Modifier ton identité
	git config --global user.name "Ton Nouveau Nom"
2. Générer une clé SSH (recommandé)	
	ssh-keygen -t ed25519 -C "ton.email@example.com"

4. Ajouter la clé SSH à ton compte GitHub	
	cat ~/.ssh/id_ed25519.pub
- Copie le texte affiché sur GitHub > Settings > Deploy keys | SSH and GPG keys > New SSH key
- Colle ta clé, donne-lui un nom, puis valide.
  
4. Se connecter à un dépôt (repository)
	- Pour créer un nouveau dépôt sur GitHub : "New" ou "Nouveau repository".
		- Donne un nom, puis crée-le.
	- Cloner ce dépôt sur ton ordinateur : 
		- Récupère l’URL SSH du dépôt (git@github.com:...)
		- Dans Git Bash 
			- git clone git@github.com:ton-nom-utilisateur/nom-du-repo.git
			cd nom-du-repo
