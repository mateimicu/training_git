# Training Git & GitHub ( ASII )

  
### 1. Instalare

#### 1.1 Windows
    Descarcam installerul de la [aici](http://git-scm.com/download)
    Dupa rulare, vedem unde a fost instalat git-ul.
        Exemple de path pot fi :
            - `C:\Program Files (x86)\Git\bin`
            - `C:\Program Files\Git\bin`
    Dupa ce stim exact care este ar trebui sa putem rula `path/to/file/git --version`, daca comanda este recunoscuta atunci path-ul gasit este corect.
    Adaugam path-ul corect  in enviromentul de sistem.
    Pasi :
        - Click dreapta *My Computer*
        - Click *Adcanve System Settings*
        - Click *Evironment Variables*
        - La tabul cu *System Variables* 
        - Cauta variabila *path* si apasa pe *editare*
        - Adaugat pathul gasit la sfarsitul textului ( Obs. Adaugat un `;` inainte sa dai paste )

    //////// pas -> cu -> pass -> unde -> se -> acceseaza 

#### 1.2 Linux
    Depinde in functie de sistem:

    *Ubuntu si Debian like sistem (Ubuntu, linux mint):**
        `
        sudo apt-get update
        sudo apt-get upgrade
        sudo apt-get install git-all
        `

    *Arch Linux sistem (Ubuntu, fedora, linux mint):**
        `
        pacman -S git
        De completat
        `

    *Solaris Linux sistem (Fedora):**
        `
        sudo yum install git-all
        `

#### 1.3 Mac OS X 
    Descarca instalelul de [aici](http://git-scm.com/download) si urmeaza pasi din el.

#### 1.4 Test
    Daca comanda `git --version` returneaza ceva de genu `git version 1.9.x` totul e okay.
    


### 2. Introducere Basic in CLI ( command line intercade  )
    


# Structura training
- [ ] 1. Instalare
    - [ ] 1.1 Windows
        - [ ] Install Git
        - [ ] Add to PATH
        - [ ] Get an working shell with git
    - [ ] 1.2 Linux
        - [ ] Install Git
        - [ ] Get an working shell with git
    - [ ] 1.3 Mac OS X
        - [ ] Install Git
        - [ ] Get an working shell with git

    - [ ] 1.4 Test
        Se ruleaza `git --version`
- [ ] 2. Basic CLI commands
    - [ ] 2.1 Moving around folders( cd, ., .. )
    - [ ] 2.2 Creating/Deleting directorys or files (mkdir, touch, rm, rmdir )
- [ ] 3. Basic Git Paradigma
    - 







