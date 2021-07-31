# commands of Git/github

### git add

1. git add . (Adds **all files** to staging phase, doesn't check deleted)

   1. git add -A (Add **all files** to staging and check **DELETED** files)
   2. git add -u (Stages only modified files and check **DELETED** files)

    <hr>

### git commit

2. git commit (commit the staged files and make snap of changes)<hr>

### git status

3. git status (checks status of staged/changed files)<hr>

### git diff

4. git diff <-options->
   1. git diff (shows diff between **_working tree_** and the **_staged_** file)
   2. git diff --staged (shows diff between **_commited_** and **_staged_** file)
   3. git diff HEAD (shows diff between **comitted** and **working tree**)
   4. git diff <-options-> --word-diff (show which **_words changed exactly_**)
   5. git diff <-options-> --color-words (show which **_words changed exactly)_**
   6. git diff --stat (shows summary on general changes in files)
   <hr>

### git log

5. git log (shows **_complete_** log of commits done)
   1. git log --oneline (shows **_summary_** log of commits done)
   2. git log --stat (shows complete log of commits with **_files details_**)
   3. git log --patch (shows complete log of commits with _files details_ **_AND_** _changes_ on each file)
   4. git log --graph (shows complete log with **_file structure_** main/branches )
      1. git log --graph --oneline --all --decorate (the video recommended that way)
   5. git log --stat -M --follow -- <-file path-> (shows log of **Specific file** even across moves: `-M --follow`)
   <hr>

### git remove

6. git rm <-filename-> (deleted named file from **WHOLE** system)
   1. git rm --cached (remove tracing the file but **LEAVE** it in system)
   <hr>

### git move

7. git mv <-old path-> <-new path-> (moves the named file to other location with diff name if needed: `git mv myPic.jpg imgs/pic1.png`)

   1. Easier to use explorer to move and delete then use `$git add -A .`
   <hr>

### git branch

8.  git branch (Show all branches)

    1. git branch <-branch name-> (Creates new branch with provided name)
    1. git checkout -b <-branch name-> (Creates new branch and switch to it)
    1. git branch -d <-name-> (Deletes the branch)
    1. git checkout <-name-> (switch to diff branch to work on)
    1. git checkout -- <-file-name-> (replace that file with same from last commit)
    1. git checkout <638ee7> <-newName-> (grab that file from history with <-specified hash-> and rename it then puts it in current working space)
    <hr>

### git merge

9. git merge <-name-> (Follow steps below 1~4)
   1. git checkout <-name-> (Navigate to the branch u will merge into)
   2. git branch (To see all branch names)
   3. git merge <-name-> (merge the named branch into the branch u checked into in step1)
   4. git branch -d <-name-> (Delete the branch that was merged because it's a duplicate now)
10. If u got merge conflict u need to use (git status) to see what is causing the conflict, solve it manually, then (git add fileName) and finally (git commit)
    1. If u want to abort and solve conflict later (git merge --abort)
11. git merge --squash <-target branch-> (merge branches and use target branch history only: `Wont merge both history(commits)`)<hr>

### git remote

12. git remote (Send and recieve data from url aka `github`)
    1. git remote add origin <-github url-> (Add origin to github.com?)
    2. git remote set-url origin <-other github url-> (Changes the github url)
    3. git remote rm origin (Removes the remote from github)
    4. git remote -v (Shows the urls in the working space)
13. git fetch origin (Goes to github and fetch)
14. git pull origin (combo of fetch/merge: `it goes to github, fetch data, and merge github branch with the one currently we checked into`)
15. git push origin (Pushes the data to github from PC)<hr>

### git reset [Examples](https://devconnected.com/how-to-undo-last-git-commit/)

16. git reset HEAD <-fileName-> (go back in history the default `1 log` and unstage files in that commit **WITHOUT** modifying working space)
    1. git reset --soft HEAD~5 (go back in history 5 log commits **WITHOUT** changing files modified in them in working space)
    1. git reset --hard HEAD~3 (go back in history 3 commits and **DELETE** the changes made in these commits from working space and staging~`CAREFUL`~)
    1. git revert HEAD (Sees what was that commit in history `HEAD` and makes a new commit at end of log which is before it)
    1. git checkout <638ee7> <-newName-> (grab that file from history with <-specified hash-> and rename it then puts it in current working space)
    <hr>

### git reflog

17. git reflog (Shows a log with **EVERYTHING** including checkouts/resets/merging... so u can reset to specific position in history)

1. gitk (Need further search, but it's used to show graphical log)<hr>

### git rebase

19. git rebase <-master-> (Move the whole **`checked in`** branch with its history after latest commit in the target branch: master in this case)
    1. git checkout <-branch-> (use it first)
    <hr>

### git ignore

16. git ls-files --others --ignored --exclude-standard (to see ignored files from .gitignore)<hr>
