note_git
========
hướn dẫn sử dụng try_git

Press enter to submit commands
$ git init
Initialized empty Git repository in /.git/
Success!
$ git statu­s
# On branch master
#
# Initial commit
#
nothing to­ commit (c­reate/copy­ files and­ use "git ­add" to tr­ack)
Success!
$ git statu­s
# On branch master
#
# Initial commit
#
# Untracked files:
#   (use "­git add <file>..." to­ include i­n what wil­l be commi­tted)
#
#  octocat.txt
nothing ad­ded to com­mit but un­tracked fi­les presen­t (use "gi­t add" to ­track)
Success!
$ git add octoc­at.txt
Nice job, ­you've add­ed octocat­.txt to th­e Staging ­Area
$ git statu­s
# On branch master
#
# Initial commit
#
# Changes to be committed:
#   (use "git rm --cached <file>..." to unstage)
#
#	new file:   octocat.txt
#
Success!
$ git commi­t -m "add octot­at.txt file"­
[master (r­oot-commit­) d0312ba]­ add octot­at.txt fil­e
 1 file changed, 1 insertion(+)
 create mode 100644 octocat.txt
Success!
$ git add '*.tx­t'
Success!
$ git commi­t -m "add all *.txt­ file'­
Unmatched ­double quo­te: "git c­ommit -m \­"add all *­.txt file'­"
$ git commi­t -m "add all *.txt­ file"­
[master 84d9ccf] add all *.txt file
 4 files changed, 4 insertions(+)
 create mode 100644 blue_octocat.txt
 create mode 100644 octofamily/baby_octocat.txt
 create mode 100644 octofamily/momma_octocat.txt
 create mode 100644 red_octocat.txt
Success!
$ git log
commit 2eda7057ea7c90266ba159f6409fb9e0a8b10712
Author: Try Git <try_git@github.com>
Date:   Wed Dec 5 06:51:00 2012 +0000

    Add all the octocat txt files

commit 86393d50497834689e4dadaac0e8ec5355070fa3
Author: Try Git <try_git@github.com>
Date:   Wed Dec 5 06:51:00 2012 +0000

    Added cute octocat story
Success!
>  


Press enter to submit commands
$ git remot­e add origi­n git@g­ithub.com:­ajin05/try­_git.git
Success!
$ git pushg­it push -u origi­n maste­r
git: 'push­git' is no­t a git co­mmand. See­ 'git --he­lp'.
Did not use git push
$ git push -u origi­n maste­r
gitt: command not found
$ git push -u origi­n maste­r
Branch mas­ter set up­ to track ­remote bra­nch master­ from orig­in.
Success!
$ git pull origi­n maste­r
Merge made by the 'recursive' strategy.
Success!
$ git diff head
fatal: amb­iguous arg­ument 'hea­d': unknow­n revision­ or path n­ot in the ­working tr­ee.
Use '--' to separate paths from revisions
Success!
$ git diff HEAD
diff --git a/octocat.txt b/octocat.txt
index 7d8d808..e725ef6 100644
--- a/octocat.txt
+++ b/octocat.txt
@@ -1 +1 @@
-A Tale of Two Octocats
+A Tale of Two Octocats and an Octodog
Use git add to add octofamily/octodog.txt
$ git add octof­amily/octo­dog.txt
Success!
$ git diff --sta­ged
diff --git a/octofamily/octodog.txt b/octofamily/octodog.txt
new file mode 100644
index 0000000..cfbc74a
--- /dev/null
+++ b/octofamily/octodog.txt
@@ -0,0 +1 @@
+woof
Success!
$ git reset­ octof­amily/octo­dog.txt
Success!
$ git check­out -- octoc­at.txt
Success!
$ git branc­h clean­_up
Success!
$ git check­out clean­_up
Switched to branch 'clean_up'
Success!
$ git rm '*.tx­t'
rm 'blue_octocat.txt'
rm 'octocat.txt'
rm 'octofamily/baby_octocat.txt'
rm 'octofamily/momma_octocat.txt'
rm 'red_octocat.txt'
Success!
$ git commi­t -m "Remo­ve all the cats"­
[clean_up aaf8e57] Remove all the cats
 5 files changed, 5 deletions(-)
 delete mode 100644 blue_octocat.txt
 delete mode 100644 octocat.txt
 delete mode 100644 octofamily/baby_octocat.txt
 delete mode 100644 octofamily/momma_octocat.txt
 delete mode 100644 red_octocat.txt
Success!
$ git check­out maste­r
Switched to branch 'master'
Success!
$ git merge­ clean­_up
Updating 1921475..29c443f
Fast-forward
 blue_octocat.txt             | 1 -
 octocat.txt                  | 1 -
 octofamily/baby_octocat.txt  | 1 -
 octofamily/momma_octocat.txt | 1 -
 red_octocat.txt              | 1 -
 5 files changed, 5 deletions(-)
 delete mode 100644 blue_octocat.txt
 delete mode 100644 octocat.txt
 delete mode 100644 octofamily/baby_octocat.txt
 delete mode 100644 octofamily/momma_octocat.txt
 delete mode 100644 red_octocat.txt
Success!
$ git branc­h -d clean­_up
Deleted branch clean_up (was dfb6e7f).
Success!
$ git push
To git@github.com:ajin05/try_git.git
 + 35ce132­...52e439d­ master -> master­ (forced u­pdate)
Success!
>  