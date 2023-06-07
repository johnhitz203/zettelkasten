# Bash Setup
This describes how my linux Bash terminal is currently setup.

## asdf
* Add asdf to path
  * . "$HOME/.asdf/asdf.sh"
## BASH Promt changes
* Display git branch in terminal prompted
  * create a function `git_branch` that reads the git branch info
  * Call the function in the string that defines my terminal prompt and assign it to PS1
```Bash
git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}

PS1="${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\W\[\033[00m\]\$(git_branch)\$ "
```
* Syntax Notes
  * Single Quotes - Bash interpret everything inside single quotes as a literal string
  * Double Quotes - Bash interprets variables and specific characters in a special ways
  * Limit Prompt to Working Directory v Current Working Directory 
    * w - CWD
    * W - Basename of the working directory 
  * BASH Prompt Reference: (https://phoenixnap.com/kb/change-bash-prompt-linux)

## Emacs Alias
* alias emacs='flatpak run org.gnu.emacs'


## Placed .bashrc in github repo
1. Moved .bashrc from `~$` to `~/config_repos/bashrc`
2. Created a local repo in `~/config_repos/bashrc`


[configuration_repos] A directory that contains my configuration files for various and sundry tools
[flatpak]