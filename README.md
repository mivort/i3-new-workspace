# i3-new-workspace
Automatic workspace creation script for i3 tiling window manager
(http://i3wm.org/). Sway is also supported (https://swaywm.org/).

## Usage example
Add something like this to your `i3/config` file:

    # press ~ to claim a new workspace
    bindsym $mod+grave exec --no-startup-id i3-new-workspace
