# CORSO GIT/GITHUB SORINT4SCHOOL
Guida passo per passo al successo!

***

## FASE 1
--> CREAZIONE DI DUE UTENTI SULLA PROPRIA MACCHINA, CHE NEL CORSO DELLE LEZIONI COLLABORERANNO A UN PROGETTO.
1. USER01
2. USER02

--> CREAZIONE CARTELLA DI LAVORO IN USER01
1. mkdir project01
2. cd project01

--> FAI PRIMO SCRIPT
* vim sayhello.sh
'''
#!/bin/bash

echo "hello!"
~
~
'''

--> ASSEGNA PERMESSO DI ESECUZIONE E VERIFICA
1. chmod +x sayhello.sh
2. ./sayhello.sh

--> DAI FORMA ALLA DIRECTORY GIT!
1. git init
2. visualizza branch master con:
	* git branch
	* è vuoto
3. visualizza untracked del branch master con:
	* git status
	* troverai il nostro sayhello.sh

--> TRACCIA SAYHELLO.SH + COMMIT
1. git add sayhello.sh
2. git commit
3. Inserisci messaggio di commit chiaro per aiutare a comprendere quanto hai fatto!

***

!!! DEVI INSERIRE INFORMAZIONI UTENZA !!!
1. git config --global user.email 'xxxxxxxx@yyyyy.com'
2. git config --global user.name 'xyxyxyx'
3. rifai: git commit

***

--> VISUALIZZA QUANTO HAI FATTO
1. git log
2. visualizza ultimo commit fatto
	* git show
3. visualizza un commit diverso dall'ultimo
	* git show [id_commit]

--> MODIFICARE FILE ESISTENTE
1. vim sayhello.sh
2. inserisci la modifica che desideri
3. salva [:wq]
4. osserva la modifica fatta dal branch master
	* git status
5. git add sayhello.sh
6. git commit -a [attenzione, perchè l'opzione -a include tutto i file aperti/modificati nel commit]
7. inserisci messaggio di commit

--> VISUALIZZA QUANTO E' STATO FATTO
1. git log
2. git log --graph

--> NUOVO BRANCH: UNITA' DI LAVORO DIRAMATA, FUORI DA BRANCH MASTER
1. git branch test01
2. visualizzare tutti i branch:
	* git branch
3. spostarsi di branch:
	* git checkout test01

--> MODIFICARE FILE IN NUOVO BRANCH
1. vim sayhello.sh
2. git status
3. per vedere modifiche fatte:
	* git diff
4. git add sayhello.sh
5. git commit -a
6. inserisci messaggio di commit

***

--> visualizza
--> git checkout test02
--> vim sayhello.sh
--> git add sayhello.sh
--> git commit -a
--> inserisci messaggio di commit

