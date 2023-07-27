<h1 id="bundle1">Exercise 1 </h1>

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



<h1 id="bundle2">Bundle 2</h1>

<h2>Exercises 1</h2>

```
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

$ git add services.html 

$ git commit -m "add service.html"
[ft/bundle-2 1ae4391] add service.html
 1 file changed, 11 insertions(+)
 create mode 100644 services.html

$ git push -u origin ft/bundle-2
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 426 bytes | 213.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/yves137/bundle1/pull/new/ft/bundle-2
remote: 
To https://github.com/yves137/bundle1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
Branch 'ft/bundle-2' set up to track remote branch 'ft/bundle-2' from 'origin'.

```

<h2>Exercises 2</h2>

```
$ git checkout main 
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

$ git pull
Already up to date.

$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

$ git add services.html

$ git commit -m "update service.html"
[ft/service-redesign 06d1e17] update service.html
 1 file changed, 12 insertions(+)
 create mode 100644 services.html

$ git push -u origin ft/service-redesign
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 452 bytes | 452.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/yves137/bundle1/pull/new/ft/service-redesign
remote: 
To https://github.com/yves137/bundle1.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
Branch 'ft/service-redesign' set up to track remote branch 'ft/service-redesign' from 'origin'.

$ git checkout main 
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

$ git add services.html 

$ git commit -m "service changes on main branh"
[main 962a1b3] service changes on main branh
 1 file changed, 12 insertions(+)
 create mode 100644 services.html

$ git push
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 467 bytes | 116.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/yves137/bundle1.git
   9c60637..962a1b3  main -> main

$ git checkout ft/service-redesign 
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

$ git diff main 
diff --git a/services.html b/services.html
index 7a413ee..70528f9 100644
--- a/services.html
+++ b/services.html
@@ -7,6 +7,6 @@
 </head>
 <body>
     <h1>Service</h1>
-    <p>some update on bundle 2-1 in main branch</p>
+    <p>some update on bundle 2-1</p>
 </body>
 </html>
\ No newline at end of file

$ git merge main
Auto-merging services.html
CONFLICT (add/add): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.
  
$ git add .

$ git commit -m "ft/service with main"
[ft/service-redesign 0edeca3] ft/service with main
   
$ git push
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 218 bytes | 218.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/yves137/bundle1.git
   06d1e17..0edeca3  ft/service-redesign -> ft/service-redesign


```

<h1 id="bundle3"> Bundle 3</h1>

<h2>Exercise 1</h2>

```
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

$ git add team.html 

$ git commit -m "add changes on team.html bundle3-1"
[ft/team-page 2ac45fc] add changes on team.html bundle3-1
 1 file changed, 1 insertion(+)

$ git push -u origin ft/team-page 
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 349 bytes | 116.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/yves137/bundle1/pull/new/ft/team-page
remote: 
To https://github.com/yves137/bundle1.git
 * [new branch]      ft/team-page -> ft/team-page
Branch 'ft/team-page' set up to track remote branch 'ft/team-page' from 'origin'.

$ git checkout main 
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

$ git log 
commit 2ac45fc12eadd1fd2667af4f1d211f643e1bd96b (HEAD -> ft/team-page, origin/ft/team-page)
Author: yves173 <ykwizera67@gmail.com>
Date:   Wed Jul 26 15:34:11 2023 +0200

    add changes on team.html bundle3-1

commit eb4dc206d3292745f7e814a4ff7241e2395e8b1c (origin/main, main, ft/contact-page)
Author: yves173 <ykwizera67@gmail.com>
Date:   Tue Jul 25 12:08:46 2023 +0200

    update read me

commit 962a1b316c30596100755fb4bd8244db5f69da20
Author: yves173 <ykwizera67@gmail.com>
Date:   Tue Jul 25 11:34:52 2023 +0200

    service changes on main branh

commit 9c60637871922d60827ae713fcc43967d2b1eec4
Author: yves173 <ykwizera67@gmail.com>

$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

$ git cherry-pick 2ac45fc12eadd1fd2667af4f1d211f643e1bd96b[ft/contact-page 4dda910] add changes on team.html bundle3-1
 Date: Wed Jul 26 15:34:11 2023 +0200
 1 file changed, 1 insertion(+)

$ git add contact.html

$ git commit -m "create and add content on contact.htm"
[ft/contact-page cc5bfdc] create and add content on contact.htm
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

$ git push -u origin ft/contact-page 
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 781 bytes | 781.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/yves137/bundle1/pull/new/ft/contact-page
remote: 
To https://github.com/yves137/bundle1.git
 * [new branch]      ft/contact-page -> ft/contact-page
Branch 'ft/contact-page' set up to track remote branch 'ft/contact-page' from 'origin'.

$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

$ git add faq.html

$ git commit -m "create and add content on faq.html"
[ft/faq-page a43a738] create and add content on faq.html
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

$ git push -u origin ft/faq-page 
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 436 bytes | 436.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/yves137/bundle1/pull/new/ft/faq-page
remote: 
To https://github.com/yves137/bundle1.git
 * [new branch]      ft/faq-page -> ft/faq-page
Branch 'ft/faq-page' set up to track remote branch 'ft/faq-page' from 'origin'.

$ git revert 2ac45fc12eadd1fd2667af4f1d211f643e1bd96b
[ft/faq-page 9aee5a7] Revert "add changes on team.html bundle3-1"
 1 file changed, 1 deletion(-)

$ git add .

$ git commit -m "commit after revert on faq"
On branch ft/faq-page
Your branch is ahead of 'origin/ft/faq-page' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

$ git push -u origin ft/faq-page 
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 360 bytes | 360.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/yves137/bundle1.git
   a43a738..9aee5a7  ft/faq-page -> ft/faq-page
Branch 'ft/faq-page' set up to track remote branch 'ft/faq-page' from 'origin'.
```

