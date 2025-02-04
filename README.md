# Arch Guides

# ![DWMch Linux](img/dwmchlinux.png "Arch Linux w/ DWM")

An easy to follow list of arch guides that helps you setup your system however you want but offers you the option of my window mananger that i use and personally recommend suckless dwm and the whole suckless tools like st and slock etc.

## Enable Networking and Wi-Fi (Don't forget!)

You can safely ignore this if you do not wish to use networking or have internet connectivity and / or Wi-Fi otherwise please follow the below insturctions:

To enable Networking and Wi-Fi go to [This Guide](https://github.com/tilas01/arch-guides-all/blob/main/Other%20Guides/Setup%20Wi-Fi%20with%20iwd%20and%20NetworkManager%20and%20systemd-resolved%20on%20Arch%20after%20Install.md) inside this repository. If you forget to follow some of these steps you WILL BE left WITHOUT internet connectivity!

## Fix for Networking and Wi-F if you ignored the above when installing.
#### Note if reading this before installing: It is STRONGLY unrecommended to ignore the previous headings information if you wish to have networking snd Wi-Fi connectivity on your system after install.):
```
Mount your system again AFTER install, also keep in mind
if you setup your install with LUKS and/or LVM you will
need to open the cryptsetup and point to the correct logical
volume etc to be able to mount the correct partitions / volumes to arch-chroot
in as you did when installing. You can do another arch-chroot by booting off an
arch iso the same way you did to install Arch Linux as enabling networking requires
network and wifi tools to be installed in arch-chroot before the system itself has wifi
access so the only way to download this software to the system is through arch-chroot.
Avoid having to go through this tidious process if you can by remembering to install this
software at install time! I've only put this is here if you somehow forget.

I wont be writing a guide on how to do this specifically step-by-step as its only a fix IF you forget.
```
## My Arch Linux + Suckless Tools (DWM) Rice.
An example of how Arch can look just about any way you want it to!
Here is an example of my own DWM and custom tools that I have configured and compiled with a custom config for my personal needs and preferences. Suckless Tools allow you to customise them by changing the source code and recompiling in order to stay extremely minimal, fast and versatile as you can literally add any feature to it you want if you write it or apply it via the public patches they have for each project! The Arch Linux DWM + other [Suckless Tools](https://suckless.org)  (The developers of DWM, st (my terminal) and all my other desktop setup tools. Their website contains many helpful insites on how to code efficiantlly for example [these HTML websites](https://suckless.org/sucks/web/) quite *bluntly* explaining the key of simplicity in web design). I use the following for my desktop developed by the suckless devs: dwm (window manager), st (suckless terminal), dmenu (top bar menu), slstatus (suckless status monitor), and slock (suckless lock screen). If for some reason you want to copy it my dotfiles, wallpapers and all suckless tools including my configuration changes and applied patches are all public on my github account although keep in mind the versions of these programs may be a bit outdated as they were originally downloaded and configured in 2021, note I also use PyWal to achieve my terminal colour scheme. Anyway here is my persoanl custom desktop setup, fully using [Suckless Tools](https://suckless.org) such as DWM etc. It goes without saying that I strongly recommend [Suckless Tools](https://suckless.org) and support the Suckless Devs projects as should you please do check them out! (i slightly rushed this edit in gimp but i hope it still serves its purpose as an example haha)

![DWM Setup](img/mydwmsetupedit.jpg "My DWM Custom Setup - Edited")

Contents
========

 * [Disclaimer](#disclaimer)
 * [Why?](#why)
 * [Requirements](#requirements)
 * [Use](#use)
 * [Features](#features)
 * [To-Do](#todo)
 * [License](#license)

### Disclaimer

---

I do not claim to own the rights for the Arch Linux Logo used for the "DWMch Linux" photo I edited from the official Arch Linux Logo at the beginning of this README file and am simply modifying it for comedic purposes and to make my project look nicer under fair use. If the rights holder has any issue with this please contact me at any time and it will be removed from this repository. I do not have any affiliation with the Official Arch Linux project.

I am not responsible for any damage to software, hardware or data from following these instructions although I have tested and successfully installed arch with no issues in a vm following. Before following these guides, first and if you are more of the precautious type or just likes to practice go ahead and follow these guides on vms and let me know if anything is wrong please! It is greatly appreciated and helps everyone!



I wrote this code based on the Arch Wiki in 2021, im sure it may have changed some since then and I am aware of the arch-install command if I had heard about it may of not written all this but I dedicated a lot of time and testing to this. Although most of all the testing was also done in 2021-2023 so there is a chance you run into errors but i've used this guide to install arch on my own laptop and had no issues. Im definetly going to be using these guides myself soon so they will be updated and tested to be for sure working in 2025 soon.



Also make sure to check in other guides thats where you learn how to setup wifi etc and its easier to do some things at install so check that out before you go ahead and install.



Thats all thanks for using my guides I do hope they help you!

### Why?

---

I just wanted to make a repo where anyone could just follow along and install arch and start using it, I wrote this before arch-install was around and have kept it up to date but there is a chance of outdated information although i doubt it, please let me know if you run into any issues so i can fix it and no one else does!

### Requirements

A virtual machine - great for practice, if you're on linux i recommend QEMU.

Physical hardware - arch is not resource intensive and can run on very old computers, if you are using an old computer i recommend you follow the dwm and suckless tools part of this guide and dont opt for something like kde or gnome as they can be far more resource intensive and once you setup custom keybinds learn how it all works you will not only have learn something but also have a more smooth customised workflow exactly how you want it and if you want to add any features just patch your dwm, st etc.

A basic good general understanding a grip on how linux and unix systems work to troubleshoot any errors along the way and maintain your system.

---

### Use

Ensure you know whether you are using BIOS or UEFI, if i had to guess you are probably using UEFI. The only exclusion to this rule is virtual machines with weird settings or very old computers which i have guides for if you are using BIOS also. If you dont know just try the UEFI one if that doesnt work do the BIOS one but really you should be using UEFI these days.

Decide and know whether you want:

UEFI or BIOS

LUKS (Full Disk) Encryption

LUKS (Full Disk) Encryption + LVM

If you want to dual boot with Windows from the same drive *make sure you setup windows before arch as if you do it the other way around hte windows installer might just delete your entire arch partition and you will lose all your data - this is very important*

If you want to use Secure Boot with SHIM (for protection or dual booting with bitlocker on windows etc)

If you want to encrypt the windows install with BitLocker or Veracrypt (recommended). Having both systems encrypted means neither can compromise each other in the invent of an infection, a virus on the windows machine would not know what to even edit to make changes and infect my arch machine and vise versa if my arch linux install was infected because the windows install is encrypted by bitlocker or veracrypt no data can be stolen from it and it can not be infected. It also prevents thieves from ever accessing your personal data and gives you overall more privacy and security and thats why I always recommend it.

---

#### Features

- Setup a minimal customisable desktop manager with accompanying tools like suckless terminal (st) and the whole suckless toolkit which I recommend, of course if you just prefer gnome or whatever and you can run it feel free to do so use your computer the way you want to!
- Easy encrypted installs with secure boot and dual boot and lvm
- Setup wifi and dns, dhcp (Local DNS caching, DoT, DoH)
- Feel free to change any of these steps to your own setup along the way its the whole point of arch i just hope i could help :) !

#### To-Do:
- Add my own custom auto install script for me thst setups up and rices my machine
- Add install script for you guys to auto cudtomise your install with this guide as a base


### License

---

Licensed under the [MIT License](LICENSE)
