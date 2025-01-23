1. Created new repository named FlexiSAF2 from the github.com GUI
2. Cloned FlexiSAF2 into my computer
3. Created a branch named 'local' for changes being made on my computer
4. Edited files on 'local' branch
5. Merged changes from 'local' into 'main'
6. Pushed commits to remote repository
7. Created upstream for local branch
8. Commited and reverted the 'greeting' commit
9. Made changes in remote repository and pulled those changes into my computer.
10. Renamed 'local' branch to 'new-local'

The full CLI interaction is pasted below for reference:


BASI@BASI MINGW64 ~
$ cd /c/Users/BASI/repos/bitbucketstationlocations/stationlocations
bash: cd: /c/Users/BASI/repos/bitbucketstationlocations/stationlocations: Not a directory

BASI@BASI MINGW64 ~
$ cd ~/repos/bitbucketstationlocations/stationlocations
bash: cd: /c/Users/BASI/repos/bitbucketstationlocations/stationlocations: Not a directory

BASI@BASI MINGW64 ~
$ cd ~/repos/bitbucketstationlocations/

BASI@BASI MINGW64 ~/repos/bitbucketstationlocations (future-plans)
$ git status
On branch future-plans
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   stationlocations


BASI@BASI MINGW64 ~/repos/bitbucketstationlocations (future-plans)
$ git commit -m 'making a change in a branch'
[future-plans 2c6b089] making a change in a branch
 1 file changed, 8 insertions(+), 4 deletions(-)

BASI@BASI MINGW64 ~/repos/bitbucketstationlocations (future-plans)
$ git status
On branch future-plans
nothing to commit, working tree clean

BASI@BASI MINGW64 ~/repos/bitbucketstationlocations (future-plans)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

BASI@BASI MINGW64 ~/repos/bitbucketstationlocations (main)
$ git merge future-plans
Updating 748cac3..2c6b089
Fast-forward
 stationlocations | 12 ++++++++----
 1 file changed, 8 insertions(+), 4 deletions(-)

BASI@BASI MINGW64 ~/repos/bitbucketstationlocations (main)
$ git branch -d future-plans
Deleted branch future-plans (was 2c6b089).

