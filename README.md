# hello-world

Learning what is Github

git start

Adding new lines :)

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

8.  git branch <-name-> (Creates new branch with provided name)

    1. git branch -d <-name-> (Deletes the branch)
    2. git checkout <-name-> (switch to diff branch to work on)

    <hr>

### git ignore

9. git ls-files --others --ignored --exclude-standard (to see ignored files from .gitignore)<hr>
