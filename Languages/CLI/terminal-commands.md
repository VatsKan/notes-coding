# General terminal commands

* ```|``` (pipe). 
* ```grep```
* ```ps -ax``` list all processes
* ```kill <processId>``` kills the process with processId (number). Be careful!
* ```ps -ax | grep <SearchValue>``` will search all processes with the search value and print them. [Ref](https://www.chriswrites.com/how-to-view-and-kill-processes-using-the-terminal-in-mac-os-x/).

* ```process1 & process2``` will run process 1 in the background. 
    ```fg <processId>``` to bring a process to foreground.
    ```jobs``` to list all jobs. 
    [Ref](https://stackoverflow.com/questions/3004811/how-do-you-run-multiple-programs-in-parallel-from-a-bash-script)
    [Ref](https://bashitout.com/2013/05/18/Ampersands-on-the-command-line.html)

CHECK ALL ABOVE AND UNDERSTAND BETTER!

* ```open <file>``` is equivalent to double clicking on a file in the Finder. (e.g. text based files will open in your default text editor)

    To open a new terminal window
        - with the same working directory
        ```open -a Terminal "`pwd`"```
        - in the home directory
        ```open -a Terminal ~```
        - in general
        ```open -a Terminal <filepath>```

    I believe ```-a``` here stands for app. 

* to list all files in a directory (including hidden files)
    ```ls -a```

* deleting
    - empty directory
    ```rmdir <directoryName>```
    - file
    ```rm <filename>```
    - recursively -- LOOK UP

* print a string in terminal
    ```echo "string"```
    ```echo <filepath>```

* To look up: 
    ```cat```
    ```nano```
    ```z```
    ```top```
    ```sudo```
    ```osascript```
    difference between backticks and string. 

* can learn vim using
    ```vimtutor```

* conditionals
    [reference](https://linuxacademy.com/blog/linux/conditions-in-bash-scripting-if-statements/)
    ```
    if [ "a" != "b" ]; 
    then
        echo 'clearly'
        echo 'not equal' 
    else 
        echo 'they are equal'
    fi
    ```