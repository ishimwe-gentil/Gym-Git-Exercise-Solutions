
# Git exercise project

This project will be used for a series of git exercises

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