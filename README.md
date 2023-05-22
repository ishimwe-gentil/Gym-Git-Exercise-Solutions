
# Git exercise project

This project will be used for a series of git exercises

## Bundle 1

### Exercise 1

```powershell
Initialized empty Git repository in C:/Users/gentil/gym-git-exercise/.git/
PS C:\Users\gentil\gym-git-exercise> git status
On branch master

No commits yet

PS C:\Users\gentil\gym-git-exercise> git branch -M main       
PS C:\Users\gentil\gym-git-exercise> git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\gentil\gym-git-exercise> git remote add origin https://github.com/ishimwe-gentil/Gym-Git-Exercise-Solutions.git
PS C:\Users\gentil\gym-git-exercise> git push -u origin main
error: src refspec main does not match any
PS C:\Users\gentil\gym-git-exercise>  git add README.md
PS C:\Users\gentil\gym-git-exercise> git status
On branch main
No commits yet
Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md

PS C:\Users\gentil\gym-git-exercise> git commit -m "init project"
[main (root-commit) 0a294f0] init project
 1 file changed, 4 insertions(+)
 create mode 100644 README.md
error: remote origin already exists.
PS C:\Users\gentil\gym-git-exercise> git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
PS C:\Users\gentil\gym-git-exercise> git push --set-upstream origin main
Delta compression using up to 4 threads
Writing objects: 100% (3/3), 282 bytes | 282.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\gentil\gym-git-exercise> git push
Everything up-to-date
PS C:\Users\gentil\gym-git-exercise> git branch dev
PS C:\Users\gentil\gym-git-exercise> git switch dev
Switched to branch 'dev'
PS C:\Users\gentil\gym-git-exercise> git status
nothing to commit, working tree clean
PS C:\Users\gentil\gym-git-exercise> git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking

remote:
remote:      https://github.com/ishimwe-gentil/Gym-Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/ishimwe-gentil/Gym-Git-Exercise-Solutions.git
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.
PS C:\Users\gentil\gym-git-exercise> git push
Everything up-to-date
PS C:\Users\gentil\gym-git-exercise> git branch test
Switched to branch 'test'
remote:
remote: Create a pull request for 'test' on GitHub by visiting:
remote:
To https://github.com/ishimwe-gentil/Gym-Git-Exercise-Solutions.git
branch 'test' set up to track 'origin/test'.
Everything up-to-date
PS C:\Users\gentil\gym-git-exercise>
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.
PS C:\Users\gentil\gym-git-exercise> git push --set-upstream origin dev 
Everything up-to-date
PS C:\Users\gentil\gym-git-exercise> git branch -d test
Deleted branch test (was 0a294f0).
PS C:\Users\gentil\gym-git-exercise> git push --set-upstream origin dev
Everything up-to-date
branch 'dev' set up to track 'origin/dev'.
PS C:\Users\gentil\gym-git-exercise> git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean
PS C:\Users\gentil\gym-git-exercise> git push origin --delete test
To https://github.com/ishimwe-gentil/Gym-Git-Exercise-Solutions.git
 - [deleted]         test
PS C:\Users\gentil\gym-git-exercise>
```

### Exercise 2
```powershell
PS C:\Users\gentil\gym-git-exercise> git switch dev
PS C:\Users\gentil\gym-git-exercise> git stash list
PS C:\Users\gentil\gym-git-exercise> git status

  (use "git restore --staged <file>..." to unstage)
        new file:   home.html
PS C:\Users\gentil\gym-git-exercise> git stash
Saved working directory and index state WIP on dev: 0a294f0 init project
PS C:\Users\gentil\gym-git-exercise> git stash list
stash@{0}: WIP on dev: 0a294f0 init project
PS C:\Users\gentil\gym-git-exercise> git add about.html
PS C:\Users\gentil\gym-git-exercise> git stash
Saved working directory and index state WIP on dev: 0a294f0 init project
PS C:\Users\gentil\gym-git-exercise> git stash list    
PS C:\Users\gentil\gym-git-exercise> git status
Your branch is up to date with 'origin/dev'.

Untracked files:
        team.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\gentil\gym-git-exercise> git add team.html
PS C:\Users\gentil\gym-git-exercise> git stash
Saved working directory and index state WIP on dev: 0a294f0 init project
PS C:\Users\gentil\gym-git-exercise> git stash list
stash@{0}: WIP on dev: 0a294f0 init project
PS C:\Users\gentil\gym-git-exercise> git stash pop
Your branch is up to date with 'origin/dev'.

Changes to be committed:
        new file:   team.html

Dropped refs/stash@{0} (0f4ce5cc2b330a48dd0fc74edd5a41f92889c195)
PS C:\Users\gentil\gym-git-exercise> git add team.html
PS C:\Users\gentil\gym-git-exercise> git stash
Saved working directory and index state WIP on dev: 0a294f0 init project
stash@{0}: WIP on dev: 0a294f0 init project
stash@{1}: WIP on dev: 0a294f0 init project
stash@{2}: WIP on dev: 0a294f0 init project
PS C:\Users\gentil\gym-git-exercise> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --quiet           be quiet, only report errors

PS C:\Users\gentil\gym-git-exercise> git stash pop stash@`{1`}
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (ad2cbf37ae996ed2effd0e56a03a1fd3434a67cc)
PS C:\Users\gentil\gym-git-exercise> git stash list
stash@{0}: WIP on dev: 0a294f0 init project
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

PS C:\Users\gentil\gym-git-exercise> git add --all
PS C:\Users\gentil\gym-git-exercise> git status
On branch dev
Your branch is up to date with 'origin/dev'.
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

PS C:\Users\gentil\gym-git-exercise> git commit -a -m "restoring both home and about pages"
[dev fdf899a] restoring both home and about pages
 2 files changed, 41 insertions(+)
 create mode 100644 home.html
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 781 bytes | 390.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/ishimwe-gentil/Gym-Git-Exercise-Solutions.git
   0a294f0..fdf899a  dev -> dev
stash@{0}: WIP on dev: 0a294f0 init project
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
        new file:   team.html

Dropped stash@{0} (034a8469f80c4ebc2193759a8632cbc383d0a1ef)
PS C:\Users\gentil\gym-git-exercise> git reset --hard
HEAD is now at fdf899a restoring both home and about pages
PS C:\Users\gentil\gym-git-exercise> git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean
PS C:\Users\gentil\gym-git-exercise> git stash list
PS C:\Users\gentil\gym-git-exercise> 
```