# Training Git 2.0

Structura:
Timp aproximativ : 200 minute  
  
    
- 1. Recapitulare [80m]
    - 1.1 Initializare repo [5m]
    - 1.2 Commits [10m]
    - 1.3 Logs [5m]
    - 1.4 Branching [30m]
        - 1.4.1 Creare [10m]
        - 1.4.2 Stergere [10m]
        - 1.4.3 Tranzitie de pe un branch pe altul [10m]
    - 1.5 Merge branches [15m]
    - 1.6 Clone a remote repo [10m]
    - 1.7 Push to a remote repo [10m]
- 2. Schimbarea Istoriei [70m]
    - 2.1 Reverting [10m]
    - 2.2 Reset [10m]
    - 2.3 Rebasing [50m]
        - 2.3.1 Basic Rebasing [15m]
        - 2.3.2 Interactiv Rebasing [20m]
    - 2.4 Rezolvarea confictelor CLI [15m]
- 3. Colaborare [50m]
    - 3.1 On the same repo (using branches) [20m]
    - 3.2 On differit repos [30m]


## 1.Recapitulare
  
1.1 Initializarea unui repo :  
```vim
git init
```

1.2 Making a commit :  
```vim
git add <file> # add file in staing area
git commit -m "<mesaj de commit>" # crearea commitului
```

1.3 Look at the logs:  
```vim
git log
git log --pretty=<options>
git log --graph
```
#### 1.4 Branching
1.4.1 Crearea de branchiuri :  
```vim
git branch <nume branch>
git checkout -b <nume branch>
```

1.4.2 Deletarea unui branch :
```vim
git branch -d <nume branch>
git branch --delete <nume branch>
```
1.4.3 Switching branchiuri 
```vim
git checkout <nume branch>
```

- 1.5 Merge branches  
Merge ` <branch> `  in branchiul current.
```vim
git merge <branch>
```
1.6 Clone a remote repo
```vim
git clone <url catre repoul remote >
```

1.7 Push to a remote repo
```vim
git push <url catre repo / alias > <nume branch remote>
```


## 2. Schimbarea Istoriei

2.1 Reverting  
```vim
git revert <commit message / shortcut using HEAD>
```
2.2 Reset  
```vim
git reset <commit message / shortcut using HEAD>
```
### 2.3 Rebasing    
2.3.1 Basic Rebasing  
```vim
git rebase <branch>
```
2.3.2 Interactiv Rebasing  
```vim
git rebase -i <commit / shortcut using HEAD>

git --continue
git --abort
```
2.4 Rezolvarea confictelor CLI 
```vim
git status
# resolv conflicts
git add
git --continue
```


## 3. Colaborare 
3.1 On the same repo (using branches)
We can use the same repo and push to diferit branches then merge them, we don't hae the same controll and it's not indicated for big projects but it's quick and dirty for a small group of people.
3.2 On differit repos
We can "Fork" a repo ( make our own clone ), make our changes to a new branch then make a "Pull Request" to the "upstream"( the original repo )
