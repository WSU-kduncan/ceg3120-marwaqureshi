status
Shows status of the local repository. This status includes:
1) number of local commits that have not been synced with remote (GitHub)
2) list of files in local folder than are NOT being tracked by git
3) list of files in local folder that have changes that need to be committed
command: git status

clone 
Clones a repository into a new directory
1)Creates a copy of the target repository. The target repository may be a remote or local repository. The content of the clone can be changed with different configurations.
command: git clone

add
Adds file contents to the index
1) This adds a change in the working directory to the staging area. It allows Git to understand that you want to updates some file(s) in the next commit. However, changes cannot be made until you run the commit command.
command: git add

rm
Removes files from the working tree and from the index
1) It can be used to remove individual files or a couple files. It removes tracked files from Git index, and may do the same in staging index and working directory. However, this command does not remove branches.
command: git -rm

commit 
Records changes to the repository
1)Stores the current contents of the index in a new commit along with a the message that the user adds when commiting. When the user runs the command git add, git commit is the next command that actually commits those changes that were made when you added the file.
command: git commit

push
Update remote refs along with associated objects
1) Used to upload local repository content to a remote repository. Push command can be specified to branch.
command: git push

fetch 
Downloads objects and refs from another repository
1) It downloads commits/refs/files from local repository. When downloading content from remote repository, git pull and fetch commands get the work done. Fetch downloads the remote content, but does not update the working stage of local repository, which makes it better. 
command: git fetch

merge 
Join two or more development hisstories together
1) This joins the changes from the named commits into the current branch. Integrates independent lines of development into a single branch.
command: git merge 

pull
Fetch from and integrate with another repository or a local branch
1) Serves as a combination of git fetch and git merge.
2) Without git pull the local repository will never be updated from the changes in remote repository
command: git pull

branch 
Allows you to list, create, or delete branches
1) This command does NOT let you switch between branches. However, you can do a couple different things from the base of this command such as rename a branch as well. For exmaple, if i wanted to use the git branch command to list all the branches, I would do git branch --list
command: git pull

branch 
Allows you to list, create, or delete branches
1) This command does NOT let you switch between branches. However, you can do a couple different things from the base of this command such as rename a branch as well. For exmaple, if i wanted to use the git branch command to list all the branches, I would do
command: git branch

checkout 
Switching between different versions of a target entity such as a branch
1) checking out the branch lets you update the files in the working directory to match the version stored in that branch. It allows git to record all new commits on that branch.
command: git checkout

.git folder
1) .git is initialize by git init
2) It contains all information required for version control. When wanting to clone your repository you can do copy .git
3) It contains all information about commits, remote repository address, etc. 
command: ls -a 

.gitignore file
1) This tells GIT which files to ignore when commiting your project to the GitHub repository. 
2) It is located in the root direcotry of your repository
3) It contains sensitive data so you may want GIT so ignore the file.
command: touch .gitignore

pull request
1)Go to GitHub repo and click the fork button. This creates a new copy of the repo (demo repo) under your GitHub account. Clone the repo in terminal, then create a new branch and a new remote for the upstream repo. Make sure to create a new branch and make a little change and push to new branch ("new_branch). Then push and click on the "compare & pull request" button when it appears on GitHub. This will take you to a pull request screen and create a pull request. Now if you like you can merge if you want for some reason.

SSH authentication to repositories
1) Create SSH key in terminal using keygen and follow the process
2) Go to GitHub and settings and create a new SSH key while giving it a good title and copying the public key that was created in the terminal
3) Clone the Git repo with SSH
4) Run the clone "SSH" in the terminal
5) If asked yes/no, press yes until process is successfully done
SSH key Authentication done 
