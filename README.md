# git-imp-comands
-------------------
git reset --hard # removes staged and working directory changes

## !! be very careful with these !!
### you may end up deleting what you don't want to
### read comments and manual.
git clean -f -d # remove untracked
Note that git clean -f -d will delete files from ignored folders too. So all you local logs and things like that will be gone. Usually it's not a big problem, but it's better to know.

git clean -f -x -d # CAUTION: as above but removes ignored files like config.

git clean -fxd :/ # CAUTION: as above, but cleans untracked and ignored files through the entire repo (without :/, the operation affects only the current directory)

git clean -fxd can actually be REALLY dangerous if you don't know what you're doing. You may end up permanently deleting some very important untracked files, such as your database, etc. Use caution.

To see what will be deleted before-hand, without actually deleting it, use the -n flag (this is basically a test-run). When you are ready to actually delete, then remove the -n flag:
git clean -nfd

https://git-scm.com/docs/git-clean

# Git multiuser setup
--------------------
## To set git default editor as vs code
> git config --global core.editor "code --wait"
## to set diffrent user for diffrent git repo
> git config --global credential.github.com.useHttpPath true

## To Open global git config
> git config --global -e

## If nothing scaning for windows credential manager 
> git config --global credential.helper manager

## git checkout error Filename too long

>  git config --global core.longpaths true

**OR**
>  git config --system core.longpaths true


--system will set the variables for all users on the system, but what we are looking for is to the set it for currently logged in user.
