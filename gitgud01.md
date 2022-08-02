---
marp: true
title: GIT GUD
author: Jakub Olejnik & Aleksander Pucher
theme: gitgud
size: 4:3
color: white
backgroundColor: #262C39
paginate: true
---
# $ <span class="git">git</span> gud
### LEARN <span class="git">GIT</span> CLI BASICS :technologist:

<!-- _footer: _Prepared by [Jakub Olejnik]() | 2022_-->

---

# PREREQUISITES
- <span class="git">Git</span>
    - Linux/Mac - you should be good👍
    - Windows - [<span class="git">Git</span> Bash](https://git-scm.com/download/win) :
- <span class="git">Git</span>Hub Account
  - [with added SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
- Python 3 🐍

---
# TODO
- Bash 101
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
`rm <file>` - remove a file
`rmdir <directory>` - remove a directory

---
# TODO
-  Bash CLI 101 ✅
- **What is <span class="git">Git</span>?** 👈
- Creating a repository
- Working in a team
- Best practices

---
# WHAT IS <span class="git"> GIT</span>?
_<span class="git">Git</span> is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency._ 

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

Next, run this command to initialize as a git repository:
```
$ git init
```

With this command you can turn any directory into a <span class="git">Git</span> repository. It's all thanks to the magical `.git` directory.
Now check for the magical `.git` directory.

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

By using <span class="git"> Git</span> of course!

---
## CLONING A <span class="git">GIT</span> REPOSITORY
Let's start by cloning this repo: [repolinkTODO]()

```
$ git clone repolinkssshTODO
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

In that case we need to remove the data that link the files in the repository to my remote and link it to the one that you have access to. 

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




---
# TODO
- Bash CLI 101 ✅
- What is <span class="git">Git</span>? ✅
- Creating a repository ✅
- Working in a team ✅
- **Best practices** 👈

---
# BEST PRACTICES
- One change per commit
- Verbose commit messages
- 

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
