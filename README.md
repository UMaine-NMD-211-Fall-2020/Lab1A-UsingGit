# Lab1A - UsingGit
This is the first week of labs (week of 9/7/2020). 
We will learn how to use git to version control our work and github to manage remote projects. 

## How Labs will Run
- Walk in & Discussion of concepts in Readings
- Start Excuting Parts of Lab

If you have questions
- reread/ retry the point where you have an issue, documenting your problem
- send a message to the troubleshooting slack channel
- if Katarina is free, she will help right away, but if not, other students may help

Do not get up and go ask for help, due to social distancing concerns. 
## 0. Pre Lab
To be looked over before lab. 
The actions should be completed.  

### Pre Lab Actions / Requirements
Bring  your laptopto the lab session.

It will be useful to have a text editor on your computer. 
[Atom](https://atom.io/) or [Sublime](https://www.sublimetext.com/) are great choices, but you can use what you will. 
Notepad will suffice, but will become cumbersome quickly and is not recommended.
We will use text editors when creating README.md files. 

If you cannot make the in-person lab session for any reason, contact the instructors simultaneously, through email or slack.  

### Pre Lab Readings
Lab will make more sense and run more smoothly if you have the chance to read these beforehand. 
Since this lab was released late, you may not be able to. 
We will briefly discuss the contents in lab. 
Please consult these resources if you are confused about why we are doing this lab. 

The last reading, [Git vs. Github: What's the Difference?](https://blog.devmountain.com/git-vs-github-whats-the-difference/), may give you sufficient information. 
If not, check out the other readings. 
Also, as always, feel free to search the internet for more information. 

### Version Control 

#### What is it?
[What is Version Control](https://www.atlassian.com/git/tutorials/what-is-version-control)

#### Why use it?
[Why use a Version Control System](https://www.git-tower.com/learn/git/ebook/en/desktop-gui/basics/why-use-version-control#:~:text=%20Why%20Use%20a%20Version%20Control%20System%3F%20,a%20file%20%28or%20even%20the%20whole...%20More%20)

### What is Git? 
Git is the version control system we will use. Learn more about [git](https://www.git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F) specifics here. It is a-ok if not everything is clear. 

### Git Vs. Github
[Git vs. Github: What's the Difference?](https://blog.devmountain.com/git-vs-github-whats-the-difference/)

## 1. Git on your Machine 
For the labs, you will want to have git on your local machines / your laptops. 

### Is Git already installed?
Navigate to your command prompt / shell / terminal. 
If none of the above are features that come with your operating system, try googling first, then asking.  
(If you have a windows or a mac, you should have command prompt/terminal). 
If you are curious, you can read an unofficial writeup about the difference between the different terms on  [askubuntu.com](https://askubuntu.com/questions/506510/what-is-the-difference-between-terminal-console-shell-and-command-line)
- [Windows](https://www.howtogeek.com/235101/10-ways-to-open-the-command-prompt-in-windows-10/)
- [Mac](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac)
- [Ubuntu Linux](https://www.wikihow.com/Open-a-Terminal-Window-in-Ubuntu)

Once open, type
```
git --version
```
and hit enter.

If you have git on your machine, you will see a version number. 
If you do have git, skip installation. 

If you want to upgrade git, please do. 
Search online to figure out how to upgrade git on your operating system.

### Installation
If you do not Follow the directions for your machine to [install](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) git.

## 2. Your First Git Repo
First, you will make your own github repository. 
This is how you would start any solo project that you would want to put under version control. 
This is also how you would start a team project, but in that case, only one person needs to make the initial folder. 

It is a very good idea to put any coding projects under version control. 

### Make a Folder (Repository)

Make a folder for the first section of Lab 1A somewhere appropriate on your computer, such as a folder for all labs in this class. 
Name it `1AC-*YOUR FIRST NAME*-*YOUR LAST NAME*`. 

#### git init
Open your command line/terminal/shell.
Navigate to your saved folder `1AC-I-*YOUR FIRST NAME*-*YOUR LAST NAME*` by typing. You can see all files in a folder in terminal by typing `ls` on mac/linux or `dir` on windows. You can navigate to subfolders by typing `cd SUBFOLDER1\SUBFOLDER2\...\SUBFOLDERN`. If you have gone too far, you can type `cd ..` to go up one level. 

Initialize the folder `1AC-*YOUR FIRST NAME*-*YOUR LAST NAME*` as a git folder by typing
```
git init
``` 
This allows us to start keeping track of changes / versions on our local systems. 

But before we can keep track of content, we need content. 

#### Initial folder content

##### README.md
Open your text editor (atom, sublime, etc). 
Open a new file. 
Click on file, save, then navigate to the folder. 
Save the new file as **README.md**. 
Fill the README.md with the text below
```markdown
# Lab 1AC
## Version Controlled - Processing
1. Lab 1A: initialize version controlled repository
2. Lab 1C: 
```
##### .gitignore file
Running processing and other computer programs generates files we do not necessarily want or need to save. 
We do not need to save them, and convince the computer to ignore them with a `.gitignore` file. 

Open a new file.
In the same folder, save a file called `.gitignore`.
Fill it with the 10 lines of code from [here](https://github.com/github/gitignore/blob/master/Processing.gitignore), like so: 
```processing
# source file -> https://github.com/github/gitignore/blob/master/Processing.gitignore
.DS_Store
applet
application.linux-arm64
application.linux-armv6hf
application.linux32
application.linux64
application.windows32
application.windows64
application.macosx
out
```
### Your First Commit
1. Make sure you are still in `1AC-I-*YOUR FIRST NAME*-*YOUR LAST NAME*`
2. Check to see what files need to have their new changes tracked by typing ```
git status ```. Files that need to have their changes tracked are often shown in red. 

3. To track the changes of a file, say your `README.md`, type ```
git add README.md ```
and then hit `ENTER`. 
To add another file, say the `.gitignore`, repeat the process, but use the name `.gitignore` instead.  

4. Type `git status` again to make sure that all files are added and have their changes tracked. Oftentimes, added files have changed to green. 

5. We need to commit these changes to the version control log of happenings. 
To do so, type ```
git commit -m "Initial commit - add README and gitignore" ```

6. Check your status again! There should now be no changes pending on your local machine. 

Every time you make significant changes, commit. 
Each time you commit, write a useful commit message. 
This way, if you ever need to go back and undo your work, you can reset your project. Say something went wrong after I changed my triangles green. If my commit message tells me when triangles are green, I can roll back to that point in time. We will not discuss rolling back changes yet, but if for some reason you need this, I will help you get through the process.  

## 3. Add Project to Github
Back up your version controlled code on your computer online through Github. 
Not only does this give you a backup copy, but it starts to provide framework for remote teamwork - sharing code and working together on different parts of the same code simultaneously. 
We will not be working on remote teamwork this week, but will introduce it next week. 

### Create a github account
[Join Github](https://github.com/join)
You can use a school email, emails are not displayed unless you choose them to be.

Keep your login information somewhere safe. 

### Communicating with github
#### Set your username
So that Github knows you are the person trying to communicate with it and commit code, [set your github username](https://docs.github.com/en/github/using-git/setting-your-username-in-git#setting-your-git-username-for-every-repository-on-your-computer). Set it for every repository on your machine. 

#### SSH Keys
This the secret password exchange that Github needs so that it knows this computer is allowed to send it code. 
[Generate and add SSH Keys](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent). 
Truthfully, you can copy and paste the ssh keys, which is my preferred way. If many of you get here and are stuck, I am happy to give a class demo. 

#### Add Your Local Repository to Github
Follow the steps [here](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

Basically this is
1. Create a repo on Github with the appropriate name (`1AC-I-*YOUR FIRST NAME*-*YOUR LAST NAME*`)
2. Skip to step 7. You should still be in your local directory `1AC-I-*YOUR FIRST NAME*-*YOUR LAST NAME*` on the command line/terminal/shell. You have already initialized the folder, added files, commited. 
3. Complete steps 7 - 9. 

Now, your code is under version control and accessible remotely. Any time you make local changes, remember to add, commit, and push to the online version by typing `git push origin master`. 

This is the simplest type of putting our code online with version control. We will discuss better github ettiquette for pushing changes next week.

## Next Steps
We will continue with this repository in Lab 1C. Lab 1C covers some processing exercises. 

We will pick up with these concepts next week, introducing how to get a repository stored on computer not on your computer and how to work on the same file as other people. 

