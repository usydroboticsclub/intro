# intro
Welcome!

In this guide, we will be teaching you how to use `git`, a sharing tool for code. `git` is used throughout software engineering and mechatronics fields because of its ability to store, share and merge parallel versions of functional code. This makes it very useful, so let's get it right!

If you want to deep dive into what git is, checkout the `more-about-git` branch at the end of this tutorial ;)

### Git vs Github
`git` is a tool for sharing collections of files. `github` is a centralised space to store collections of files, accessible using `git`. If you like metaphors, `github` is to `git` as `outlook` is to `email`.

## 1 Using the terminal
As a roboticist, not all computers have screens - such as robots you might find in the brain of a self-driving car, self-sailing boat, self-walking dog or self-chilling smart fridge. `git` especially was designed in an era when screens with GUIs were harder to come by - so in this tutorial we'll give you a crash course on terminal commands too.

1. Open a terminal window.
   - Windows: Type in 'cmd' into your start, and click `command prompt`. If all goes well, a black cmd window should appear.
      - Don't use `git bash` when it appears on your start menu. That will bring up a linux style terminal. 
   - OSX: Type in 'terminal' into your launcher. If all goes well, a white terminal window should appear.
   - Linux: Type in 'terminal' into your start. If all goes well, a black terminal window should appear.
2. Locate yourself.
   - Windows: Each line of your terminal should show you where you are. E.g. Your terminal should start with `C:\Users\<your-username>`.
   - OSX: Your terminal should show you the folder you are in next to your username. To figure out the entire path (aka _absolute path_) to where you are, type `pwd` and hit enter.
   - Linux: Depending on which distribution you're using, you may have your full path or just the folder. Typing `pwd` will work as well.
3. Make a folder (aka _directory_).
   - All platforms: Type in `mkdir USRC` and hit enter. `mkdir` stands for "MaKe DIRectory".
4. Enter the directory you just made.
   - All platforms: Type in `cd USRC` and hit enter. `cd` stands for "Change Directory".
5. Leave the directory you just made.
   - All platforms: Type in `cd ..`. `..` is a special sequence that tells `cd` that you want to go out of the folder. 
6. Go into the directory you just made again. (Review step 4).
7. Make a file in this directory.
   - Windows: Type in `type nul > newfile.txt` in your terminal and hit enter. (Ask stackoverflow if you want to know what this means - its a long answer).
   - OSX: Type in `touch newfile.txt` in your terminal and hit enter. 
   - Linux: Type in `touch newfile.txt` in your terminal and hit enter.
8. Figure out what is in this directory.
   - Windows: Type in `dir` and hit enter. Read the output.
   - OSX: Type in `ls -a` and hit enter. Read the output.
   - Linux: Type in `ls -a` and hit enter. Read the output.
9. Open a normal file explorer, and check everything matches up.
   - Windows: Type `explorer .`, then confirm using the file explorer that newfile.txt exists.
   - OSX: Type `open .`, then confirm using finder that newfile.txt exists.
   - Linux: Type `nautilus .`, then confirm using the file explorer that newfile.txt exists.
10. [TEST YOUR KNOWLEDGE]: List all the files in your `Desktop` folder.

A quick summary of the commands we learnt:
```
mkdir <name>: Make a directory called <name>.
cd <name>: Open the directory called <name>.
cd ..: Go up one directory level.
ls -a OR dir: List the files and directories in this folder.
touch <name> OR type nul> <name>: Create an empty file in this folder.
```

For more terminal *fun*, checkout the `fun-with-terminal` branch at the end of this tutorial ;)

