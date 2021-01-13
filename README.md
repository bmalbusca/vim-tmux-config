# Config. files for your Terminal :blue_book:
### Vim configurations files to Linux and MacOS

For use this configuration files you need Vim and/or Tmux installed on your terminal, and you will need create/update these files:

- .vimrc    (``` yourterminal@console: vim  ~/.vimrc ```)
   - Plugins
     - preservim/nerdtree
     - airblade/vim-gitgutter
     - Valloric/YouCompleteMe
     - wakatime/vim-wakatime
- .tmux.conf (``` yourterminal@console: vim  ~/.tmux.conf ```)
  - First steps
     1. Adjust the keys combo to yourself. Like the keys for open new windows. ex: 'ctrl-q' + '-' | '\ '
     2. Memorize keys for: how to move the coursor over windows and how to resize window panes 

Also, you will need some packages installed on Vim or Terminal:

 - *Vundle* : https://github.com/VundleVim/Vundle.vim
 - *Powerline* : https://github.com/powerline/powerline
 
 
Other essentials:

 - *Oh My Zsh* : https://ohmyz.sh  (See first if Zsh makes sense to you, over your Bash already configured)
 
 
> **_NOTE:_**  *In this file is missing some packages installations and other bash things, but you will figure out how to resolve the errors and warnings asking your friend Google* :mag_right:
>
> You should link your `.bash_profile` with `.bashrc` to see the same terminal styling in tmux. Add '`source ~/.bashrc`' to `.bash_profile` [(ref)](https://askubuntu.com/questions/925881/tmux-colors-not-working).
 
 ____________________________
 
 # Tmux 2.8.x to 2.9.x migration from [this issue](https://github.com/tmux/tmux/issues/1689)
 
 ```
 ########################################################################   
#   file: ~/.tmux.conf
#   version: 2.8.x -> 2.9.x 
#   note: change '*-<style_type> <value>' to '*-style <style_type>=<value>' 
#         or in some cases where '*-attr <attribute_val>' change to '*-style  <attribute_val>'
#   styles:             
#             message-command-style style
#             message-style style
#             mode-style style
#             pane-active-border-style style
#             pane-border-style style
#             status-left-style style
#             status-right-style style
#             status-style style
#             window-active-style style
#             window-status-activity-style style
#             window-status-bell-style style
#             window-status-current-style style
#             window-status-last-style style
#             window-status-style style
#             window-style style
#
#######################################################################
 
 ```
 
 # Screenshots
 
 
 1. Linux (Ubuntu)
 ![Linux screenshot](Linux_conf/linux.png)
 
 2. MacOS (Mojave)
 ![MacOS screenshot](Macos_conf/mac_terminal.png)
 
