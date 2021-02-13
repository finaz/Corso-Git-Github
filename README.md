# CORSO GIT/GITHUB SORINT4SCHOOL
Guida passo per passo al successo!

***

## FASE 1
* CREAZIONE DI DUE UTENTI SULLA PROPRIA MACCHINA, CHE NEL CORSO DELLE LEZIONI COLLABORERANNO A UN PROGETTO.
1. USER01
2. USER02

<br />

* CREAZIONE CARTELLA DI LAVORO IN USER01
1. mkdir project01
2. cd project01

<br />

* FAI PRIMO SCRIPT
1. vim sayhello.sh
```
#!/bin/bash

echo "hello!"
~
~
```
<br />


* ASSEGNA PERMESSO DI ESECUZIONE E VERIFICA
1. chmod +x sayhello.sh
2. ./sayhello.sh

<br />

* DAI FORMA ALLA DIRECTORY GIT!
1. git init
2. visualizza branch master con:
	* git branch
	* è vuoto
3. visualizza untracked del branch master con:
	* git status
	* troverai il nostro sayhello.sh

<br />

* TRACCIA SAYHELLO.SH + COMMIT
1. git add sayhello.sh
2. git commit
3. _Inserisci messaggio di commit chiaro per aiutare a comprendere quanto hai fatto!_
<br />

***

### !!! DEVI INSERIRE INFORMAZIONI UTENZA !!!
1. git config --global user.email 'your@email.com'
2. git config --global user.name 'yourname'
3. rifai: git commit

***
<br />

* VISUALIZZA QUANTO HAI FATTO
1. git log
2. visualizza ultimo commit fatto
	* git show
3. visualizza un commit diverso dall'ultimo
	* git show [id_commit] 

<br />

* MODIFICARE FILE ESISTENTE
1. vim sayhello.sh
2. inserisci la modifica che desideri
3. salva [:wq]
4. osserva la modifica fatta dal branch master
	* git status
5. git add sayhello.sh
6. git commit -a [attenzione, perchè l'opzione -a include tutto i file aperti/modificati nel commit]
7. _inserisci messaggio di commit_

<br />

* VISUALIZZA QUANTO E' STATO FATTO
1. git log
2. git log --graph
<br />

***

## FASE 2
* NUOVO BRANCH: UNITA' DI LAVORO DIRAMATA, FUORI DA BRANCH MASTER
1. git branch test01
2. visualizzare tutti i branch:
	* git branch
3. spostarsi di branch:
	* git checkout test01

<br />

* MODIFICARE FILE IN NUOVO BRANCH
1. vim sayhello.sh
2. git status
3. per vedere modifiche fatte:
	* git diff
4. git add sayhello.sh
5. git commit -a
6. _inserisci messaggio di commit_
<br />


* VISUALIZZA QUANTO E' STATO FATTO
1. git log --graph
2. git log --graph --all --decorate

<br />

* PORTARE LE MODIFICHE DA BRANCH TEST01 A BRANCH MASTER [AGGIORNARE I COMMIT DA BRANCH A BRANCH]
1. git checkout master
2. git merge test01
3. visualizza:
	* git log --graph --all --decorate
<br />


* SIMULAZIONE DOPPIO BRANCH - CONFLITTO
1. git branch test02
2. restando su branch master:
	* vim sayhello.sh
3. git status
4. git diff
5. git add sayhello.sh
6. git commit -a
7. inserisci messaggio di commit
8. _visualizza_
9. git checkout test02
10. vim sayhello.sh
11. git add sayhello.sh
12. git commit -a
13. _inserisci messaggio di commit_
14. _visualizza_
15. git checkout master
16. git merge test02
17. **!!! CONFLITTO !!!**
18. git status
19. vim sayhello.sh
20. **!!! RISOLVI CONFLITTO !!!**
21. git status
22. git add sayhello.sh
23. git commit -a
24. _inserisci messaggio di commit_
25. _visualizza_

<br />

* RIMUOVERE BRANCH CHE NON SERVONO
1. git branch -d test01
2. git branch -d test02
3. _visualizza_
<br />

* MODALITA' CHERRY-PICK
1. git branch test03
2. git checkout test03
3. vim sayhello.sh
4. git add sayhello.sh
5. git commit -a
6. _inserisci messaggio di commit_
7. _visualizza_
8. git checkout master
9. git cherry-pick [id_commit]
10. git branch -d test03
11. git branch -D test03
12. _visualizza_
<br />

* TOGLIERE IL COMMIT
1. per tornare al commit precedente:
	* git reset
2. per togliere il commit senza togliere modifiche fatte:
	* git reset --soft [id_commit]
<br />

***

## FINE PRIMA PARTE

***
<br />

# SECONDA PARTE - DA GIT A GITHUB

***

**COLLABORAZIONE TRA DUE UTENTI [da Git a Github]**
<br />

* IN USER02
1. git clone ssh://[user@]host.xz[:port]/path/to/repo.git
2. _visualizza_
3. git branch
4. git branch -a
<br />

* IN USER01
1. vim sayhello.sh
2. git add sayhello.sh
3. git commit -a
4. messaggio di commit
5. _visualizza_ in user01 e in user02
<br />

* IN USER02
1. git fetch
2. _visualizza_
3. per vedere qualche info in più:
	* git branch -avv
4. git merge origin/master
5. è possibile unire fetch e merge in un unico comando
	* git pull
<br />

**GITHUB**
<br />

* Crea nuova repository su github.com
* In user01
1. git remote add origin [id_github]
2. ssh-keygen [con password]
3. cat ~/.ssh/id_rsa.pub
4. copia e incolla in github.com [settings > SSH keys]
5. git branch -M master
6. git push -u origin master
7. inserire username e la password di github

* PASSARE A SSH
1. cat .git/config
2. prendi url ssh da github.com
3. vim .git/config
4. cambia url [remote "origin"] all'interno del file con quello copiato da github
5. vim sayhello.sh
6. git add sayhello.sh
7. git commit -a
8. _messaggio di commit_
9. git push origin master

<br />

* COLLABORAZIONE TRA UTENTI
1. In user02 rimuovi cartella precedente:
	* rm -rf project01/
2. su github.com cerca il progetto di user01
3. clona repository di user01
	* git clone [https://github.com/user01/nomeprogetto]
4. cd project01/
5. _visualizza_

<br />

* MODIFICA E PUSH DA USER02
1. creare un fork dal progetto su github.com
2. git remote add github [SSH_key]
3. vim sayhello.sh
4. git add sayhello.sh
5. git config --global user.email 'your@email.com'
6. git config --global user.name 'yourname'
7. git commit -a
8. _messaggio di commit_


