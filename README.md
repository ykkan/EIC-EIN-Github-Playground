# EIC-EIN-Github-Playground

This repository is a **playground for simulating a Git/GitHub workflow** for lattice development.  
It walks you through the following steps:
1. Clone the repository  
2. Create a branch for development  
3. Develop the lattice (simplified as just creating a new file)
4. Commit the changes  
5. Push the development branch to the remote repository  
6. Create a pull request  
7. Address reviewer feedback and update the branch

## Scenario
This repository contains lattice files for an accelerator ring.  
Currently, two beam lines are stored in `line_a.txt` and `line_b.txt`.

Your task is to develop an additional beam line and add it to the repository.

## Clone the repository
Your work will build on the existing lattice. To get started, you need to obtain a local copy of this repository by running:
```
> git clone git@github.com:ykkan/EIC-EIN-Github-Playground.git
```
Once done, you should see a copy of this repository in your current directory:
```text
> ls
EIC-EIN-Github-Playground
```

## Create a branch for development
Move into the directory. You can check your current branch by typing:
```
> git branch
* main
```
Instead of working directly on the `main` branch, a common practice is to create a new branch and carry out further development there. This approach separates ongoing development from the main branch, allowing you to always return to a stable baseline. Therefore, we can create a new branch named `line_{your-github-username}`:
```
> git branch line_ykkan
```
At this point, we are still on the main branch:
```
> git branch
  line_ykkan
* main
```
To start working on the new branch, switch to `dev` using:
```
> git checkout dev
Switched to branch 'dev'
```

## Develop the lattice
You start to develope your beam line and store it in a file named `line_{your-github-username}.txt`. Please create an empty file named `line_{your-github-username}.txt`.

## Commit the changes
So far, the modifications you made are not yet tracked by Git:
```
> 
git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   ring.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        line_ykkan.txt
```
To allow Git to track your changes, you need to add them to the staging area and then commit:

## Push the development branch
Now, you wan to requst merging your new feature to the main branch in the remote repository. Before doing so, you first need to push your branch to the remote repositroy:
```
> git push origin line_ykkan
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 10 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 270 bytes | 270.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'line_ykkan' on GitHub by visiting:
remote:      https://github.com/ykkan/EIC-EIN-Github-Playground/pull/new/line_ykkan
remote:
To github.com:ykkan/EIC-EIN-Github-Playground.git
 * [new branch]      line_ykkan -> line_ykkan
```

## Create a pull request (PR) 
Your branch is now available on the remote repository, so you can create a pull request on GitHub

## Address reviewer feedback and update the branch
The team has decided that all newly added lattices should use the `.lat` file extension. Therefore, in the PR, the reviewer has requested that you make this change.
