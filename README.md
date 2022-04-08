# Docker pour Drupal

Un environnement Docker pour utiliser Drupal 9

## Lancement

Après avoir cloné ce dépôt:

	docker-compose up

## commandes utiles

* Liste des containers

	docker container ls

* Prunage des containers non utilisés

	docker container prune

## Terminal

* Lancement du terminal sur le container du service apache

	bin/shell

## Services

* Site Web
	http://localhost

* Serveur SQL
	localhost
	Port 3306

* Adminer
	http://localhost:8080

* MailHog

	Client Mail: http://localhost:8025
	Serveur SMTP localhost:1025

	* Tester MailHog via telnet

	Vous pouvez facilement l'envoi de mail via telnet

	```bash
	$ telnet localhost 1025

	EHLO 19ft.com
	MAIL FROM:
	RCPT TO:
	DATA
	Subject: Hello World

	Hello World!
	.
	QUIT
	```

	Tapez chaque ligne et appuyez sur Entrée à chaque fois.

	Le message devrait apparraitre dans l'interface de Mailhog accessible via:

	http://localhost:8025
