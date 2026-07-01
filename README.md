# FOSSIERGlaze

*Fork with extra distros and niri setup in fossierglaze --setup tiling. Feel free to issue any distro you'd like me to add or fork this fork (or the original source) to do so and tinker a bit more with the program. :3*
*Shoutout to szoltysek for making this awesome larpmaxxing package. 🫶*

***

### Why just use Linux when you can rub it in everyone's face on Discord?

All of your Discord friends need to know that you are currently on a Linux system instead of Windows. FOSSIERGlaze solves this existential crisis by plastering your distro of choice all over your Discord profile.

#### Features:

- Smart Distro Detection: Automatically figures out what you're running by reading /etc/os-release.

- The Most Important Feature: Sets your status to "i use arch btw" if it detects an Arch-based system. Let's sort Linux users and Arch users.
    *Artix Linux now has it's own "i use artix btw."*

- Fallback Support: A respectful "i use linux just in case" for... everyone else (Debian, Fedora, etc.).

- Gaslight Your Friends: Use fossierglaze `--distro` gentoo to pretend you've spent 3 days wasting your life - other XXXtoo forks aren't supported yet. Go find a life purpose and stop building these distros.

- Safe, Sudo-Free Autostart: A handy fossierglaze --setup systemd command that installs a user service (no sudo needed) and just works.

- Tiling WM Support: fossierglaze --setup tiling will print the exact exec-once lines for your "saucy" Hyprland, i3, *or niri* config.

### Installation
*This is* ***not*** *on the* ***AUR*** *yet, registration is currently disabled.*

If you're not on an Arch-based distro, I don't know what to tell you. Clone the repo, install python-pypresence (`pip3 install pypresence`), and run python3 fossierglaze.py.

### Usage (After Installing)

After you install it from the AUR, you have two choices:
1. *Peasant Mode* (Run it manually)
Just run fossierglaze in your terminal. It will stay running. Close the terminal, it dies. Simple.

2. ***King Mode*** (Make it start automatically)
You want this to run every time you log in, right? Right.
Run this one command. It does not need sudo and is 100% safe: `fossierglaze --setup systemd`
This will ask you for permission, then automatically create a user service file at *~/.config/systemd/user/fossierglaze.service* and enable it. It will now launch when you log in and restart if it ever crashes.

#### For Tiling WM Chads
If you don't use a DE and laugh at systemd user services, just run:

`fossierglaze --setup tiling`

It will print the exact exec-once line you need to paste into your hyprland.conf or i3/config.

#### IF IT DOESN'T WORK (IT DEFINETELY SHOULD):
You're going to run this and see *FOSSIERGlaze Error: Could not connect to Discord.*

You will say, "but my Discord is open??? duhhhhhh"
I know. The stable Discord client on Linux is... special. Its RPC socket is notoriously broken.
**The Fix**: Use **Discord Canary**! This is the fix. 99% of the time, this is the entire problem. Stable is for horses, Canary is for users.
And then:
- Run Discord Canary.
- Run fossierglaze.

It will now work. Also, make sure "Activity Status" is enabled in your Discord User Settings -> Activity Privacy, but you already checked that, right?

### Forking & Adding Your Own Distro

*Want to add your special distro that only you and 3 other people use? Request it under an issue or fork this repo (or the original repo) and create your own Discord application.* 

### License
GPL-3.0. Go nuts. Do whatever you want I guess.
