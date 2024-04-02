# git-imp-comands

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
1. git config --global core.longpaths true OR
2. git config --system core.longpaths true
--system will set the variables for all users on the system, but what we are looking for is to the set it for currently logged in user.
