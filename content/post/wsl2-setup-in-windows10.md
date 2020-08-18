---
author: "Geo V L"
date: 2020-08-18
linktitle: Working WSL2 Debian in Windows10
next: /tutorials/github-pages-blog
prev: /tutorials/automated-deployments
title: Working WSL2 Debian in Windows10
categories : ["server"]
image: img/tags.jpg
---

We can configure Debian Linux from our Windows 10 machine as Windows App. When we work with static site generators like Hugo or need to check any thing in linux from linux machine we can choose this method of linux

![Install the Windows Subsystem for Linux](../img/wsl2-debian.png)

For configuring this in our Windows10 machine we need to follow the following steps.

### Initial Settings

Ensure that Windows 10 update is available in our machine. For checking this do the following steps

#### Check your version of Windows

It can be done very easily by using in command prompt. For checking this we have to type this command 

` C:\Users\Geo V L> winver

If the version is greater than "OS Build 19041" this WSL2 feature can be installed in your machine. 

![Ensure Windows version for WSL2](../img/winver.jpg)

Otherwise you can check for updates in your Windows. This can be done in the following way:

` Start>Settings> Update & Security

When we start directly install the Linux app in windows we may face an issue that Subsystem not enabled "Press any key to continue" in linux. To avoid this error we need to enable  Microsoft Windows Subsystem Linux. This can be done either by using power shell feature of Windows 10 using 'Open as Administrator' or with command prompt open as administrator. After opening your command window in either method we need to run the following command

* Enable Windows optional Feature : Microsoft Windows Subsystem Linux

`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`

* Reboot Your Windows10 PC. This may take few minutes to reboot your pc after update.
* Using start menu select the Ubuntu icon to start terminal 
* When you start and your linux distribution from terminal you find an issue like these. When trying to install new applications using apt-get, the command seems to fail every time.


#### Reference


* [Install the Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10) 
* [Linux commands not working](https://stackoverflow.com/questions/36466076/apt-get-command-does-not-work-on-ubuntu-on-windows)