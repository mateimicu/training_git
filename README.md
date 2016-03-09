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
        - [ ] Ex.5 Make your own repo
        - [ ] Ex.6 Push your own changes ( both branches )
        - [ ] Ex.7 Clone my test repo
        - [ ] Ex.6 Push my_repo on your GitHub
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
Este chiar continutul directorului tau cu toate modificarile lui
  
** Staging area **
Este o zona "separata" in care sunt pastrate fisierele pe care tu ai decis ca sunt okay.
  
** Repository **
Este chiar zona in care se pastreaza commiturile, ( snapshoturile ), nimic nu poate exista in zona asta daca nu este sub forma unui commit.

Aceste zone sunt reprezentate asa conceptula.Un workflow specific git ar fi urmatoru:
	- Initializez repository ( adica creez un `.git` in folderu curent si asa acesta devine un repository, comanda pentru asta `git init` )
	- Adaug fisiere / fac modificari fisierelor ( asta se face doar in **working directory** )
	- Dupa ce am decis ca anumite fisiere (X, Y, Z) sunt complete si sunt la o versiune anume, le adaug in staging area ( cu alte cuvinte versiunea actuala a fisierelor, va face parte din viitorul commit )
	Obs.
	Comanda pentru a adauga un fisier din **working directory** in **staging area** este `git add <nume_fisier>`
	- Repet adaugatul fisierelor in **staging area** pana cand toate fisierele care au fost modificate ajung la o versiune  "stabila"( cu alte cuvinte cred ca fisierele care se afla in staging area ar constitui un commit, snapshot )
	- Impachetez fisierele din **staging area** intr-un commit folosind comanda `git commit`, o sa se deschita un editor de text ( nano cel mai probabil ) care te roaga sa descrii continutul commitului ( sa le fie mai usor altor dezvoltatori sa inteleaga ce vrei sa faci ), dupa ce salvezi mesajul commitul este salvat. Poti sa vezi commiturile folosind `git log`.
	
#### 3.2 Branches
In git pot executa mai multe "fire" de dezvoltare al unui proiect. Adica de la un anumit punct ( commit mai exact ) doriti sa puteti crea doua commituri independente. Un exemplu ar fi urmatoru : Lucrati la un proiect cu o persoana, pana intr-un punct ati lucrat de la acelasi pc, dar acum mergeti fiecare acasa si aveti fiecare de terminat o functie anume, ca sa fiti siguri ca nu stricrati programul creati doua branchiuri (A si B), fiecare implementeaza functia lui pe un branch iar la final le combinati.Voi nota cu M branchiul master( cel default pe care ati lucrat la comun ).

            M - commit_m1
                    |
                commit_m2
                    |
                commit_m3
                    |
                commit_m4
                    |
            (crearea banchiurilor)
            /        |        \
    A - commit_a1    |   B - commit_b1
        |         |          |
        commit_a2    |        commit_b2
        |         |          |
        commit_a3    |        commit_b3
        |         |          |
        commit_a4    |        commit_b4
        |         |          |
        commit_a5    |          |
        |         |          |
        \                    /
            \                  /
            \                /
            \              /
            \            /
            ( Merging, combinare)
                    |
            M - commit_m5   <- acest commit combina cele doua branchiuri 

Pentru a crea o noua branch folosim `git branch <nume_branch>`		
Pentru a ne muta pe ea `git checkout <nume_branch>`		
Putem combina cele doua comenzi ( sa cream si sa ne mutam pe o branch ) `git checkout -b <nume_branch>`
Commiturile pe branchiuri se fac normal.

#### 3.3 Merging 
Dupa cum am vazut noi putem combina  doua branchiuri sau mai multe putem folosi comanda `git merge <nume_branch>`. Dar lucrurile sunt mai simple. Noi putem face mergi doar intre doua branchiuri, cand folosim comanda noi spunem ca facem merge intre branchiul pe care ne aflam si cel dat ca parametur comenzi, pentru a optine rezultaul de mai sus ar trebui sa facem ceva de genu :

            M - commit_m1
                    |
                commit_m2
                    |
                commit_m3
                    |
                commit_m4
                    |
            (crearea banchiurilor)
            /        |        \
    A - commit_a1    |   B - commit_b1
        |         |          |
        commit_a2    |        commit_b2
        |         |          |
        commit_a3    |        commit_b3
        |         |          |
        commit_a4    |        commit_b4
        |         |          |
        commit_a5    |          |
        |         |          |
        \         |          |
            \        |          |
            \( git merge A)    |
                    |          |
            M - commit_m5      /
                    |         /
                    |        /
                    |       /
                    |      /
            (git merge B)
                    |
            M - commit_m6 <- acest commit are acum toate schimbarile

Daca ne uitam acum peste `git log` fiind pe branchiul M o sa vedem ceva de genu
    commit_b4
        |
    commit_b3
        |
    commit_b2
        |
    commit_b1
        |
    commit_b1
        |
    commit_a5
        |
    commit_a4
        |
    commit_a3
        |
    commit_a2
        |
    commit_a1
        |
    commit_m4
        |
    commit_m3
        |
    commit_m2
        |
    commit_m1

Cu alte cuvinte ordinea in care au loc commiturile este data de ordinea in care li se face merge.
                
