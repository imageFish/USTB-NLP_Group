# Steps for adding your reports to the USTB-NLP_Group repository
## Step 1: Install git
Install git on windows or Linux
## Step 2: Configure git and Github
### 2.1 Git
Configure the user name and email using the below command:
```bash
git config --global user.name "YourName"
git config --global user.email "YourEmail"
```
Using the below command to generate your public SSH key
```bash
ssh-keygen -t rsa -C "youremail@example.com"
```
Then, you can find your public SSH key file 'id_rsa.pub' and private SSH key file 'id_rsa' where the current location is.
### 2.2 Github
Fork the <a herf='https://github.com/imageFish/USTB-NLP_Group'>USTB-NLP_Group repository</a> to your own account.

Open the 'id_rsa.pub' with the Notepad, and copy the content to your Github account SSH-KEYS. You can find 'SSH and GPG keys' in your account setting. The SSH-key title can be named as anything, it's useless.
## Step 3: Clone USTB-NLP_Group repository
Clone USTB-NLP_Group repository to your computer using "clone" commmad
```bash
git clone git@github.com:imageFish/USTB-NLP_Group.git
```
This command clone USTB-NLP_Group to your current location, you can use 'pwd' to see what is the current location.
## Step 4: Add your files to USTB-NLP_Group
Befor adding your own files, here are some rules wu should follow:
- For each group meeting, There is a folder to store our reports, named as the data when we had the meeting.
- Add your own fold to store your own files in each meeting fold.
- the file structure is as follows:
  - 2018-12-05
    - Heran Wu
    - Lu Zhang
    - Bei Yin
  - 2018-12-12
    - Bowen Zhang
    - Zanxia Jin
  - $\cdots$

Add new folds and files through the file manager, then inform these changes on Git, the command is as follows:
```bash
git add path/to/your/files/or/folds
```
Apply these changes
```bash
git commit -am 'YourAnnotation'
```
## Step 5: Push local repository to Github
First, link the local repository to USTB-NLP_Group on Github
```bash
git remote add USTB-NLP_Group git@github.com:imageFish/USTB-NLP_Group.git
```
Finally, push these changes to USTB-NLP_Group on Gitgub
```bash
git push USTB-NLP_Group master
```