# HOW TO INSTALL POWERLINE - LINUX
***
<br />

### Powerline è una feature molto diffusa tra gli sviluppatori software, offrendo un'esperienza personalizzata del prompt dei comandi che include i prompt e la codifica a colori per gli stati di GIT.

<br />

* *FASE UNO*
1. Verificare di aver installato sul proprio sistema Python,
	* ``` python --version ```
	1. altrimenti:
	* ``` sudo apt install python ```
2. Verificare di aver installato l'opzione _pip_, 
	* ``` pip --version ```
	2. altrimenti:
	* ``` sudo apt install python-pip ```

* *FASE DUE*
1. Installare powerline shell tramite il comando _pip_:
	* ``` pip install powerline-shell ```
2. Occorre ora editare il file .bashrc, con l'editor che preferite:
	* es.: ``` vim ~/.bashrc ```
3. Inserendo in fondo al codice già presente il seguente script:
	```
	function _update_ps1() {
    	PS1=$(powerline-shell $?)
	}

	if [[ $TERM != linux && ! $PROMPT_COMMAND =~ _update_ps1 ]]; then
    	PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
	fi
	```
4. Infine, installare i fonts powerline:
	* ``` sudo apt-get install fonts-powerline

<br />
<br />

### Ottimo! Ora dovresti avere una powerline funzionante!
<br />
***
# THE END
