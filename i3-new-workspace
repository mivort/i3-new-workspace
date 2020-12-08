#!/bin/bash
# Based on https://github.com/sandeel/i3-new-workspace
# Script occupies free workspace with lowest possible number

# Use swaymsg if WAYLAND_DISPLAY is set
WM_MSG=${WAYLAND_DISPLAY+swaymsg}
WM_MSG=${WM_MSG:-i3-msg}

WS_JSON=$($WM_MSG -t get_workspaces)
for i in {1..10} ; do
    if [[ ! $WS_JSON =~ \"num\":\ ?$i ]] ; then
        $WM_MSG workspace number "$i"
        break
    fi
done