<h2>Exercise 2</h2>

```
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

$ git checkout main 
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

$ git add index.html 

$ git commit -m "update context to index.html"
[main 0dbd0e9] update context to index.html
 1 file changed, 1 insertion(+)

$ git push 
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 324 bytes | 162.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/yves137/bundle1.git
   eb4dc20..0dbd0e9  main -> main

$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

$ git rebase main 
Successfully rebased and updated refs/heads/ft/home-page-redesign.

$ git add home.html

$ git commit -m "update home.html"
[ft/home-page-redesign 498d755] update home.html
 1 file changed, 1 insertion(+)

$ git push -u origin ft/home-page-redesign 
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 17, done.
Counting objects: 100% (17/17), done.
Delta compression using up to 4 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.56 KiB | 199.00 KiB/s, done.
Total 14 (delta 8), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (8/8), completed with 3 local objects.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/yves137/bundle1/pull/new/ft/home-page-redesign
remote: 
To https://github.com/yves137/bundle1.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
Branch 'ft/home-page-redesign' set up to track remote branch 'ft/home-page-redesign' from 'origin'.
```

<h1 id="bundle4"> Bundle 4</h1>

<h2>Exercise 1</h2>

```
$ git checkout main 
Already on 'main'
Your branch is up to date with 'origin/main'.

$ git remote add git-copy https://github.com/yves137/bundle1cp.git

$ git add home.html 

$ git commit -m "Added new changes to home.html"
[main 8a28c53] Added new changes to home.html
 1 file changed, 1 insertion(+)

$ git push origin main 
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 332 bytes | 166.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/yves137/bundle1.git
   95ae8b9..8a28c53  main -> main

$ git push git-copy main 
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 48, done.
Counting objects: 100% (48/48), done.
Delta compression using up to 4 threads
Compressing objects: 100% (47/47), done.
Writing objects: 100% (48/48), 7.65 KiB | 783.00 KiB/s, done.
Total 48 (delta 26), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (26/26), done.
To https://github.com/yves137/bundle1cp.git
 * [new branch]      main -> main

```

<h2>Exercise 2</h2>

```
$ git checkout -b ft/footer
Switched to a new branch 'ft/footer'

$ git add footer.html 

$ git commit -m "added footer.html"
[ft/footer 81a4004] added footer.html
 1 file changed, 11 insertions(+)
 create mode 100644 footer.html

$ git add footer.html 

$ git commit -m "added more changesto footer.html"
[ft/footer 2645716] added more changesto footer.html
 1 file changed, 1 insertion(+)

$ git push origin ft/footer 
Username for 'https://github.com': yves137
Password for 'https://yves137@github.com': 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 717 bytes | 179.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/footer' on GitHub by visiting:
remote:      https://github.com/yves137/bundle1/pull/new/ft/footer
remote: 
To https://github.com/yves137/bundle1.git
 * [new branch]      ft/footer -> ft/footer

$ git checkout main 
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

$ git checkout -b ft/squashing
Switched to a new branch 'ft/squashing'

$ git merge --squash ft/footer 
Updating 8a28c53..2645716
Fast-forward
Squash commit -- not updating HEAD
 footer.html | 12 ++++++++++++
 1 file changed, 12 insertions(+)
 create mode 100644 footer.html

$ git status 
On branch ft/squashing
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   footer.html
   
$ git add footer.html 

$ git commit -m "footer changes squashing"
[ft/squashing 236fb36] footer changes squashing
 1 file changed, 12 insertions(+)
 create mode 100644 footer.html

$ git push origin ft/squashing 
yUsername for 'https://github.com': yves137
Password for 'https://yyves137@github.com': 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 450 bytes | 450.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/squashing' on GitHub by visiting:
remote:      https://github.com/yves137/bundle1/pull/new/ft/squashing
remote: 
To https://github.com/yves137/bundle1.git
 * [new branch]      ft/squashing -> ft/squashing

```