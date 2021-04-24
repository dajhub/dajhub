---
layout: post
title:  "Budgie Desktop in Opensuse"
date:   2021-04-08 09:53:59 +0000
tags: linux
---

The Budgie desktop orginates from [Solus OS](https://getsol.us/solus/about/) and is a fantastic distribution.  It can also be installed on other operating systems.  This post looks at how to install the Budgie desktop on [Opensuse Tumbleweed](https://get.opensuse.org/tumbleweed).  It assumes that you have downloaded the ISO and installed on a USB using, for example, [Etcher](https://www.etcher.net/).

## Installing Opensuse Tumbleweed

The steps for installing Opensuse Tumbleweed from your USB:

1) On the first screen select "Installation"

2) Progress through the installation screens until the following screen:

![online-repository]({{"//assets/img/opensuse-budgie/online-repository.png" | absolute_url }})

	Select 'Generic Desktop'.  After this step follow through the remaining screens to setup your installation, e.g. username.

3) Login in to the new generic desktop which will be icewm window manager:

![icewm]({{"//assets/img/opensuse-budgie/icewm.png" | absolute_url }})


4) The first step in any fresh install is to update your system. Open a terminal (e.g. xterm) and enter the following command:

~~~
$ sudo zypper dup
~~~

5)  At this stage it is worth  installing [Packman](https://en.opensuse.org/SDB:Installing_codecs_from_Packman_repositories).  Packman conveniently groups several third party repositories together and is the largest group of third party packages built for openSUSE. Packman can be easily enabled via the Terminal.

~~~
$ sudo zypper addrepo -cfp 90 'https://ftp.gwdg.de/pub/linux/misc/packman/suse/openSUSE_Tumbleweed/' packman
~~~

6) After adding the Packman repository, it's necessary to refresh and move package updates to the Packman repository (the latter helps to avoid conflicts when packages are updated):

~~~
$ sudo zypper refresh
$ sudo zypper dist-upgrade --from packman --allow-vendor-change
~~~

## Install Budgie Desktop

To install the [budgie desktop](https://en.opensuse.org/Portal:Budgie) open a terminal:

~~~
$ sudo zypper install budgie-desktop
~~~

Once the packages have been installed log out of the desktop.  Once you have logged out you can then select the Budgie desktop:

![budgie-login]({{"//assets/img/opensuse-budgie/login-budgie.png" | absolute_url }})

When you now log in you should see your Budgie desktop:

![budgie-desktop]({{"//assets/img/opensuse-budgie/budgie-desktop.png" | absolute_url }})

You may, at this point, want to look to change the appearance of your new desktop.