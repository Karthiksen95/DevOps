In this lab, we'll explore key Git concepts using a sample project: creating a simple Python script. The project will demonstrate how to use branches, commits, merging, and pull requests to collaborate and track changes in the codebase.

Step 1: Create a GitHub repository

Sign up or log in to your GitHub account at https://github.com.
Click the "+" icon in the upper-right corner and select "New repository."
Choose a repository name (e.g., "python-sample"), provide a short description, and select the desired visibility (public or private).
Initialize the repository with a README file and choose a license if desired, then click "Create repository."
Optionally you can also create a test file and commit it

Step 2: Clone the repository
Clone the repository to your local machine to start working with the code. Open your terminal or command prompt and run:
```
git clone https://github.com/your-username/python-sample.git
cd python-sample
```
Step 3: Create a new branch for the Python script
Create a new branch to work on the Python script without affecting the main branch. Run:
```
git checkout -b script-feature
git branch
```
Step 4: Add the Python script
Create a new Python file named ```hello.py``` in your repository folder with the following content:
```
def hello(name):
    return f"Hello, {name}!"

if __name__ == "__main__":
    name = input("Enter your name: ")
    print(hello(name))
```
Step 5: Commit the changes
Stage and commit the changes to the script-feature branch:
```
git add hello.py
git config --global user.email "username@example.com"
git config --global user.name "name"
git commit -m "Add hello.py script"
git status
```
Step 6: Push the changes
Push the changes to the remote repository:
```
git push origin script-feature
```
give the username and password token
Step 7: Create a pull request

Navigate to your "python-sample" repository on GitHub.
Click the "Pull Requests" tab and then click "New Pull Request."
Select the source branch (script-feature) and the target branch (main).
Add a title and description for the pull request, then click "Create Pull Request."
Step 8: Review and merge the pull request

Review the changes in the pull request and, if necessary, discuss any issues in the comments section.
Once the changes are approved, click "Merge Pull Request" and confirm the merge.
Step 9: Update your local main branch
Switch to the main branch and pull the changes:
```
git checkout main
git pull origin main
```
Step 10: Delete the feature branch
Now that the changes have been merged, you can delete the feature branch:
```
git branch -d script-feature
git push origin --delete script-feature
```
In this lab, we covered essential Git and GitHub concepts, including creating a repository, working with branches, committing changes, pushing to a remote repository, and collaborating through pull requests. By applying these concepts to the sample Python project, we demonstrated how to manage and track changes in a codebase effectively.
