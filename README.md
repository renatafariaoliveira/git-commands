### What is Git?
Git is an open source distributed version control system.

Version control system maintain a history of what changes have happened in your project or especifically code. Also, Git provides features like branches and merges that helps you to organize your repository.

### Download Git
This [link](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) has details on how to install Git.
Verify if Git is installed by using the following command in the command prompt:

```
git --version
```


Create your local Git repository

In your computer, create a folder for your project. Let’s call the project folder git-commands.
Go into your project folder and add a local Git repository to the project using the following commands:

```
git init
```

Let’s Add some Small Code now
Create a file called example.txt in the project folder and add the following text into it:

---

### Example Git commands

_Staging and Committing the code_

Committing is the process in which the code is added to the local repository. Before committing the code, it has to be in the staging area. The staging area is there to keep track of all the files which are to be committed.
Any file which is not added to the staging area will not be committed. This gives the developer control over which files need to be committed.

Use the following command for staging the file:
```
git add example.txt
```

In case you want to add multiple files you can use:
```
git add file1 file2 file3
```

If you want to add all the files inside your project folder to the staging area, use the following command:

```
git add .
```

Committing
Use the following command to commit the file:
```
git commit -m "Initial Commit"
```

_“Initial Commit”_ is the commit message here. Enter a relevant commit message to indicate what code changes were done in that particular commit.

_Status_

Use git status to find out information regarding what files are modified and what files are there in the staging area — it shows other information as well, which we can ignore for now.

Use the following command to see the status:

```
git status
```

_Log_

Use git log to print out all the commits which have been done up until now.

The command used for this is:
```
git log
```

The log shows the author of each commit, the date of the commit, and the commit message.

**Branches**

Up until now we have not created any branch in Git. By default, Git commits go into the master branch.

What is a branch?

A branch is nothing but a pointer to the latest commit in the Git repository. So currently our master branch is a pointer to the second commit “example.txt file is modified”.

Why are multiple branches needed?

Multiple branches are needed to support multiple parallel developments.

_Create a New Branch in Local_

Create a new branch called test using the following command:

```
git branch test
```

This command creates the test branch.

We are still in the context of the master branch. In order to switch to the test branch. use the following command:

```
git checkout test
```

Now we are in the test branch.

You can list out all the branches in local using the following command:

```
git branch
```

_Do Some Commits in the New Branch_

Modify example.txt by adding the following snippet:

Initial Content Adding more Content Adding some Content from test Branch

Now stage and commit using the following commands:

```
git add example.txt git commit -m "Commit message: here, you will add example.txt file with changes"
```

or, to add all files that you need:

```
git add . git commit -m "Commit message: here, you will add all files with changes"
```


_Merging_

Currently, Test Branch is ahead of the Master by 1 commit. Let’s say that now we want all the code in the Test Branch to be brought back to the Master Branch. This is where git merge is very useful.

In order to merge the code from the test branch into the master branch, follow these steps:

First go back to the master branch:

```
git checkout master
```

Then run the merge command:

```
git merge test
```

After running these 2 commands, the merge should be successful. In this example, there are no conflicts.

**The Remote Git Repository**

Until now, we have been working only in the local repository. Each developer will work in their local repository but eventually, they will push the code into a remote repository. Once the code is in the remote repository, other developers can see and modify that code.

_GitHub_

Here we will be using GitHub for the remote repository. Start a Project to create a new Git repository. 
Give the name as ```git-commands```.

To point your local repository to the remote repository, use the following command:

```
git remote add origin [repository url]
```

In my case, _[repository url]_ is https://github.com/renatafariaoliveira/git-commands.git

_Git Push_

In order to push all the code from the local repository into the remote repository, use the following command:

```
git push -u origin [branch name]
```

This pushes the code from the branch in the local repository to the branch in the remote repository.

_Git Pull_

Git pull is used to pull the latest changes from the remote repository into the local repository. The remote repository code is updated continuously by various developers, hence git pull is necessary:

```
git pull origin master
```

_Git Clone_

Git clone is used to clone an existing remote repository into your computer. The command for this is:

```
git clone [repository url]
```

___

That is it! Here is a basic tutorial about the Git.

So, if you need to know another commands, follow the Git [documentation](https://git-scm.com/docs).