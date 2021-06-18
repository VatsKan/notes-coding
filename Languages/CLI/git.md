# Git notes

[git rebasing reference](https://www.git-tower.com/learn/git/ebook/en/desktop-gui/advanced-topics/rebase#start)

## git workflow

[All git workflows link](https://www.atlassian.com/git/tutorials/comparing-workflows)

Gitflow:

[Gitflow original link](https://nvie.com/posts/a-successful-git-branching-model/)

[Gitflow link](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)


## commands

- ```git reset <filename>``` unstages a ```git add <filename>```. 
```git reset``` unstages ```git add .```.

- ```git commit --amend -m "my message"``` will change just the commit message to your new message. If you have made changes to the code and
do ```git add .``` first, followed by the command above, then it will overwrite your previous commit with this one. [CHECK THIS IS TRUE!]

- ```git log``` shows you your commit history.

- to remove node_modules from github, create a gitignore file
```npx gitignore node```
then run
```git rm -r --cached .```
which will remove all stuff
specified in gitignore file.
Then add and commit as usual.

- ```git diff branch1 branch2``` will show you differences between branch1 and branch2. [Q: does it show you the diff between the remote or local branches?]