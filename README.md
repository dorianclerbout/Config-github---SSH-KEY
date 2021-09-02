# GitHub Config

- [1 - Create SSH KEY](#1---Create-SSH-KEY)
- [2 - Adding SSH KEY on GITHUB](#2---Adding-SSH-KEY)
- [3 - Activate local SSH KEY ](#3---Activate-SSH-KEY)
- [4 -  Git Local config](#4---Git-Local-config)
- [5 -  Check Git config](#5---Check-Git-config)


## 1 - Create SSH KEY 

Inside terminal enter : 

     ssh-keygen -t rsa -b 4096 -C "your-mail@exemple.com"

## 2 - Adding SSH KEY

Take your SSH KEY with : 

    cat ~/.ssh/id_rsa.pub

Go to your [GitHub](http://github.com) account and :

    Settings > SSH and GPG keys > New SSH key > Paste your keys !

## 3 - Activate SSH KEY

Launch ssh-agent secure :

    eval "$(ssh-agent -s)"

And activate your SSH KEY :

    ssh-add ~/.ssh/id_rsa 

## 4 - Git Local config

1. Register your user name :
    
        git config --global user.name "your-name"
2. Register your email
        
        git config --global user.email "your-mail@exemple.com"

3. Edit your FAV IDE :
                    
        git config --global core.editor code # for VSC
4. (OPTIONNAL) Activate color :
   
         git config --global color.ui true

## 5 -  Check Git config

For see your config : 
    
    git config -l

