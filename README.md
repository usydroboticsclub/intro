# Two ways to make a repository
The three most common ways `git` starts to get involved in a project are:
1. You find someone's project on github. You go: Cool! I'll check it out! You clone the repository.
2. You write some code. You think: Hey, it'd be great if I shared this with the world! You push to github.
3. You start a group project. You think: We're probably going to be collaborating a lot. You create a repository on github and start there.

We've already covered case 1. This tutorial covers cases 2 and 3.

## Pushing existing code to github
Say you have some existing code you want to push to github. Let's create that now:

1. Go to your `USRC` folder and make a new directory called `my_repo_from_local`.
2. Make a couple of files inside `my_repo_from_local`.

Great! Now, let's push it to github.

1. `cd` into `my_repo_from_local`.
2. Tell `git` that you want `git` to care about this directory you just made, by typing `git init .`
3. Go to [https://github.com](https://github.com) and log in if you haven't already.
4. Press the little green `New` button to create a new repository.
5. Call your repository `my_repo_from_local`. Don't check any of the checkboxes on the bottom.
   - This doesn't have to match up your folder name, but its usually nice if it does, since other people cloning will make the folder names match.
6. Don't check `create a readme` or `create a .gitignore` or any of those options!!
7. Press `Create Repository`.
8. You can follow the steps in the "Upload an existing repository" step - we'll explain them here.
   - `git remote add origin https://github.com/your-username/my_repo_from_local.git` tells git: Hey, there's a repository up in the cloud at this address, and we'll call it `origin`.
   - `git branch -M main` tells git: Make the `main` branch the main branch. Old `git` uses the `master` branch as the main branch, but some people figured that the term `master` has its roots in slavery and they prefer `main`. This step is optional.
   - `git push -u origin main` tells git: Give `main` to `origin`, and `origin` happens to be github, so give main to github. 
      - Naturally if you skipped the optional step, type `git push -u origin master`.
9. And congrats! You should now have a repository on github. Refresh the page to check that the files you made are now on git.

## Starting on github and cloning
Say you thought ahead and started from github. You would.
1. Press the little green `New` button. 
2. Give your repository a name, and also check `Add a readme`.
3. `cd` to the `USRC` folder.
4. Clone your repository.

Easy peasy. 

That's all for this one! Check out the other branches available using `git branch`, then `git checkout <branch-name>`. You can `git checkout master` to check out the tutorial order.