# CMD - Terminal Commands
## Introduction
- Shell => is the command line interpreter
- Terminal => Text input/output Enviroment
- CMD => is the original shell for the Microsoft DOS operating system
- PowerShell => After CMD (Has More Featers than CMD)
- GUI => Graphical User Interface
## Why use CMD - Terminal ?
- Use less System Resources
- Use Loops to Repeat Commands
- Deal With Package Manager
- Use Git Commands
- Increase Writing Speed
- ...
## Directories
- ### change
    - cd => Change Directory
        ````
        cd path
        cd Desktop
        cd Documents
        ````
    - Return to Previous Directory
        ````
        cd ..
        ````
    - To auto complet path you can use <strong>Tab</strong> Keyword
    - Return to Root path (cd path)
        ````
        cd \
        ````
    - To get current Directory
        ````
        pwd
        ````
- ### create
    - <strong>md</strong> OR <strong>mkdir</strong> (Make Directory)
        ````
        mkdir public_html
        => folder public_html has been Created

        cd public_html
        => change directory to public_html folder
        >cd/public_html

        mkdir css js imgs fonts
        => Create 4 folders inside public_html
- ### move and replace
    - <strong>mv</strong> OR <strong>move</strong> is rename folder Or move it if the name exist
        ````
        cd dsktop public_html
        >go to public_html

        ls
        > get list files /css /js /imgs /fonts

        mv imgs images
        > rename imgs folder to images /css /js /images /fonts

        mv fonts images
        > move fonts into images folder
- ### copy
    - cp -r file toPath
        ````
        cd Desktop/public_html
        >public_html

        ls
        >images /css /js /images /fonts

        cp -r css css2
        >images /css /css2 /js /images /fonts
- ### remove
    - rm -r folderName
        ````
        ls
        >images /css /css2 /js /images /fonts

        rm -r css2
        >images /css /js /images /fonts
        ````

## Cat and Echo
- ### Echo
    - The <strong>echo</strong> command writes an argument to the Terminal's standard output
    - We can use <strong>echo</strong> command to put string in text file
    ````
    echo hello world > file.txt
    => new txt file has been created with "hello world" value
    ````
    - the <strong>></strong> Keyword is repleace The previouse data in the file
    - the <strong>>></strong> Keyword is append The data to The file
    ````
    echo "hello again" >> file.txt
    => append "hello again" to the previouse data in file.txt
- ### Cat
    - The <strong>cat</strong> (short for “concatenate“) command is one of the most frequently used commands in Linux/Unix-like operating systems. cat command allows us to create single or multiple files, view content of a file, concatenate files and redirect output in terminal or files.
    - View Content
        ````
        cat file.txt
        => hello world
        hello again
        ````
    - Create and Copy file(s)
        ````
        cat newfile.txt
        => newfile.txt has been created

        cat file.txt > newfile.txt
        => copy file.txt data to newfile.txt

        cat file.txt >> newfile.txt
        => append file.txt data to newfile.txt
        ````
    - Concatenate files
        ````
        cat file.txt newfile.txt > lastfile.txt
        => lastfile.txt has been created with concatenate between file.txt and newfile.txt data
        ````
## Grep (Global regular expression print)
- <strong>grep</strong> is a command-line utility for searching plain-text data sets for lines that match a regular expression
    ````
    grep "text" file.txt
    => search "text" in file.txt

    grep "text" -r
    => search in all directory

    grep "text" -r -l
    => get list of files has text value
    ````
## Tree
- The tree is a tiny, cross-platform command-line program used to recursively list or display the content of a directory in a tree-like format
- show folders
    ````
    tree /a
    ````
- show shema folders and files nested
    ````
    tree /f
    ````

## More Tricks
- CTR + C => to stop command line process
- Alias : is used to create soutcuts of code
    ````
    alias
    pwd=cd
    explorer=e
    ...
    ````
- To create Alias
    ````
    alias gtp=git push
    ````
- Run multiple command with <strong>&&</strong>
    ````
    ipconfig && mkdir saad
    ````
- whoami : used to get current user name
    ````
    whoami
    => administrator
    ````
- Stock command result to file
    ````
    ping google.com > ping_google.txt
    ````
- Copy command result to clipboard
    ````
    ipconfig | clip
    ````
    
## cmdChallenge
- ### Tail
    - The <strong>tail</strong> command shows you data from the end of a file. Usually, new data is added to the end of a file, so the tail command is a quick and easy way to see the most recent additions to a file
        ````
        tail -5 newfile.txt
        => get the last 5 line from newfile.txt
        ````
- ### Touch
    - The <strong>touch</strong> command is a standard command used in UNIX/Linux operating system which is used to create, change and modify timestamps of a file. Basically, there are two different commands to create a file in the Linux system which is as follows: cat command: It is used to create the file with content.
        ````
        touch index.html
        => index.html has been created
        ````
- ### Create nested directory in a single command
    - To Create nested directory we can use <strong>-p</strong> keyword is stand for parent
    - create <i>temp/files</i>
        ````
        mkdir -p temp/files
        ````
- ### Symbolic Links
    - A <strong>symbolic link</strong> is a term for any file that contains a reference to another file or directory in the form of an absolute or relative path and that affects pathname resolution.
    - Hard link and soft link (symbolic link)
    ![hard link - soft link](https://miro.medium.com/max/624/1*bEu7dBB67IXWxxb_Qi8A0w.jpeg)

        ````
        ln -s [OPTIONS] FILE LINK
        ln -s source_file symbolic_link
        => -s stand for soft
        ````
    - show list of links created
        ````
        ls -l
        ````
    - Removing Symlinks
        ````
        unlink symlink_to_remove

        rm symlink_to_remove
        ````
- ### Remove files
    - remove all files in a directory
        ````
        rm -r *
        ````
    - remove files with specific extension
        ````
        rm **/*.css

        find . -name "*.css" -type f -delete
        ````

all command docs in [ss64](https://ss64.com/)