# Introduction to Git Github

Here we are mastering Git Github and other Version Control System. 

Here we will learn both theoratical and practical perspective.

Here we learn not only git github commands but how the workflow of git works when we actually design a software.

We will see behind the seen about git.

### Day 1 - Introduction

- Tools We are going to use to learn git.
    - Warp Terminal 
    - Git
    - Vs Code

### Day 2 - Git Init & Hidden Folder

- Git is a Software & Github is service Provider.
- Git is version control system which keep track files for changes.
- Learning Path
    - Get the basics
    - Use it daily
    - face the problem & solve the problem

- **Repo(Repository)** :- the git-enabled folder. Think of it as your project folder with a hidden .git folder inside. This repository can have branches, forks, and various commits. The main goal is that it tracks all of the versions of a project, both working and development.

- **`git status`** 
    - Show status of files which one is changed or new files & folder is added or not .

- **`git init`** -
    - Use this command one time per Project.
    - It creates `.git` hidden folder which keeps history of all files & sub-folders.

- **Commit**  
    - It is a checkpoint .(like game)
    - It saves all the changes made to files & sub-folders .
    - It makes a sanpshot of all the changes .

***Work flow of git :*** 

> Working Dir -> git add -> Stagging Area -> git commit -> git push -> Github

### Git commits and logs

- **`git add `** - move the file to stagging area.
- **`git status`** - Show tracked and untracked files.
- Stagging area is an intermediate zone before making any commit.
- **`git rm -cached <file>`** - unstage the file.
- `git commit` - commit needs a message , reason to commit the file.
- `git commit -m "<msg>"`

**Stage Area**
    - `git init`
    - create file or files
    - git add `file1` `file2` || git add .
    - `git status`

**Commit**
    - `git commit -m "a good descriptive message"`
    - `git status`
    - Repeat two three times
    - `git log` -> gives commit id , Author , Date , commit msg
    - `git log --oneline` -> shorter and in one line 

**Atomic Commits**
- Keep commit centric to `one feature` , one component or one fix. Focused one one thing.
- `Present of Past` commit message
    - Depends {Present tense , Imperative}
    - give order to code base.
    - Don't care.

- git config --global   



