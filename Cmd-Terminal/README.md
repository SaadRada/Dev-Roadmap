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

