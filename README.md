# GIT GUD

A small Git CLI (Command Line Interface) workshop prepared for people that haven't used Git before, haven't used it in a while, have used it very sparsely or would like to learn CLI instead of GUI. 

---
## PREREQUISITES
- Git CLI 
- Python 3 
- GitHub account
- Code editor of your choice (I recommend [Vistual Studio Code](https://code.visualstudio.com/?wt.mc_id=vscom_downloads), different than Vistual Studio)

If something is missing go to [Setup](#setup) section.

Once you have everything you're free to get started!
 
## SETUP
### Installing Git CLI
#### Windows
Git installation on Windows is a really straightforward process. Go to  [official Git website download section](https://git-scm.com/downloads), select Windows, then pick your system version. Finally download and launch the installer. When asked bout the defualt text editor open the drop down list and select `nano` or leave it as `vim` if you're feeling adventurous.Apart from that you don't need to change anything else and just go with the suggested installation options. 

#### Mac/Linux
Git comes installed by default on most Mac machines and Linux distributions. So you who are working on these operating systems are in luck. To make sure you have it installed open a terminal and type in:
```
$ git --version
```
If the command executes succesfully and you get an output that looks similar to this: `git version 2.25.1`, then you have Git installed.

If not, go to [official Git website download section](https://git-scm.com/downloads), select your OS and follow the instructions (which are mainly typing in 1-2 commands into your terminal).

### Installing Python
#### Windows
[This article on RealPython](https://realpython.com/installing-python/) (great Python blog BTW) explains everything much better than I would ever have. Scroll down to Windows section and follow the instructions for one of the 3 ways of installation.

#### Mac/Linux
Similar to Git, Python comes preinstalled on most Mac machines and Linux distributions. You can check if you have one installed similarily to Git. Just open your terminal and type in: 
```
$ python --version
```
If the output looks similar to this: `Python 3.9.7` you have **Python 3** installed.

**Note** that I said Python 3, since on some OS Python 2 can be installed along Python 3 and aliased to the `python` keyword. If the first number of your Python version is 2 then this is Python 2. Try using `python3` instead of `python` and check if it outputs a Python 3 version.

If none of the above works, then check [this article on RealPython](https://realpython.com/installing-python/) on how to get Python 3 on your Mac/Linux machine.

