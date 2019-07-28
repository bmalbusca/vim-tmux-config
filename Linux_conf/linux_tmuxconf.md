# remap prefix from 'C-b' to 'C-a'
unbind C-b
set-option -g prefix C-q
bind-key C-q send-prefix
# split panes using | and -
bind \ split-window -h
bind - split-window -v
unbind '"'
unbind %

# Start window numbering at 1
set -g base-index 1

# loud or quiet?
set-option -g visual-activity off
set-option -g visual-bell off
set-option -g visual-silence off
set-window-option -g monitor-activity off
set-option -g bell-action none
# set 256 color
set -g default-terminal "screen-256color"
#  modes
setw -g clock-mode-colour colour5
setw -g mode-attr bold
setw -g mode-fg colour1
setw -g mode-bg colour18

# panes
set -g pane-border-bg colour0
set -g pane-border-fg colour19
set -g pane-active-border-bg colour0
set -g pane-active-border-fg colour9

# statusbar
set -g status-position bottom
set -g status-justify left
set -g status-bg colour18
set -g status-fg colour137
set -g status-attr dim
set -g status-left ''
set -g status-right-length 50
set -g status-left-length 20

setw -g window-status-current-fg colour1
setw -g window-status-current-bg colour19
setw -g window-status-current-attr bold
setw -g window-status-current-format ' #I#[fg=colour249]:#[fg=colour255]#W#[fg=colour249]#F '

# status bar theme

set -g status-bg 'colour235'
set -g message-command-fg 'colour222'
set -g status-justify 'centre'
set -g status-left-length '100'
set -g status 'on'
set -g pane-active-border-fg 'colour154'
set -g message-bg 'colour238'
set -g status-right-length '100'
set -g status-right-attr 'none'
set -g message-fg 'colour222'
set -g message-command-bg 'colour238'
set -g status-attr 'none'
set -g pane-border-fg 'colour238'
set -g status-left-attr 'none'
setw -g window-status-fg 'colour121'
setw -g window-status-attr 'none'
setw -g window-status-activity-bg 'colour235'
setw -g window-status-activity-attr 'none'
setw -g window-status-activity-fg 'colour154'
setw -g window-status-separator ''
setw -g window-status-bg 'colour235'
setw -g window-status-format ' #I#[fg=colour237]:#[fg=colour250]#W#[fg=colour244]#F '

setw -g window-status-bell-attr bold
setw -g window-status-bell-fg colour255
setw -g window-status-bell-bg colour1

set -g mouse on
bind -n WheelUpPane if-shell -F -t = "#{mouse_any_flag}" "send-keys -M" "if -Ft= '#{pane_in_mode}' 'send-keys -M' 'select-pane -t=; copy-mode -e; send-keys -M'"
bind -n WheelDownPane select-pane -t= \; send-keys -M
bind -n C-WheelUpPane select-pane -t= \; copy-mode -e \; send-keys -M
bind -T copy-mode-vi    C-WheelUpPane   send-keys -X halfpage-up
bind -T copy-mode-vi    C-WheelDownPane send-keys -X halfpage-down
bind -T copy-mode-emacs C-WheelUpPane   send-keys -X halfpage-up
bind -T copy-mode-emacs C-WheelDownPane send-keys -X halfpage-down

# To copy, left click and drag to highlight text in yellow,
# once you release left click yellow text will disappear and will automatically be available in clibboard
# # Use vim keybindings in copy mode
setw -g mode-keys vi
# Update default binding of `Enter` to also use copy-pipe
unbind -T copy-mode-vi Enter
bind-key -T copy-mode-vi Enter send-keys -X copy-pipe-and-cancel "xclip -selection c"
bind-key -T copy-mode-vi MouseDragEnd1Pane send-keys -X copy-pipe-and-cancel "xclip -in -selection clipboard"

set-option -g default-terminal "screen-256color"
#set g:ycm_global_ycm_extra_conf = '~/.vim/.ycm_extra_conf.py'

# messages
set -g message-attr bold
set -g message-fg colour232
set -g message-bg colour16
