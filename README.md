# Training Git & GitHub 

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

    - [ ] 1.5 Configurare git 
    
    
- [ ] 2. Basic CLI commands
    - [ ] 2.1 Moving around folders( cd, ., .. )
    - [ ] 2.2 Creating/Deleting directorys or files (mkdir, touch, rm, rmdir )
    
- [ ] 3. Basic Git Concepts  
    - [ ] 3.1 Commits  
        - [ ] Stagiile din git ( working directory, staging area, commited )  
        - [ ] How to move a file betwen stages (`add`, `commit`, `reset`, `git rm`, ``git mv`)
    - [ ] 3.2 Branches 
        - [ ] Concepts and utility
        - [ ] How to make a branche 
        - [ ] How to move betwen branches
    - [ ] 3.3 Merging 
        - [ ] How to combine ( merge branches )
        - [ ] How to rezolve conflics
    - [ ] 3.4 Exercitii
        - [ ] Ex1. Create Repo
        - [ ] Ex2. Creare commits
        - [ ] Ex3. Create a branche
        - [ ] Ex4. Merging the two branches
  
- [ ] 4. GitHub explained
    - [ ] 4.1 What is good for ?
    - [ ] 4.2 Creare cont
    - [ ] 4.3 Creare repo
    - [ ] 4.4 Uploading
        - [ ] Clone an existing repo
        - [ ] Attach to an existing repo
        - [ ] Pushing to a repo
    - [ ] 4.5 Exercitii
        - Ex.5 Clone my test repo
        - Ex.6 Push some changes
        - Ex.7 Make your own repo
        - Ex.8 Push your own changes ( both branches )
- [ ] 5. Colaboration and final exercise


### 1. Instalare

#### 1.1 Windows
Descarcam installerul de [aici](http://git-scm.com/download) .
Dupa rulare, vedem unde a fost instalat git-ul.    
Exemple de path pot fi :   
- `C:\Program Files (x86)\Git\bin`   
- `C:\Program Files\Git\bin`    
Dupa ce stim exact care este ar trebui sa putem rula `path/to/file/git --version`, daca comanda este    recunoscuta atunci path-ul gasit este corect.   
Adaugam path-ul corect  in enviromentul de sistem.   
Pasi :   
- Click dreapta *My Computer*       
- Click *Adcanve System Settings*    
- Click *Evironment Variables*    
- La tabul cu *System Variables*        
- Cauta variabila *path* si apasa pe *editare*   
- Adaugat pathul gasit la sfarsitul textului ( Obs. Adaugat un `;` inainte sa dai paste )   
   
#### 1.2 Linux     
Depinde in functie de sistem:    
     
**Ubuntu si Debian like sistem (Ubuntu, linux mint):**    
`   
sudo apt-get update        
sudo apt-get upgrade      
sudo apt-get install git-all       
`
      
**Arch Linux sistem (Ubuntu, fedora, linux mint):**   
`
pacman -S git      
De completat   
`   

**Solaris Linux sistem (Fedora):**   
`  
sudo yum install git-all   
`  

#### 1.3 Mac OS X    
Descarca instalerul de [aici](http://git-scm.com/download) si urmeaza pasi din el.

#### 1.4 Test
Daca comanda `git --version` returneaza ceva de genu `git version 1.9.x` totul e okay.
    
#### 1.5 Configurare
Fiecare snapshot trebuie sa aiba o semnatura, adica un autor.
Pentru a specifica un autor global pentru git putem rula comenzile:  
`git config --local user.name "John Doe"`  
`git config --local user.email "johndoe@company.com"`  
     
    
### 2. Introducere Basic in CLI ( command line intercade  )
2.1 Dupa cum stim de la Sisteme de Operare ( Anu I semestru al II-lea ), comenzile pentru navigare prin fisiere:
- `cd <path>`  change directory
- `.`  alias pentru directorul curent
- `..`  alias pentru directorul parinte
  
2.2 Comenzi pentru crearea/stergerea de directoare/fisiere:
- `touch <nume_fisier>`  creaza un fisier gol
- `rm <path>` deleteaza un fisier
- `rmdir <path>` deleteaza un director gol

### 3. Basic Git Concepts
#### 3.1 Commits
#### 3.2 Branches
#### 3.3 Merging 
#### 3.4 Exercitii 
    - Ex1. Create Repo
    - Ex2. Creare commits
    - Ex3. Create a branche
    - Ex4. Merging the two branches


### 4. GitHub Explained
   
#### 4.1 What is good for?
Git este doar un tool, el pastreaza niste snapshoturi despre continutul unui director( mai bine zis o istorie a continutului ). Toolul nu are nevoie de internet, el pastreaza toate informatile intr-un fisier ascuns ( se numeste `.git` ).
    GitHub este un serviciu care iti permite sa pastrezi istoria asta pe un server, in asa fel poti sa clonezi aceasta informatie.


#### 4.2 Creare cont
#### 4.3 Creare repo
#### 4.4 Uploading 
#### 4.5 Exercitii

### 5. Colaboration and final exercise

    









