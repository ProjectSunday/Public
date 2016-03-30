## Virtual Machine Setup

1. Download Ubuntu.iso from [Ubuntu.com](http://ubuntu.com)
2. Download Oracle VM Virtual Box - [virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
3. Install Virtual Box
4. Install Extensions for it
5. Create a new virtual machine
 * Give it at least 1.5GB of RAM, no more than 50% of total RAM
 * Create new Hard Disk, VMDK, Dynamic, 2GB split checked
 * HDD Space, 12-20 GB is typically good.
6. Right-Click > Settings
 * General > Advanced > Bidirectional Clipboard and Drag/Drop
 * System > Processor > Usually you want 2 processors, no more than half of your total (if you have 8 cores, pick 2, 3, or 4).
 * Display > Screen > 32MB of Video Memory is usually plenty. No more than 50% (okay to aim low if you have little to spare, 16MB works fine too).
 * Storage > Optical Drive Dropdown > Choose Virtual Optical Disk File > Ubuntu.iso you downloaded in step 1
7. Start up VM
8. Install Ubuntu
 * Make your password something easy like the number 0. Ubuntu will ask you to type it in every .3 miliseconds, you'll thank me later.
 * Automatic Login
 * Install updates while installing the OS

## Setting up your OS

9. Install updates, reboot, install updates, reboot, etc.
10. In the Virtual box menu > Devices > "Insert Guest Additions CD image..."
11. Install Virtual Box stuff and reboot when done. Eject fake disc if it's still in there.
12. Back in Ubuntu > System Settings > Brightness & Lock > Never | Off | uncheck require pw
13. Change desktop background if you want by Right-clicking it
14. Open Firefox, adjust all the browser settings to your liking.

## Uninstall Software

15. Start button at top of dock > Applications button at bottom of screen > Installed (See X more results) > Right-click on a program to uninstall
 * Anything Libre Office
 * Landscape
 * Anything else you don't need, like games or Thunderbird Mail

## Install Software

16. [sublimetext.com/3](http://sublimetext.com/3) - download the .deb file and run it. It will open the Software Center. Click Install. Open it and lock to dock.
17. Any other browser you want, like Chromium or Opera, or just stick with Firefox

## Set up Dev environment

18. Open up terminal and run the following:
 * `sudo apt-get update`
 * `sudo apt-get install unity-tweak-tool`
 * `sudo apt-get install compizconfig-settings-manager`
 * `sudo apt-get install -y nodejs`
 * `sudo apt-get install -y build-essentials`
 * `sudo apt-get install npm`
 * `sudo ln -s /usr/bin/nodejs /usr/bin/node`
 * `sudo apt-get install git`
19. [syntevo.com/smartgit/download](http://syntevo.com/smartgit/download) - **Scroll down** and find the Debian package > Download and Install SmartGit
20. Open Files > Computer > Home > drag your user folder into sublime text after opening it to create a sidebar.
21. Create a GitHub folder in your user folder (`mkdir ~/GitHub`)
22. In ST3 open `~/.bashrc` and add this at the bottom and save:

    ```
    alias dir='ls'
    alias cd..='cd ..'
    alias cls='clear'
    alias csl='clear'
    alias home='cd ~/GitHub
    clear'
    ```
23. Open SmartGit
 * I understand/Non-commercial > Next > I confirm soley > OK
 * Leave Username/Email blank > next
 * User SmartGit as SSH client > next
 * GitHub > Generate API Token > Use GitHub password for Master Password > OK
 * Browser launches > Log in to Github if not already > Copy code > paste it into SmartGit > Authenticate > Accept > Next
 * Uncheck auto-send crash > Finish
 * Clone Existing Repo > OK > Dropdown > github.com > pick repo > Select > Next
 * Include Sub Check | Fetch all Check | Create Up Uncheck > Next
 * Path: `~/GitHub/Whatever your repo name is`
24. Open Sublime Text
 * Go to [packagecontrol.io](http://packagecontrol.io) > install now > copy the code
 * In ST3 > `CTRL + ~` > Paste > `Enter` > OK > `ESC`
 * `CTRL + SHIFT + P` > Install > `Enter`
  * PackageResourceViewer
  * Sidebar Enhancements
  * BufferScroll
  * Trailing Spaces
  * Sass
  * EditorConfig
  * Monokai JSON+
  * Pretty JSON
  * Text Pastry
 * `CTRL + SHIFT + P` > PackageResourceViewer: Open Resource > Theme - Default > Default.sublime-theme
    ```
    {
        "class": "icon_file_type",
        "content_margin": [0,0]
    },
    {
        "class": "icon_folder",
        "content_margin": [0,0]
    },
    {
        "class": "icon_folder_loading",
        "content_margin": [0,0]
    }
    ```
 * `CTRL + SHIFT + F` > Where: `~/Github, -*/node_modules/*, -*/.git/*, -*/bower_components/*`
 * Menu > Preferences > Settings - User >
    ```
    "folder_exclude_patterns":
    [
        "Application"
    ],
    ```

## Customization:

25. Remove junk from sidebar (Libre Office, Amazon, etc.) and add stuff to it. Here's what you should have:
 * Start Button
 * Ubuntu Software Center
 * Files
 * SmartGit
 * Firefox
 * System Settings
 * Sublime Text
 * Software Updater
 * Terminal
26. Start > Search: "CompizConfig Settings Manager"
 * Uncheck all Effects and Animations and Fading Windows
27. Open Files > Home > `CTRL + H` (unhide files)