## 2 Installing Git
Your `git` journey will be different depending on what platform you're using. Select from the below:
### Windows
1. If you're on windows, you'll need to start by downloading git. Go here: <https://git-scm.com/downloads>
2. Once you get to the screen where there are a whole bunch of checkboxes, leave it at the default configuration.
3. When you get to the screen where it says 'Use VIM as the editor by default, **change it to Nano**. Unless you're a masochist.
4. Choose 'Use windows' default console window' when you get to it.
5. Leave the rest of the config as is.
6. Once you're done, follow the **COMMON** steps below.
### MacOSX
1. If you're on MacOSX, you'll need to start by installing Homebrew, which then can install git, so copy this command: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
2. Open up Terminal, which can be found through Spotlight, paste the link and then press enter. (You might need to enter your computer password)
3. Next press enter when prompted, and let the terminal install Homebrew. You'll know this is over when you stop getting prompts.
4. Type `brew install git` into terminal and press enter, this is installing Git. Just let the computer do its thing and you're done.
5. Once you're done, follow the **COMMON** steps below.
### Linux
1. Follow the instructions here: <https://git-scm.com/downloads>
2. Once you're done, follow the **COMMON** steps below.
### COMMON
1. Close the terminal that you opened in the previous part, and open a brand new terminal. (You need to do this because an old terminal won't know what `git` is if git is installed while the terminal is alive)
2. Create a git username and email address. (You only need to do this once per computer, ever.)
   - Type in `git config --global user.name "YOUR_NAME"` and hit enter. If you want to change your name or you blindly copied and pasted, you can run this command again anytime.
   - Type in `git config --global user.email "MY_NAME@example.com"` and hit enter.
[//]: # (git doesn't actually verify your email address for the above command and github doesn't check your commits, so you _could_ theoretically commit as a person you arent...)

## 3 Your first git repository
The simplest use for `git` is <s>copying</s> *helping contribute to* others's code. This is known as `clone`ing. Let's copy all the files in this here `intro` repository.

> **repository**: A collection of files. *Local repositories* are ones on your computer. *Remote repositories* are ones on the web (github), or other peoples' computers.

1. `cd` so that you are inside the `USRC` directory. You may already be in the `USRC` directory - can you remember how you would find this out?
2. Scroll up to the top of this page and press the **BIG GREEN "Clone or Download" BUTTON** under the header. You will see Clone / HTTPS / a link. Copy that link.
3. Type into your command window: `git clone https://github.com/usydroboticsclub/intro.git`. (Yep, that's the link you just copied. You can `ctrl-v` it in on windows, or `ctrl-shift-v` on MacOS and Linux.
4. Press Enter. You should see something like this:

```
Cloning into 'intro'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 675 bytes | 51.00 KiB/s, done.
```

5. Go into the directory you just created using git clone by typing `cd intro`.
6. List all the files in this directory. (Do you remember how?) Check that these are the same files that are in this repository, if you scroll to the top.
7. Open your file explorer (Do you remember how?) Click on `Completed.md` to open it with your text editor. (If you don't have vscode or atom or notepad++ on your computer, you may have to "open with" notepad or some other text editor.) 
8. Check out all the cool people who have done this tutorial already!

And that's it! If you want to practice this, then why not try cloning some other stuff on github, like [this one](https://github.com/rick/roll). 

## 4 Getting started with github
You can use git with 2 computers directly, but chances are that you don't have two computers on hand; so instead we'll have to use github as a third party. Let's get you signed up to github.
1. Go here: https://github.com/
2. Sign up, in the top right corner.
3. That's it. Github is nice and easy.

## 5 Fork this repository
The polite way of making changes to a repository on github is to copy it to your own github repository. This is called forking, and happens ALL on github. 

1. Scroll up to the top of this webpage, and find the `Fork` button in the top right corner. Press that button. 

> **Fork:** To create a copy of someone else's repository in your personal repository.

2. Once the repository is forked, continue the tutorial on your forked version of this repository. (Yes, that means close this window and skedaddle over. We'll come back here the long way around.)
3. `cd` back to the `USRC` directory, and make a directory called `my_fork`. (Do you remember how to make a directory?)
4. Clone your fork of the repository. (Do you remember how?)
   - Do not reclone the usydroboticsclub version! If you accidentally do that, then use your file explorer to delete the `intro` folder.
4. Since this is your copy, you are the owner, so you can change it willy nilly. Let's go do that now.

## 6 Your first changes
Now, we'll make some changes to this very repository, and tell Git that we've done so git will save it for us.

1. In **your** version of the repository, open the `Completed.md` file using a text editor.
3. Type your name on the end of `Completed.md` with your favourite text editor. I recommend getting [VSCode](https://code.visualstudio.com/) for all platforms.
4. Save your changes. 
5. Go back to your terminal window, and type in `git add .`. This tells git to look at all the changes you made, and prepare them for sharing. 
6. Now type in `git commit -m "Added my name"`. This tells git that you're sure you want to make these changes, and tells git to tell other people that these changes pertain to adding your name. (The `-m` stands for message. You must have a message with your changes, because git likes to **enforce** good coding practice.)
7. Now type `git push`. This tells git to pass your changes to github. You may have to login using your github username and password (or your email and password).
   - If you get `Permission Denied`, then you've copied the usydroboticsclub repository, not your fork! You need to delete this `intro` folder using your file explorer and start again :(
8. Visit your forked repository now on github, and check that the `Completed.md` file now has your name. 

A summary of the steps we did:
```
1. Make changes
2. git add .
3. git commit -m "some meaningful message please"
4. git push
```

## 7 Making a pull request
Now that you've made some changes to your local version of git, you'll want to make a pull request, so that we can sign off your work in our repository.

> **pull request**: a polite way of asking a project owner to accept your changes.

1. Press the `Pull requests` tab on your own github repository.
2. Click `New pull request`, then click the green button that says `Create Pull Request`.
3. Wait for us to approve it. (Github will send us an email - and if you're in one of our live tutorials, we'll get to you pretty quick.) 
4. Great! Your name is now on our list. Welcome to the club! And congrats on learning `git`!

There's still plenty more to learn, but if you've gotten up to here then you'll know enough `git` to follow on to more interesting things in our library. If you're in one of our weekly tutorials, see you next week! Otherwise, feel free to check out more below or in our [library](https://github.com/usydroboticsclub).

## 8 Extension: Branching
This file's getting pretty long! To unlock the other extras in this tutorial, let's teach you `git branches`!
1. `cd` to the `intro` folder of either our original repository or your copy. 
2. Type in `git branch`. This will list out the branches that are available.
3. Choose a branch that catches your eye, and type `git checkout <branch-name>`. I'd recommend, in order of usefulness:
```
git checkout making-a-repository
git checkout how-to-merge (how-to-merge-2 is related and intentional) [TODO]
git checkout merge-conflicts (merge-conflicts-2 is related and intentional) [TODO]
git checkout git-ignore [TODO]
git checkout git-history [TODO]
git checkout fun-with-terminal [TODO]
git checkout more-about-git [TODO]
```
