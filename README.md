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
2. git commit -a

***

!!! DEVI INSERIRE INFORMAZIONI UTENZA !!!
1. git config --global user.email 'xxxxxxxx@yyyyy.com'
2. git config --global user.name 'xyxyxyx'
3. rifai: git commit -a

***



