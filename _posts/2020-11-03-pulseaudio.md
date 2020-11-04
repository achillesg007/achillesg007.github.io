---
title: PulseAudio shenanigans
tags: Linux
article_header:
  type:overlay
  background_color:"990012"
key: pulse-audio
---

When pulseaudio gives you lemons make Lauwiliwilinukunuku’oi’oi

<!--more-->

## The problem
Headphones stops working after sleep. Speakers work fine.

## The solution
Go to `/etc/pulse/default.pa`
comment out the line:
```bash
load-module module-switch-on-port-available
```

### OpenRC

You don't have systemctl on openRC so manually restart pulseaudio:

```bash
pulseaudio -k
pulseaudio --start
#this should work on both openrc and systemd
```

## The other problem
Sometimes problems look like they're from pulseaudio but actually no:<br>
If you broke something in the xfce config and have to boot using tty,
There's a chance that it starts with no audio.

## The other solution
make `~/.initrc`<br>
append `exec startxfce4`

