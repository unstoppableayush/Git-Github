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

- **Stage Area**
    - `git init`
    - create file or files
    - git add `file1` `file2` || git add .
    - `git status`

- **Commit**
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

### Git internal working and configs

- `git config --global code.editor "code --wait` -> changes default editor to vs code.

- There are two ways to configure configuration fils
    1. Global
    2. Local

- Set a Git username : `git config --global user.name "<username>"`
- Set a Git email : `git config --global user.email "<email>"`

- `.gitignore`
    - Don't track some files & folders
    - node modules , API Key, Secret
    - get template online , pattern can be tricky

- **Commit behinde the scene**
    - In the world of git every commit is depneded on previous commit.
    - Every commit has hash value and info about parent commit 

### Git merge and git conflicts

- **Branches**
    - Like an alternative timeline.
    - You are always on some branch.
    - Create new : `git branch <BRANCH_NAME>`
    - Switch to other Branch : `git checkout <BRANCH_NAME>`
    - Check current branch : `git branch`
    - Create a branch & move there : `git switch -c <BRANCH_NAME>` , `git switch -c <BRANCH_NAME>`
    - commit before switching to another branch
    - go to .git folder & checkout HEAD file

- **HEAD**
    - Head points to where a branch is currently at

- **Merging the branches**
    1. Fast Forward Merge
        - `git switch master` & `git merge bugfix`
        -  Git will move the `master `branch pointer to the latest commit on the `bugfix` branch without creating a merge commit.
        - Possible only if there is no divergence between branches.
    
    2. Not Fast Forward Merge
        - `git switch master` & `git merge --no-ff bugfix`
        - Merge the `bugfix` branch into `master` with a merge commit.

    - Git Tries best to resolve conflicts
        - Above ===== represents the `master` branch changes.
        - Below ===== represents the `other` branch changes.
        - Keep whatever you want , remove markers & save.