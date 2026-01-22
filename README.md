Dec 21 12:30 PM:

what is toes. Branching: with the help of branching, we can create a copy of file that we are working on, we can make changes independently in our own branch without impacting the

original branch, once our changes are good, we can merge our changes with our original file.

Repository: It is a place for our project that contains files and versions. Commit: A saved snapshot of our code at a time.

Pull Request: Request for our code to be merged into another repo or branch.

Staging: group of changes are there to go before committing them. Clone: Local copy of remote repo.

Merge: Combine the changes from one branch into another branch.

Push: Upload our commits from our local copy to remote repo.

Pull: Fetch and get the changes from remote repo to local copy.

Fork: fork is used only in GitHub and GitLab platforms to creating the some one else repo, and we can make changes independently.

GitHub: GitHub is cloud based platform, which allows us to host and collaborating on Git repositories.

To know about where git installed on our machine: use command "which git" then the output of this command displays the path of git binary. know the git who we are, we need to set global configurations, because while committing the code, git will thrown an error that who you are.

To so, to config our name and email we use below commands.

1. git config --global user.name "Spandana Ravula"

2. git config --global user.email "spanda****8" We can remove our name and email also using below command:

1. git config --global unset user.name

2. we create a folder ex "git made-easy" and open it in VS code, and create new files in it such as script.py and project.txt and save them.

Initialize the Repo:

1. we open GitHub and create a new repo ex "git made-easy"

3. now we initialize the git made easy folder as a new repository. 4. to check status of our local repo: git status, this command will show how many files needs to staged.

5. to add all files to staging area: git add to unstage the files: git rm file names.
8. then again execute git status commands, if it gives output as nothing to commit, then all your files are in staging area.

9. then to add remote repo: git remote add origin <remote repo URL> 10. git branch -M main (m flag is used to rename the branch name)

11. git push -u origin main (it uploads our local main branch to remote origin branch)

Jan 2nd/26 9PM:

for ex, if we want to contribute some code on public repository and others also working on same repo, they also making some changes to that repo, to contribute that

GitHub Workflow from remote-local:

first we need to create local copy of remote repo, so for that we use git clone. 1. git clone cepourl: it will copy the entire repo from remote repo to local machine.

git fetch: since other people also working and they are also making some changes to the code, so git fetch will only download those changes what other people did but it will not update our local dir or files.

2.

3. git pull: git pull will fetches the changes made by other developers and also merges them to our current branch/code. 4. sometimes it leads to conflict, so that is why first we need to use git fetch.

GitHub Workflow from Local-Remote:

for ex, when we want to push our local code to remote repo or same public repo. 1. first we need to do git add, which push the changes to staging area

2. then we do git commit with message which describe the changes.

3. then do git push, to push all the changes we made at local to remote repo.

Jan 3rd/26 3:30 PM:

1. to do git clone, first we need to create any directory in our local and open it with vs code, then go to Github, copy https url of remote repo, the execute git clone <url>, then that remote repo is downloaded in our local file system with the exact same remote repo name.

2. once the repo in our local system, if we want to add some code to readme file, we added some code to file, then that file turns into yellow color, that means the

file have been modified, then to add that file to staging area we do git add file name, then do git status, that file will be green color and in staging area. 3. to unstage the files git restore-staged <filename>.

4. then do git commit -m "message"

5. then do git push

Jan 4th 2:30 PM: Branching

1. Head is a pointer to the current branch.

2

How to create new branch: git branch <branch name> so, when we executed this command, it creates new branch based upon the current branch we are in. and it doesn't

switch immediately to that branch.

4. when we want to create new branch and switch to that branch: git switch -c <branch name>, this command will create new branch and switch into that branch.

2. To list out the existing branches: git branch

3. To switch into b/w the branches: git switch <targetbranchname>

1. lets assume we have index.html file in the main branch, now we want to add some code to index.html file. so for that I have created a one feature branch called

Lets work on git branches:

"new-feature" by executing command git switch -c new-feature (c flag lag indicates create) 2. Now I switched into new-feature branch and I added one line code that is one heading(h1) to index.html file.

3. then to commit that one line code, we did git add and git commit to the new-feature branch.

4. if we want to see the difference between the two branches we can use this command: git diff main new-feature (it will displays the changes in terminal) 5. now to merge the new feature branch changes into main branch, first we need to switch main branch (where we doesn't made any changes) and we need to execute the

command like- git merge new-feature (the branch name where we made changes)

6. Note: to do the merge, first we need to be in the branch where we doesn't made any changes and execute git merge <branch_name> (where we made changes).

.gitignore:

I

1. gitignore file is a plain text file, where we can list the files or file types that we don't want git to track.

2. we can create git ignore file in GitHub and as well in vs code.

3. let's say we don't want to track log files such audit.log and crash.log files, so for that in vs code, I have created one gitignore file and I have written that

*.log then got will not track any log files.

3. to know the files which are not tracked by git: git status-igored, this command will displays the file name which are not tracked by git.

Jan 19th 10:40 AM:

git log: git log command is used to showcase the history of git commits on that particular directory. In the history of commits, it displays commit id, author name,

commit date, and commit messagae what we given at the time of commit.

If we want to see the few latest commits, let's say 4, then execute git log -n 4

gone, to revert them back to file, we execute "git stash apply" command.

Git Stash: git stash is used to save the changes to our local file, for ex we made some changes to our file and to save them we execute git stash, then all the changes gone, to revert them back to file, we execute git stash apply command.
Git revert: git revert command is used to undo the changes, for ex: you have typo mistake in your file or you commited some unwanted code without observing it, then you want to delete that code from your file, at that time we can use git revert command to undo the changes what we made.

process: git log and get the commit id

git revert <commit id of where you committed unwanted code or typo mistakes>

Git fork: It is used to create the copy of repository from the someone else account to our account, and we can work on their repo, without impacting the original

source code.
  
