# Build your own custom scripts

[Reference](https://medium.com/devnetwork/how-to-create-your-own-custom-terminal-commands-c5008782a78e)

* create a .my-scripts.sh file
in your home directory ~. Note
that a dot is placed before 
the file name so that it is hidden.

* Add the following line of
code to your .zshrc (or .bashrc) 
file ```source ~/.my-scripts.sh``` 
which will load your scripts
into every new terminal window 
you create. 

* You can write any terminal scripts
inside your .my-scripts.sh file. (Note if you write a function direct into the terminal, then it won't be available in other terminal windows)

* The first line inside your .my-scripts.sh file should be ```#!/bin/bash```, which is a 
convention used by Shell scripts to use
the appropriate interpreter. 


### Syntax
- the \$ sign is used for variables. e.g. \$1 

### Example scripts

In your .sh file (or in the terminal), add 
```
function print_my_input() {
  echo 'Your input: ' $1
}
```
then run
```
print_my_input 'Just trying out my new command'
```
in your terminal. 


### Asides
- By default new files only have read permission (not write permission)...which is enough in the case above of creating scripts. If you wanted to set 
executable permission in terminal, you would have to ```chmod +x .my-scripts.sh``` (not sure exactly what this does!)
- .sh is a file used for bash scripts. (its a unix shell executable file)
- The .zshrc or .bashrc files run every time a new zsh or bash terminal is opened. (note this is not true of .bash_profile, which runs on login i believe, but am not sure). 
- rc stands for "run command" (not too clear online... seems to be multiple possibilities e.g runtime configuration)... and it contains startup info.