BASI@BASI MINGW64 ~/repos/bitbucketstationlocations (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

BASI@BASI MINGW64 ~/repos/bitbucketstationlocations (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 369 bytes | 369.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
To https://bitbucket.org/basi-1991/bitbucketstationlocations.git
   748cac3..2c6b089  main -> main

BASI@BASI MINGW64 ~/repos/bitbucketstationlocations (main)
$

BASI@BASI MINGW64 ~/repos/bitbucketstationlocations (main)
$ cd /c/Users/BASI/repos

BASI@BASI MINGW64 ~/repos
$ mkdir FlexiSAF2

BASI@BASI MINGW64 ~/repos
$ cd FlexiSAF2

BASI@BASI MINGW64 ~/repos/FlexiSAF2
$ git clone https://github.com/basii199/FlexiSAF2.git
Cloning into 'FlexiSAF2'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (6/6), done.

BASI@BASI MINGW64 ~/repos/FlexiSAF2
$ cd ~/repos

BASI@BASI MINGW64 ~/repos
$ git clone https://github.com/basii199/FlexiSAF2.git
Cloning into 'FlexiSAF2'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (6/6), done.

BASI@BASI MINGW64 ~/repos
$ cd /c/Users/BASI/repos/FlexiSAF2

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git branch local

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git checkout local
Switched to branch 'local'

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git status
On branch local
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ touch index.html

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git status
On branch local
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
Add HTML file and update readme file























[local 9cb3390] Add HTML file and update readme file
 2 files changed, 2 insertions(+)
 create mode 100644 index.html

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git status
On branch local
nothing to commit, working tree clean

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git status
On branch local
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .vscode/

no changes added to commit (use "git add" and/or "git commit -a")

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ rm-r .vscode
bash: rm-r: command not found

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git status
On branch local
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git add index.html

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git status
On branch local
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   index.html


BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git commit -m 'Adding elements to HTML file'
[local 704750d] Adding elements to HTML file
 1 file changed, 74 insertions(+)

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git merge local
Updating c0fcd92..704750d
Fast-forward
 README.md  |  2 ++
 index.html | 74 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 2 files changed, 76 insertions(+)
 create mode 100644 index.html

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git push
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 1.60 KiB | 1.60 MiB/s, done.
Total 7 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/basii199/FlexiSAF2.git
   c0fcd92..704750d  main -> main

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git checkout local
Switched to branch 'local'

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git status
On branch local
nothing to commit, working tree clean

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git push
fatal: The current branch local has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin local

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$  git push --set-upstream origin local
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'local' on GitHub by visiting:
remote:      https://github.com/basii199/FlexiSAF2/pull/new/local
remote:
To https://github.com/basii199/FlexiSAF2.git
 * [new branch]      local -> local
branch 'local' set up to track 'origin/local'.

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ echo 'How far' >> greetings.txt

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git add greetins.txt
fatal: pathspec 'greetins.txt' did not match any files

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git add greetings.txt
warning: in the working copy of 'greetings.txt', LF will be replaced by CRLF the
 next time Git touches it

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git commit -m 'Add greeting'
[main b5b03ac] Add greeting
 1 file changed, 1 insertion(+)
 create mode 100644 greetings.txt

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git push origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 322 bytes | 322.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/basii199/FlexiSAF2.git
   704750d..b5b03ac  main -> main

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git log
commit b5b03aca56693004648e60a44e5152c0165fe33f (HEAD -> main, origin/main, orig
in/HEAD)
Author: basii199 <ubokabasi135@gmail.com>
Date:   Thu Jan 23 09:57:18 2025 +0100

    Add greeting


    Add greeting

commit 704750d640c33e5ca14a105da29ba3f1c5582769 (origin/local, local)
Author: basii199 <ubokabasi135@gmail.com>
Date:   Thu Jan 23 09:46:04 2025 +0100
Revert "Add greeting"























[main cc9bf32] Revert "Add greeting"
 1 file changed, 1 deletion(-)
 delete mode 100644 greetings.txt

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 250 bytes | 250.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/basii199/FlexiSAF2.git
   b5b03ac..cc9bf32  main -> main

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 1.12 KiB | 7.00 KiB/s, done.
From https://github.com/basii199/FlexiSAF2
   cc9bf32..8f057c3  main       -> origin/main
Updating cc9bf32..8f057c3
Fast-forward
 README.md | 6 ++++++
 1 file changed, 6 insertions(+)

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git checkout local
error: Your local changes to the following files would be overwritten by checkou
t:
        README.md
Please commit your changes or stash them before you switch branches.
Aborting

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git add index.html

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git commit -m 'Pull request'
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git add .

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git commit -m 'Pull request'
[main 0662f10] Pull request
 1 file changed, 1 insertion(+), 1 deletion(-)

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git checkout local
Switched to branch 'local'
Your branch is up to date with 'origin/local'.

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (local)
$ git branch -m new-local

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (new-local)
$ git status
On branch new-local
Your branch is up to date with 'origin/local'.

nothing to commit, working tree clean

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (new-local)
$ git pull
Already up to date.

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (new-local)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git checkout new-local
error: Your local changes to the following files would be overwritten by checkou
t:
        README.md
Please commit your changes or stash them before you switch branches.
Aborting

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git add .

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git commit -m 'Update'
[main 8785f64] Update
 1 file changed, 1 insertion(+)

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git checkout new-local
Switched to branch 'new-local'
Your branch is up to date with 'origin/local'.

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (new-local)
$ git pull origin main
From https://github.com/basii199/FlexiSAF2
 * branch            main       -> FETCH_HEAD
Updating 704750d..8f057c3
Fast-forward
 README.md | 6 ++++++
 1 file changed, 6 insertions(+)

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (new-local)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git push origin main
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 657 bytes | 328.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/basii199/FlexiSAF2.git
   8f057c3..8785f64  main -> main

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (main)
$ git checkout new-local
Switched to branch 'new-local'
Your branch is ahead of 'origin/local' by 3 commits.
  (use "git push" to publish your local commits)

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (new-local)
$ git pull origin main
From https://github.com/basii199/FlexiSAF2
 * branch            main       -> FETCH_HEAD
Updating 8f057c3..8785f64
Fast-forward
 README.md | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (new-local)
$ git status
On branch new-local
Your branch is ahead of 'origin/local' by 5 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (new-local)
$ git push
fatal: The upstream branch of your current branch does not match
the name of your current branch.  To push to the upstream branch
on the remote, use

    git push origin HEAD:local

To push to the branch of the same name on the remote, use

    git push origin HEAD

To choose either option permanently, see push.default in 'git help config'.

To avoid automatically configuring an upstream branch when its name
won't match the local branch, see option 'simple' of branch.autoSetupMerge
in 'git help config'.


BASI@BASI MINGW64 ~/repos/FlexiSAF2 (new-local)
$ git push origin HEAD
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'new-local' on GitHub by visiting:
remote:      https://github.com/basii199/FlexiSAF2/pull/new/new-local
remote:
To https://github.com/basii199/FlexiSAF2.git
 * [new branch]      HEAD -> new-local

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (new-local)
$ git push origin --delete local
To https://github.com/basii199/FlexiSAF2.git
 - [deleted]         local

BASI@BASI MINGW64 ~/repos/FlexiSAF2 (new-local)
$
