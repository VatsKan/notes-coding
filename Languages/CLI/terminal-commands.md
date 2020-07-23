# General terminal commands

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