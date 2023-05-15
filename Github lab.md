## Lab 1: Git operations


Create the github repository based on the method shown in the course document
Create an empty repository in your github account. Name = hello-world

After that, lets operate in local Git repository


### Initializing the local git repository and committing changes

On the vm, do the below:
```
cd ~/
```
Check GIT version. 
```
git --version
```
If it does not exist, then you can install with below command. Else no need to execute below line:  
```
sudo apt install git -y
```
Download the Java code we are going to use in the CICD pipeline
```
wget https://devops-e-e.s3.ap-south-1.amazonaws.com/hello-world-master.zip
```
```
sudo apt install unzip
unzip hello-world-master.zip -d hello-world-master
```
```
ls
rm hello-world-master.zip
cd hello-world-master
ls
```
```
git init .
```
Check the email and user name configured.
```
git config user.email
git config user.name
```
If you need to change it, you can use below:
```
git config --global user.email "< Add your email >"
git config --global user.name "< Add your Name >"
```
```
git status
git add .
git status
```
```
git log
git commit -m "This is the first commit"
git log
git status
```
```
git remote add origin < Replace your Repository URL > 
```
Ex: git remote add origin https://github.com/karthiksen/hello-world.git
```
git remote show origin
```


### Task 3: Pushing the Code into your Remote GitHub Repository  

To push code to Github, You need to generate a Personal Access Token (PAT) in github.
Go to your Github homepage. Click on settings in right side top menu. Click on Developer settings on 
left side menu bottom. Click on Personal Access Token on left side menu. Click on Generate New Token
Under 'Select Scopes' select all items. Click on 'generate token'. Copy the token

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
```
git push origin master 
```
when it asks for password, enter the PAT Token
Token: <enter your PAT> 
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 # Use your respective PAT
When you enter the token, the cursor does not move. It's the expected behavior
 

### Task 4: Creating a Git Branch and Pushing into the Remote Repository  

```
git branch dev
git branch
git checkout dev
git branch
```
```
vi index.html
```
Press INSERT and add the below content
```
<html>
<body>
<h1> Hi There! This file is added in dev branch </h1>
</body>
</html>
```
Save vi using ESCAPE + :wq!
```
git status
git add index.html
git status
```
```
git commit -m "adding new file index.html in new branch dev"
git log
```
```
git push origin dev
```
when it asks for password, enter PAT Token
Token: <your PAT>
```
git branch
git branch prod
git branch
git checkout prod
git branch
git merge dev
git push origin prod
```
Token: <PAT>
```
git checkout master
git merge prod
git push origin master
```


