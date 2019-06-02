---
title: "I switched to Ubuntu… and then back to Windows."
description: "I’ve grown up using Windows. And I love open source. But in the open source world, the assumption is almost always that you are running either Linux or macOS. Windows is ignored and shunned…"
date: "2018-07-14T18:31:41.189Z"
categories: 
  - Linux
  - Windows 10
  - Software Development
  - Open Source
  - Developer Experience

published: true
canonicalLink: https://medium.com/nprail/i-switched-to-ubuntu-and-then-back-to-windows-d170d4a63147
---

![“Close-up of a person's hands on the keyboard of a MacBook” by [Glenn Carstens-Peters](https://unsplash.com/@glenncarstenspeters?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)](./asset-1)

I’ve grown up using Windows. And I love open source. But in the open source world, the assumption is almost always that you are running either Linux or macOS. Windows is ignored and shunned. Sometimes that makes it hard to find the right instructions or documentation.

With that in mind and since I do not like Apple (for very good reasons), I decided that I was going to switch to Ubuntu. I was planning on waiting until I purchased a new SSD (my current one is too small) to switch. But then I rebooted Windows one day and it just sat on the boot screen. Something had gone wrong (disclaimer: I was on a preview release). I tried quite a few things without success. The only option left: a clean start. I figured that it would be a great time to switch to Ubuntu.

I got Ubuntu 18.04 installed with no problem at all. I quickly started setting everything up. Chrome, no problem. VS Code, no problem. Minecraft, no problem. Android Studio, no problem. OneDrive? A third party tool did the job. Pen tablet driver? A third party tool did the job after a little tinkering. Google Drive? For some reason, Google doesn’t have an official Drive client for Linux. A third party tool did the job but only after a lot of tinkering. And so on. A lot of third party or half baked software.

### Ubuntu has some nice benefits

Ubuntu’s base install is 3 times smaller than Windows. That meant I had 20 GB more space available on my SSD. Previously, I had all of my Git repositories on a separate HDD since that folder is about 10 GB (node\_modules folders get big fast). Since I had more space, I moved the repositories to the SSD. That made a few things quite a bit faster. Ubuntu also seems to run a little faster than Windows (maybe because it was fresh).

On Windows, Android emulators are SLOW. Unless you use the Virtual Box emulators. But I use Hyper-V on Windows because Docker currently needs it. Microsoft has a great Hyper-V based Android emulator but again, I didn’t have enough space for it and you can’t install it on a separate drive... On Ubuntu, the Android emulators use KVM and they are fast. Docker also does not require a hypervisor on Ubuntu.

Ubuntu dropped their Unity desktop environment in 18.04 in favor of the GNOME desktop environment. GNOME is extremely customizable. You can do a lot with themes and you can also have extensions on the top bar. There are a lot of nice extensions that makes finding certain information easier.

### The issues begin…

Not all was good, though. There were some programs I needed that I knew would only work on Windows. For school, I have a program called Switched on Schoolhouse. That only works on Windows. The whole Adobe suite is only on Windows (or macOS). Two thirds of the games a play are only Windows (SW Battlefronts and Age of Empires 2). I decided that I would dual boot to Windows. Apparently, if you want to dual boot to Windows, you are supposed to install it first and then Ubuntu. Otherwise it is more complex.

After dual booting didn’t work, I went with a virtual machine. I got KVM installed and then had to search through their docs to figure out how to properly setup a network bridge. Finally, I got that setup. My Windows 10 VM was finally alive. But it didn’t have sound. Oh, and try playing a fairly graphics intensive game on a VM over remote desktop… Well, it doesn’t work very well.

### Customizability vs. Productivity

Ubuntu is great, especially for those who like customizability (example: me). But it isn’t great if you need things to “just work.” On Ubuntu, I was constantly having to fix something or other, finding third party software, or dealing with half baked software. It was hard to be productive and I have enough trouble as it is being productive. I don’t need more distractions. On Windows, most things just work. Sometimes they don’t but far less than Ubuntu. I love customizability but I need stability. Ubuntu just isn’t stable enough for me to be productive.

My reasons for needing Ubuntu are getting fewer and fewer as well. Google just a few days ago announced Hyper-V support for Android emulators (thanks to Microsoft). Microsoft is currently working on a native Docker solution so that a VM is no longer required for running Linux Docker containers. And finally, Windows Subsystem for Linux is getting significantly better with each and every release.

### Conclusion

Microsoft has truly created an amazing OS for developers. And their recent [purchase of GitHub](https://medium.com/nprail/microsoft-bought-github-what-does-that-mean-for-gitlab-d6ce392f1768) just shows that they are embracing open source software. The Microsoft of today is very different than the Microsoft of just a decade ago. Microsoft really is making a superb developer experience. The stability that Windows offers is far better than Ubuntu and the trade off is light. Linux is great. Just not for me.