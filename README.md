# git_tutorials


git status
On branch master

No commits yet

Untracked files: ( Not tracking by git this file is available in OS)
  (use "git add <file>..." to include in what will be committed)
        file1.txt
		
		
Now we have to move the file from untracked to staging area

git add file.txt

git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   file1.txt
		
		
commit the changes from Staging area to git repo

git commit -m "added a new file"


git status
On branch master
nothing to commit, working tree clean

Whenever we want git to track file we should follow 2 step process
1. Staging the file using git add <file_name>
2.commit the changes using git commit -m ""


git log
commit c2d67ecad55f4e4e09764da7a635290917235b49 (HEAD -> master)
Author: Althaf <althaf@gmail.com>
Date:   Wed May 7 06:17:22 2025 +0000

    this is file2

commit 7851f447d765c3229622347f498eef18824be3ab
Author: Althaf <althaf@gmail.com>
Date:   Wed May 7 06:13:57 2025 +0000

Whenever we change the content inside the file which is already in git repo we have to add and commit if we want that changes to track.

.gitignore -if we don't want to track any file
1. Create a .gitignore file
2. Put the name of the file inside .gitignore



Git branching:

1. Create branch ( from main/master)
2. Apply fix/upgrdes
3. Merge with master/main.


Merging:

scenario 1: 8AM I have created a feature baranch from master > All the files from master are copied to feature barnch > 9AM I planned to merge changes to main.

During 8 AM to 9 AM not changes happened at master branch so, it is called fast forward merge.

SCenario 2: During the same interval many commits are happening at master branch it is called three way merge



To add remote repo:

git remote add origin "githubrepourl"  > git remote add <local_name> <path of remote repo >

origin means any name 


git remote -v
ubuntu@ip-172-31-11-191:~/github$ git remote add devops_project https://github.com/shaikaltaf1/git-practice.git
ubuntu@ip-172-31-11-191:~/github$ git remote -v
devops_project  https://github.com/shaikaltaf1/git-practice.git (fetch)
devops_project  https://github.com/shaikaltaf1/git-practice.git (pushh)




3  mkdir ass4
    4  cd ass4
    5  git init
    6  git config --global user.name "Althaf"
    7  git config --global user.email "Althaf@gmail.com"
    8  git init
    9  git log
   10  git branch
   11  touch master.txt
   12  git status
   13  git add .
   14  git commit -m "master file"
   15  git status
   16  git branch
   17  create branch public1 public2 private
   18  git branch public1 public2 private
   19  git branch public1
   20  git branch public2
   21  git branch private
   22  git branch
   23  git checkout public1
   24  echo "content in public1 branch" > public.txt
   25  ls
   26  git checkout master
   27  ls
   28  git branch
   29  git branch public1
   30  git checkout public1
   31  git status
   32  git add .
   33  git commit -m " this is public branch file"
   34  git status
   35  git checkout master
   36  ls
   37  git merge
   38  git remote add origin https://github.com/shaikaltaf1/git-practice.git
   39  git merge
   40  git remote add origin "https://github.com/shaikaltaf1/git-practice.git"
   41  git remote 0v
   42  git remote -v
   43  git merge
   44  git branch -M main
   45  git branch
   46  ls
   47  git merge
   48  git merge public1 main
   49  ls
   50  git branch -M master
   51  git branch
   52  git merge public2
   53  ls
   54  git checkout private
   55  ls
   56  vi master.txt
   57  git add master.txt
   58  git commit -m "commting master in private brnch"
   59  git status
   60  cat master.txt
   61  git checkout public1
   62  get merge private
   63  git merge private
   64  ls
   65  git branch
   66  cat master.txt
   67  git checkout public2
   68  git merge private
   69  ls
   70  cat master.txt
   71  git checkout master
   72  cat master.txt
   73  git merge private
   74  cat master.txt
