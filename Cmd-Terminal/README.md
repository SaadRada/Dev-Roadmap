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
## Directories
- ### change
    - cd => Change Directorie
        ````
        cd path
        cd Desktop
        cd Documents
        ````
    - Return to Previous Directorie
        ````
        cd ..
        ````
    - To auto complet path you can use <strong>Tab</strong> Keyword
    - Return to Root path (cd path)
        ````
        cd \
        ````
    - To get current Directorie
        ````
        pwd
        ````
- ### create
    - <strong>md</strong> OR <strong>mkdir</strong> (Make Directorie)
        ````
        mkdir public_html
        => folder public_html has been Created

        cd public_html
        => change directorie to public_html folder
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
        