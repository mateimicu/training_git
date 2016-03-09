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
        - [ ]Ex.5 Clone my test repo
        - [ ] Ex.6 Push some changes
        - [ ] Ex.7 Make your own repo
        - [ ] Ex.8 Push your own changes ( both branches )
- [ ] 5. Colaboration and final exercise
- 6. Referinte
	- 6.1 Tutoriale
	- 6.2 Bibliografie


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
In git exista mai multe stagii:
    - Working Directory
    - Staging area
    - .git directory ( repository )
![alt tag](https://git-scm.com/book/en/v2/book/01-introduction/images/areas.png)
** Working Directory **
Este chear continutul directorului tau cu toate modificarile lui
  
** Staging area **
Este o zona "separata" in care sunt pastrate fisierele pe care tu ai decis ca sunt okay.
  
** Repository **
Este chear zona in care se pastreaza commiturile, ( snapshoturile ), nimic nu poate exista in zona asta daca nu este sub forma unui commit.

Aceste zone sunt reprezentate asa conceptula.Un workflow specific git ar fi urmatoru:
	- Initializez repository ( adica creez un `.git` in folderu curent si asa acesta devine un repository, comanda pentru asta `git init` )
	- Adaug fisiere / fac modificari fisierelor ( asta se face doar in **working directory** )
	- Dupa ce am decis ca anumite fisiere (X, Y, Z) sunt complete si sunt la o versiune anume, le adaug in staging area ( cu alte cuvinte versiunea actuala a fisierelor, va face parte din viitorul commit )
	Obs.
	Comanda pentru a adauga un fisier din **working directory** in **staging area** este `git add <nume_fisier>`
	- Repet adaugatul fisierelor in **staging area** pana cand toate fisierele care au fost modificate ajung la o versiune  "stabila"( cu alte cuvinte cred ca fisierele care se afla in staging area ar constitui un commit, snapshot )
	- Impachetez fisierele din **staging area** intr-un commit folosind comanda `git commit`, o sa se deschita un editor de text ( nano cel mai probabil ) care te roaga sa descrii continutul commitului ( sa le fie mai usor altor dezvoltatori sa inteleaga ce vrei sa faci ), dupa ce salvezi mesajul commitul este salvat. Poti sa vezi commiturile folosind `git log`.
	
#### 3.2 Branches
In git pot executa mai multe "fire" de dezvoltare al unui proiect. Adica 
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
    - Ex.5 Clone my test repo
    - Ex.6 Push some changes
    - Ex.7 Make your own repo
    - Ex.8 Push your own changes ( both branches )

### 5. Colaboration and final exercise

    
### 6. Referinta
#### 6.1 Tutotiale
	- https://try.github.io/levels/1/challenges/1
	- http://pcottle.github.io/learnGitBranching/
#### 6.1 Bibliografie 
    - https://git-scm.com/book/en/v2/Getting-Started-Git-Basics
	- https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging










