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

## Bibliography
* Bash Single vs. Double Quotes What's the Difference (https://www.tutorialspoint.com/bash-single-vs-double-quotes-what-s-difference#:~:text=In%20summary%2C%20main%20difference%20between,them%20as%20a%20literal%20string.)
* How to Customize Bash Prompt in Linux (https://phoenixnap.com/kb/change-bash-prompt-linux)

## Table of Contents
- [[alias]]
- [[bash_setup]]
- [[communication]]
- [[migration_phx_site_from_digital_ocean_to_gigalixir]]
- [[Debuging_Elixir]]
- [[design system]]
- [[Elixir]]
- [[elixir_configuration]]
- [[elixir_exports]]
- [[elixir_phoenix]]
- [[emacs]]
- [[event_sourcing]]
- [[File_Tree_Tools]]
- [[foam_extensions]]
- [[gigalixir]]
- [[git]]
- [[git_commands]]
- [[git_tags]]
- [[git_workflow]]
- [[Phoenix.LiveView]]
- [[livebook_smart_cells]]
- [[ice_breakers]]
- [[mc]] (Midnight commander)
- [[ecsx_game_evelopment]]
- [[postgres]]
- [[postgres_installation]]
- [[rexbug]]
- [[process_boundaries]]
- [[silversearcher-ag]]
- [[sql]]
- [[speed_test]]
- [[supervisor_vs_linking]]
- [[tailwind_css]]
- [[tailwind_CSS_Justin_M]]
- [[zettelkasten]]
- [[Zettelkasten]]