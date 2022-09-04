---
marp: true
title: GIT GUD
author: Jakub Olejnik 
theme: gitgud
size: 4:3
color: white
backgroundColor: #262C39
paginate: true
---
# $ <span class="git">git</span> gud
### LEARN <span class="git">GIT</span> CLI BASICS :technologist:

<!-- _footer: _Prepared by [Jakub Olejnik](https://www.linkedin.com/in/jakub-olejnik-85a686203/) | 2022_-->


---
# TODO
- Bash CLI 101
- What is <span class="git">Git</span>?
- Creating a repository
- Working in a team
- Best practices

---
# TODO
- **Bash CLI 101** 👈
- What is <span class="git">Git</span>?
- Creating a repository
- Working in a team
- Best practices


---
# BASH 101
`ls` - display content of the current directory
`mkdir <directory>` - create a new directory
`cd <directory>` - go to a directory
`touch <file>` - create a file
`cat <file>` - display file contents
`rm <file>` - remove a file
`rmdir <directory>` - remove a directory

---
### ADDING SSH KEY TO YOUR GITHUB ACCOUNT
This part might be a bit confusing at this moment and you might find it much more clearer after the workshop.

All need to know now is that wit an SSH key you don't have to authorize yourself everytime you want to push changes to your remote.

Now open your terminal and type in:
```
$ ssh-keygen -t ed25519 
```
After successful completion, go to `~/.ssh` and check what files have been created. 

---
### ADDING SSH KEY TO YOUR GITHUB ACCOUNT
`ssh-keygen` generates two keys: private and public.
The former is just `id_ed25519` and the latter is `id_ed25519.pub`.

Display contents of public key file and copy all of it.

Nextly open GitHub and follow instruction of my real life version.

---
# TODO
-  Bash CLI 101 ✅
- **What is <span class="git">Git</span>?** 👈
- Creating a repository
- Working in a team
- Best practices

---
# WHAT IS <span class="git"> GIT</span>?
_<span class="git">Git</span> is a free and open source distributed Version Control System (VCS) designed to handle everything from small to very large projects with speed and efficiency._ 

<span class="audience-question">Ok, but what does it actually mean?</span>

I like to think about it as a very elaborate save system.
Let my real life version explain what I mean!

---
# TODO
- Bash CLI 101 ✅
- What is <span class="git">Git</span>? ✅
- **Creating a repository** 👈
- Working in a team
- Best practices
---
## CREATING A <span class="git"> GIT</span> REPOSITORY
Let's create a new directory called `repo-test` and then inside this directory create a new file `README.md`.

Next, run this command to initialize it as a <span class="git">Git</span> repository:
```
$ git init
```

With this command you can turn any directory into a <span class="git">Git</span> repository. It's all thanks to the magical `.git` directory.

<span class="audience-question">What are you talking about?
 I can't see anything like that!</span>

---
## .<span class="git">git</span> DIRECTORY
It is so important, that it is hidden by default.
This is the heart of your git repository.
Without it, no git commands would work.

 Type the following and check again:
 ```
 $ ls -al
 ```
Can you see it now? 

---
## .<span class="git">GIT</span>IGNORE
`.gitignore` is a special file in which you can put files which you want to, like the name suggests, ignore.

Anything listed in the file will be omitted when commiting new changes.

You can ignore single files, whole directories and its contents.
You can even use regular expressions to ignore series of files which names have some kind of pattern.

---
## CREATING YOUR FIRST COMMIT
The command I end up using the most is:
```
$ git status
```
It prints out a concise description of the current status of your repository and its contents.

Now you can add some files to be included in the next commit using:
```
$ git add <file>
```
It's also possible to add whole directories, which will add all of its contents.

---
## CREATING YOUR FIRST COMMIT
Now that you have all the desired files added, it's finally time to create a commit.
To do so you use the following command:
```
$ git commit
```
It will open a text editor (most likely _nano_) in which you can type a description of the changes you made.

If your commit message is short you can skip opening the editor and set the commit message directly in the command:
```
$ git commit -m <message>
``` 
---
## PUSHING YOUR CHANGES TO A REMOTE
Pushing changes is basically uploading them to a remote server.
You do that simply by typing:
```
$ git push
```
<span class="audience-question">Hmm, it doesn't seem to work...</span>

Ah, of course. We haven't set up a `remote` yet, that's why <span class="git">Git</span> doesn't know where to push the changes.

A `remote`, which as name suggests, is a remote repository corresponding to the local one.

---
## PUSHING YOUR CHANGES TO A REMOTE
To add a new `remote` to the repository use the following command:
```
$ git add remote origin <repo-url>
```
`repo-url` is the  URL of the repository you're gonna create on <span class="git">Git</span>Hub - right now!
\
\
All done? Let's try with the push one more time.

<!-- <span class="audience-question">Hey it works!</span> -->

---
# TODO
- Bash CLI 101 ✅
- What is <span class="git">Git</span>? ✅
- Creating a repository ✅
- **Working in a team** 👈
- Best practices

---
# TIME FOR A BREAK 🕚
Form groups of 2-4. 

After the break we'll be covering teamwork with <span class="git">Git</span>.

---
# TODO
- Bash CLI 101 ✅
- What is <span class="git">Git</span>? ✅
- Creating a repository ✅
- **Working in a team** 👈
- Best practices

---
## TEAMWORK AND <span class="git"> GIT</span>
<span class="git"> Git</span> is a great tool for a single developer. 
But is even a **greater** one for developers working in a team.

Imagine working on a big project, which has hundreds of files, each at least 500 lines of code long. How do you handle that?

By using a version control system, for example <span class="git"> Git</span>!

---
## CLONING A <span class="git">GIT</span> REPOSITORY
Let's start by cloning this repo: [git-gud-py](https://github.com/jaolejnik/git-gud-py)

```
$ git clone <repo-url>  
```

<span class="sidenote">**NOTE:** When cloning a repository it will create the directory with the exact name as the repository and put all the contents there. 
No need to create an additional directory for it.</span>

You can now see you have a local copy of the repository.

You don't have to perform any of the previous steps to start making commits, because `git clone` takes care of initialization and setting up the remote since you gave it all the required information.

But...

---
## REMOTE REPOSITORY PERMISSIONS
You need proper permissions to push the commits to the remote.

You're free to clone any public repository but you cannot publish any changes unless you are part of the collaborators for this repository.

Try to make any change, commit and push it.

<span class="audience-question">Failed...</span>

In that case we need to remove the data that link the files in the repository to my remote and, link it to the one that you have access to. 

Any ideas?

---
## QUICK EXERCISE
- Remove `.git` directory.
- Initialize it as your own repository.
- Check if there is a commit history.
- Create and add a new remote.
- Make and push a new commit.

---
## ADDING TEAM MEMBERS
To add other people to your git repository do the following:

- Open your repository on <span class="git">Git</span>Hub.
- Go to the `Settings` tab.
- On the sidebar select `Collaborators and team`.
- Click `Add people` button and type their name/username/email.

After few minutes, they should receive an email with the invitation from you.

Once they've accepted, you can edit their permissions.

Now everyone clone the repository.

---
## ABOUT THE CLONED PROJECT
The repository you just cloned contains a very simple Python project.

- `main.py` is an entry point,
- `person.py` stores the definition of a Person class.

To run it just enter the following in the project directory:
```
$ python main.py
```
Completing definition of methods will be your next exercise.

But before we get there, there's still one more file that we should talk about.

---
## WORKING WITH BRANCHES
_Branching means you diverge from the main line of development and continue to do work without messing with that main line._

To create a new branch:
```
$ git branch <new-branch>
```
...then to change to the branch:
```
$ git checkout <new-branch>
```

<!-- Now each person in the group may create a new branch with corresponding name:

----------------->  **name** | **age** | **country** | **job** <-----------------  -->

---
## EXERCISE 2
What you need to do:
- Create a new branch.
- Complete the method of your choice.
- Call it in the `introduction()`.
- Create a new Person object in `main.py` and make it introduce itself.
- Commit changes on your new branch.
- Push to the remote. 
- Mege all your branches together.


---
## MERGING CHANGES
When you completed all the changes on your branch, you  want to incorporate them into the branch you diverged form (usually `main`).

You can do that by switching to the desired branch and then typing:
```
$ git merge <branch-to-merge>
```

So let's say you were working on a branch `name`, you switch to `main` and then call `git merge name` to merge changes from `name` branch to `main`.

---
## PULL REQUESTS
But when working in a team you want to keep track of changes made by everyone and prevent some spaghetti code to be part of the main branch.

`Pull Requests` are a way to let your team know that you're done with your change and want somebody to review it.

If everything is in order you are free to merge your changes.

Let real life me show how you can create a Pull Request.

---
## MERGING CHANGES - CONFLICTS
Occasionally when making changes in parallel you and another developer will introduce different changes in the same place.
In that case <span class="git"> Git</span> is unsure what to do and informs you that there are `Conflicts`, which you need to resolve yourself.

If that is the case, then the list of files with conflicts will be displayed when you try to merge.

Now you need to go to each file and edit them according to your need.

Back to my real life version to show how it can be done.

---
# TODO
- Bash CLI 101 ✅
- What is <span class="git">Git</span>? ✅
- Creating a repository ✅
- Working in a team ✅
- **Best practices** 👈

---
<!-- _footer: This depends on the workflow of your team, but I find feature based branches to be the most common.-->
# BEST PRACTICES
- One change per commit.
- Descriptive commit messages.
- Name your branches after features.*
- Avoid pushing commits directly to `main`.
- NEVER force push to `main`.
  

---
# TODO
- Bash CLI 101 ✅
- What is <span class="git">Git</span>? ✅
- Creating a repository ✅
- Working in a team ✅
- Best practices ✅

--- 
# That is all!
### Thank you for participating!
\
\
_Now you're thinking with ~~portals~~ <span class="git">Git</span>_ 🤖
