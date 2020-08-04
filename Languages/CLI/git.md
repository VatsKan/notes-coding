# Git notes

[git rebasing reference](https://www.git-tower.com/learn/git/ebook/en/desktop-gui/advanced-topics/rebase#start)

## commands

- ```git reset <filename>``` unstages a ```git add <filename>```. 
```git reset``` unstages ```git add .```.

- to remove node_modules from github, create a gitignore file
```npx gitignore node```
then run
```git rm -r --cached .```
which will remove all stuff
specified in gitignore file.
Then add and commit as usual.