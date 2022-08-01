https://github.com/ASalad42/documentation/blob/main/README.md

# GitHub Setup with HTTPS and SSH

This markdown documentation will go through how to setup github

# Downloading Git

We begin with downloading git and git.bash 
https://git-scm.com/downloads
![image](https://user-images.githubusercontent.com/104793540/182090297-68ba1439-fa9c-4d8f-b986-bce730f8f520.png)


HTTPS

Starting a repo and pushing it with https

1. git init
2. git status
3. git add .
4. git commit -m "message"
5. after creating repo on github, copy from "...or push an existing repository from the command line"
6. git remote add origin https://github.com/ASalad42/Github-demo.git
   git branch -M main
   git push -u origin main
![image](https://user-images.githubusercontent.com/104793540/182090247-662ece96-27b9-4fe5-94a4-99d97dce7e15.png)

SSH

We can generate an ssh key for authentication 
for more pease check out:
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

1. open terminal
2. create .ssh directory (folder) mkdir .ssh
3. open directory with cd. ssh
4. Generate key with $ssh-keygen -t rsa -b 4096 -C "youremail@example.com"
5. Email MUST be the same as your github account
6. you will then be prompted to enter a file name and a passphrase
7. upon completion, you will get a public and private key
8. copy the .pub and paste into github (settings>ssh and gpg keys section)
![image](https://user-images.githubusercontent.com/104793540/182090016-aedf6e4b-d0f5-4e66-bc99-35a26baf4ed0.png)
![image](https://user-images.githubusercontent.com/104793540/182090107-54522276-eefb-4aac-8fe4-786b0e493150.png)


````bash
mkdir .filename 
cd .filename 
pwd
ssh-keygen -t rsa -b 4096 -C "ayanie@live.co.uk"
122 #name of key folder 
#press enter 
#press enter
cat 122.pub 
#copy public key
#go to github and copy key into ssh key section in settings 
eval "$(ssh-agent -s)"
ssh-add ~/filename/122

````


