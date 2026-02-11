<img width="1916" height="1038" alt="image" src="https://github.com/user-attachments/assets/91431758-f2fe-4205-8626-6121bae5aa8c" />


# Kitty terminal theme :
nano ~/.config/kitty/kitty.conf

```bash
#  _    _ _   _           _                      _             _  
# | | _(_) |_| |_ _   _  | |_ ___ _ __ _ __ ___ (_)_ __   __ _| | 
# | |/ / | __| __| | | | | __/ _ \ '__| '_ ` _ \| | '_ \ / _` | | 
# |   <| | |_| |_| |_| | | ||  __/ |  | | | | | | | | | | (_| | | 
# |_|\_\_|\__|\__|\__, |  \__\___|_|  |_| |_| |_|_|_| |_|\__,_|_| 
#                 |___/              _          _   _             
#   ___ _   _ ___| |_ ___  _ __ ___ (_)______ _| |_(_) ___  _ __  
#  / __| | | / __| __/ _ \| '_ ` _ \| |_  / _` | __| |/ _ \| '_ \ 
# | (__| |_| \__ \ || (_) | | | | | | |/ / (_| | |_| | (_) | | | |
#  \___|\__,_|___/\__\___/|_| |_| |_|_/___\__,_|\__|_|\___/|_| |_|

##########################################################################

# themes
include GruvBox_DarkHard.conf
#include Wryan.conf
#include VSCode_Dark.conf

# terminal opacity and blur
background_opacity 1.0
background_blur 1

# advance 
term xterm-kitty

# terminal bell
enable_audio_bell no

# os specific tweaks (Gnome window decoration for wayland)
linux_display_server x11

# font
font_family        SauceCodePro Nerd Font
bold_font          auto
italic_font        auto
bold_italic_font   auto
font_size 12.0

# font size management 
map ctrl+shift+backspace change_font_size all 0

# cursor customization
# block / beam / underline
cursor_shape block
cursor_blink_interval 0
cursor_stop_blinking_after 0
shell_integration no-cursor

# scrollback
scrollback_lines 5000
wheel_scroll_multiplier 3.0

# mouse
mouse_hide_wait -1

# window layout
remember_window_size  no
initial_window_width  1200
initial_window_height 750
window_border_width 1.5pt
enabled_layouts tall
window_padding_width 0
window_margin_width 2
hide_window_decorations no

# window management 
map ctrl+shift+enter new_window
map ctrl+shift+] next_window
map ctrl+shift+[ previous_window

# layout management
map ctrl+shift+l next_layout
map ctrl+alt+r goto_layout tall
map ctrl+alt+s goto_layout stack

# tab bar customization
tab_bar_style powerline
tab_powerline_style slanted
tab_bar_edge bottom
tab_bar_align left
active_tab_font_style   bold
inactive_tab_font_style normal

# tab management
map ctrl+shift+t new_tab
map ctrl+shift+right next_tab
map ctrl+shift+left previous_tab
map ctrl+shift+q close_tab
```

nano ~/.config/kitty/GruvBox_DarkHard.conf
```bash
# Selection Colors
selection_foreground     #ebdbb2
selection_background     #d65d0e

# Window border Colors
active_border_color      #8ec07c
inactive_border_color    #665c54

# Kitty tabs colors 
active_tab_foreground    #ebdbb2
active_tab_background    #458588
inactive_tab_foreground  #ebdbb2
inactive_tab_background  #8ec07c

# Basic color
background               #1d2021
foreground               #ebdbb2

# 16 main colors
color0                   #3c3836
color1                   #cc241d
color2                   #98971a
color3                   #d79921
color4                   #458588
color5                   #b16286
color6                   #689d6a
color7                   #a89984
color8                   #928374
color9                   #fb4934
color10                  #b8bb26
color11                  #fabd2f
color12                  #83a598
color13                  #d3869b
color14                  #8ec07c
color15                  #fbf1c7

# Cursor colors
cursor                   #bdae93
cursor_text_color        #665c54

# Url color
url_color                #458588
```


# Kitty help command
```bash
mkdir -p ~/.local/bin
nano ~/.local/bin/kitty-help
```
kitty-help file :
```bash
#!/bin/bash

printf "\033[1;36m
╔════════════════════════════════════════════╗
║\033[1;33m         KITTY SHORTCUTS               \033[1;36m║
╠════════════════════════════════════════════╣
║ \033[1;32mTABS\033[1;36m                                       ║
║ \033[0;37mCtrl+Shift+T\033[1;36m         \033[0;37mNew Tab\033[1;36m               ║
║ \033[0;37mCtrl+Shift+→\033[1;36m         \033[0;37mNext Tab\033[1;36m              ║
║ \033[0;37mCtrl+Shift+←\033[1;36m         \033[0;37mPrevious Tab\033[1;36m          ║
║ \033[0;37mCtrl+Shift+Q\033[1;36m         \033[0;37mClose Tab\033[1;36m             ║
╠════════════════════════════════════════════╣
║ \033[1;32mWINDOWS\033[1;36m                                    ║
║ \033[0;37mCtrl+Shift+Enter\033[1;36m     \033[0;37mNew Window\033[1;36m            ║
║ \033[0;37mCtrl+Shift+]\033[1;36m         \033[0;37mNext Window\033[1;36m           ║
║ \033[0;37mCtrl+Shift+[\033[1;36m         \033[0;37mPrevious Window\033[1;36m       ║
╠════════════════════════════════════════════╣
║ \033[1;32mLAYOUT\033[1;36m                                     ║
║ \033[0;37mCtrl+Shift+L\033[1;36m         \033[0;37mNext Layout\033[1;36m           ║
║ \033[0;37mCtrl+Alt+R\033[1;36m           \033[0;37mTall Layout\033[1;36m           ║
║ \033[0;37mCtrl+Alt+S\033[1;36m           \033[0;37mStack Layout\033[1;36m          ║
╠════════════════════════════════════════════╣
║ \033[1;32mFONT\033[1;36m                                       ║
║ \033[0;37mCtrl+Shift+Backspace\033[1;36m \033[0;37mReset Font Size\033[1;36m       ║
╚════════════════════════════════════════════╝
\033[0m
"
```

make it exacutable
```
chmod +x ~/.local/bin/kitty-help
```

add alias
```bash
# adding to .bashrc or .zshrc
echo 'alias khelp="~/.local/bin/kitty-help"' >> ~/.bashrc
# if you use zsh:
# echo 'alias khelp="~/.local/bin/kitty-help"' >> ~/.zshrc

source ~/.bashrc
# or
# source ~/.zshrc
```


fineal help command usage
```
khelp
```
