---
layout: post
title:  "Peek in Fedora"
date:   2021-01-21 10:53:59 +0000
tags: [fedora, linux]
---

[Peek](https://github.com/phw/peek) is an open source screen recorder for producing gif's.  It has an easy to use interface.  Once installed you open the app, position the see through frame over the part of the screen you want to record, and then press the record button...an example...

![img](https://i.imgur.com/fpcy0ye.gif)

When you have finished recording you press 'stop' and finally give the .gif file a name.

The current Peek version:

![about-peek]({{"/assets/img/peek/about-peek.png" | absolute_url }})


## Installing Peek

To install Peek on Fedora open a terminal and type:
~~~
$ sudo dnf install Peek
~~~

When opening the app for the first time you may get an error message

![error-message]({{"/assets/img/peek/peek-ffmpeg.png" | absolute_url }})

If this happens then in your terminal type:
~~~
$ sudo dnf install ffmpeg
~~~
Opening the app should now work.

![peek-screen]({{"/assets/img/peek/peek-screen.png" | absolute_url }})
