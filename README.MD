<h1>Exercise 1 </h1>

```
$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint: 	git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint: 	git branch -m <name>
Initialized empty Git repository in /home/green/Desktop/Magnun Opus/theGym/gate1/git practice/excer1/bunndle1/.git/

$ git branch -m main

$ touch index.html README.MD

$ git add .

$ git commit -m "first commit"
[main (root-commit) 1296a4e] first commit
 2 files changed, 11 insertions(+)
 create mode 100644 README.MD
 create mode 100644 index.html

$ git remote add origin https://github.com/yves137/bundle1.git

$ git push -u origin main 
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 403 bytes | 403.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/yves137/bundle1.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.

$ git checkout -b dev
Switched to a new branch 'dev'

$ git checkout -b test
Switched to a new branch 'test'

$ git checkout dev 
Switched to branch 'dev'

$ git branch -d test 
Deleted branch test (was 1296a4e).

```

<h1> Exercises 2 </h1>

1
```
$ touch home.html

$ git add .

$ git commit -m "add home.html"
[main 2aab486] add home.html
 1 file changed, 11 insertions(+)
 create mode 100644 home.html

$ git stash save "save stash for home"
Saved working directory and index state On main: save stash for home

$ git add about.html 

$ git commit -m "add about.html"
[main 5b67a39] add about.html
 1 file changed, 11 insertions(+)
 create mode 100644 about.html

$ git stash save "save stash for about"
Saved working directory and index state On main: save stash for about

$ git add team.html 

$ git commit -m "add team.html"
[main 6605933] add team.html
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

$ git stash save "save stash for team"
Saved working directory and index state On main: save stash for team

$ git stash list 
stash@{0}: On main: save stash for team
stash@{1}: On main: save stash for about
stash@{2}: On main: save stash for home

$ git stash pop stash@{1} 
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   about.html

no changes added to commit (use "git add" and/or "git commit -a")
Dropped stash@{1} (c6b1091c474e6bb6dbfcf8d30946ff0c36e781d1)

$ git stash pop stash@{1} 
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   about.html
	modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")
Dropped stash@{1} (5b06b78648d0e3f3312c8cc30bfe3cc262fc2dfa)

$ git add 
about.html  home.html   

$ git add .

$ git commit -m "add stashed home and about"
[main 0df3bb9] add stashed home and about
 2 files changed, 2 insertions(+)

$ git push
Username for 'https://github.com': yves173
Password for 'https://yves173@github.com': 
Enumerating objects: 14, done.
Counting objects: 100% (14/14), done.
Delta compression using up to 4 threads
Compressing objects: 100% (13/13), done.
Writing objects: 100% (13/13), 1.36 KiB | 463.00 KiB/s, done.
Total 13 (delta 6), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (6/6), done.
To https://github.com/yves137/bundle1.git
   0ddcb1a..0df3bb9  main -> main

$ git stash pop stash@{0} 
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   team.html

no changes added to commit (use "git add" and/or "git commit -a")
Dropped stash@{0} (ddad1faec99020840738f44c296a834b99982413)

$ git log 
commit 0df3bb9a931612a5b9a1957fcd226bc0aab2441e (HEAD -> main, origin/main)
Author: yves173 <ykwizera67@gmail.com>
Date:   Tue Jul 11 12:02:27 2023 +0200

    add stashed home and about

commit 6605933737f966415e39801e9656f3f7aa35ce6d
Author: yves173 <ykwizera67@gmail.com>
Date:   Tue Jul 11 11:57:28 2023 +0200

    add team.html

commit 5b67a395cd32c3455fb9bd9dd6023389d7a79764
Author: yves173 <ykwizera67@gmail.com>
Date:   Tue Jul 11 11:55:21 2023 +0200

    add about.html

commit 2aab4869cb7da717b7493068b97083b00655c019
Author: yves173 <ykwizera67@gmail.com>
Date:   Tue Jul 11 11:51:47 2023 +0200

    add home.html
    
$ git reset HEAD^
Unstaged changes after reset:
M	about.html
M	home.html
M	team.html
$ 

```