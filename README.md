# i3-new-workspace
Automatic workspace creation script for i3 tiling window manager
(http://i3wm.org/). Sway is also supported (https://swaywm.org/).

## Installation
Put `i3-new-workspace` script to any directory in your `$PATH`. This script
depends only on `bash` built-in methods and `i3-msg`/`swaymsg` (comes as part
of i3/Sway distribution).

## Usage example
Add something like this to your `i3/config` file:

    # press ~ to claim a new workspace
    bindsym $mod+grave exec --no-startup-id i3-new-workspace

    # press ~ + Shift to move current container to a new workspace
    bindsym $mod+Shift+grave exec --no-startup-id i3-new-workspace -m

    # press ~ + Alt to carry (move and focus) current container to a new workspace
    bindsym $mod+Mod1+grave exec --no-startup-id i3-new-workspace -c
