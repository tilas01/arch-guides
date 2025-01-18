# Arch Guides

An easy to follow list of arch guides that helps you setup your system however you want but offers you the option of my window mananger that i use and personally recommend suckless dwm and the whole suckless tools like st and slock etc.

Contents
========

 * [Disclaimer](#disclaimer)
 * [Why?](#why)
 * [Requirements](#requirements)
 * [Use](#use)
 * [Features](#features)
 * [License](#license)

### Disclaimer

---

I am not responsible for any damage to software, hardware or data from following these instructions although I have tested and successfully installed arch with no issues in a vm following. Before following these guides, first and if you are more of the precautious type or just likes to practice go ahead and follow these guides on vms and let me know if anything is wrong please! It is greatly appreciated and helps everyone!



I wrote this code based on the Arch Wiki in 2022, im sure it may have changed some since then and I am aware of the arch-install command if I had heard about it may of not written all this but I dedicated a lot of time and testing to this. Although most of all the testing was also done in 2022-2023 so there is a chance you run into errors but i've used this guide to install arch on my own laptop and had no issues.



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

### License

---

Licensed under the [MIT License](LICENSE)