#### 3.4 Exercitii 
- Ex1. Create Repo
Aici as vrea sa creati ( initializati  ) un repository la voi pe calculator.
- Ex2. Creare commits
In acest repot as vrea sa creati 3 fisiere cu numele :1.txt, 2.txt, 3.txt.DAR,
fiecare fisier trebuie creat intr-un commit direfit. 
- Ex3. Create a branche
Creati o noua branch ( ramura ), cu numele "newNumbers" in care veti crea alte 3 fisiere ( in comituri diferite ) cu numelele: 4.txt, 5.txt, 6.txt
- Ex4. Merging
Aici o sa va mutati pe branchiul master si o sa aduceti pe aest branch schimbarile de pe branchiul "newNumbers"


### 4. GitHub Explained
   
#### 4.1 What is good for?
Git este doar un tool, el pastreaza niste snapshoturi despre continutul unui director( mai bine zis o istorie a continutului ). Toolul nu are nevoie de internet, el pastreaza toate informatile intr-un fisier ascuns ( se numeste `.git` ).
    GitHub este un serviciu care iti permite sa pastrezi istoria asta pe un server, in asa fel poti sa clonezi aceasta informatie.


#### 4.2 Creare cont
Crearea contului este clasica ... aveti nevoie de email valid, o parola si totul ar trebui sa mearga usor.
#### 4.3 Creare repo
Noi avem un repopository pe pc ( cel creat de noi ), dar el nu este si pe GitHub.Pentru a putea urca repoul pe GitHub trebuie sa ii facem un loc, sa cream un repository golin care sa urcam schimbarile. 
Pe prima pagina ar trebui sa vedem un buton cu verge "New Repository".Daca dam click pe el si ar trebui sa ne apara un meniul de unde setam diferite lucruri pentru repoul nostru.

#### 4.5 Uploading 
Ca sa uploadam ( terminologia git este "sa facem **push**" ) schimbarile nostre pe server trebuie sa stim ceva, linkul repositoriului.Acest link este in partea de sus si este de forma "https://github.com/USERNAME/NUME_REPOSITORU.git". Daca stim linkul putem folosi comanda `git push LINK BRANCH`, in limbaj mai natural comanda asta spune ceva de genu :
"Incarca la linkul LINK, toate commiturile de pe branchiul pe care sunt, pe branchiul BRANCH de pe servarul specificat prin link".

Exista un dezavantaj sa trebuiasca mereu sa punem linkul acolo. O varianta este sa setam un alias pentru acel link, sa il salvam undeva. Git ofera aceasta posibilitate prin ceea ce el demuneste **remote** adica linkurile catre repositoriurile remote. Pentru a adauga unul putem folosi `git remote add <alis_pentru_link>  <link_catre_repo>`. Dupa ce am facut asta putem folosi `git push <alias_pentru_link> <branch>`.

Poti clona un repository de pe GitHub cu tot continutul folosint :  
`git clone <link_catre_repo>`  
Cand faci asta se va seta un **remote** denumit `origin` cu linkul de unde ai clonat ( deoarece de cele mai multe ori tot acolo o sa doresti sa urci schimbarile )

Se va clona doar un branch dar daca doriti sa aveti local si alte branchiuri de pe server puteti folosi comanda `git checkout -b <nume_branch_local>   <remote_name>/<nume_branch_remote>`. Exemplu `git checkout -b test origin/master`.
Pentru a vedea toate branchiurile remote puteti folosi `git branch  -a `.

#### 4.6 Exercitii
- Ex.5 Make your own repo
Creaza un repositoru **pe GitHub**  cu numele "training"
- Ex.6 Push your own changes ( both branches )  
- 6.1 Adauga ca remote la repositoriul facult local in exercitiile trecute linkul de la repositoriul creat pe GitHub.
- 6.2 Incarca schimbarile de pe branchiul **master** ( local  ) pe branchiul **master** remote(pe GitHub adica)
Obs. Daca branchiul remote nu exista el va fi creat automat
- 6.3 Incarca schimbarile de pe branchiul **newNumbers** ( local  ) pe branchiul **demoBranch** remote(pe GitHub adica)
Obs. Daca branchiul remote nu exista el va fi creat automat
- Ex.7 Clone my test repo
Cloneaza repositoriul trainingului ( https://github.com/micumatei/training_git  ) la tine pe calculator
-  Ex.6 Push my_repo on your GitHub
Incarca repositoriul trainingului intr-un repository nou la tine pe Git.

### 5. Colaboration and final exercise
Inainte de toate ne dati numele de git si va adaugat in organizatia ASII de pe GitHub.Acolo se va afla un repository de exercitiu, toti trebuie sa faceti urmatori pasi:
- Clonati repositoriul
- Creati un branch nou, numele branchiului va fi numele vostru.
- Creati un director nou pe branchiul ala in care scrieti un program care afiseaza
"Hello world" in C/C++/Python/JavaScript, orce doriti.
- Faceti push la branchiul acela pe GitHub.
- Va alegeti un partener
- Clonati de pe server si branchiul partenerului 
- Dati merge la branchiul partenerului peste branchiul dumneavoastra
- Faceti push cu schimbarile pe server

    
### 6. Referinta
#### 6.1 Tutotiale
	- https://try.github.io/levels/1/challenges/1
	- http://pcottle.github.io/learnGitBranching/
#### 6.1 Bibliografie 
    - https://git-scm.com/book/en/v2/Getting-Started-Git-Basics
	- https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging










