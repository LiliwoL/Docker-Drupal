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

* PHPMyAdmin
	http://localhost:8081

* MailHog

    Client Mail: http://localhost:8025
    Serveur SMTP localhost:1025

    * Tester MailHog via telnet

    Vous pouvez facilement l'envoi de mail via telnet

    *Sur MacOs, pour installer telnet*

    ```bash
    brew install telnet
    ```

    ```bash
    $ telnet localhost 1025

    EHLO mailhog.example
    MAIL FROM:<mon_adresse@mail.fr>
    RCPT TO:<mon_adresse_destinataire@mail.fr>
    DATA
    Subject: Hello World

    Hello World!
    .
    QUIT
    ```

    Tapez chaque ligne et appuyez sur Entrée à chaque fois.

    Le message devrait apparraitre dans l'interface de Mailhog accessible via:

    http://localhost:8025
