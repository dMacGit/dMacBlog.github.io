---
title: 'Changing Backgrounds In Ubuntu Disco'
date: 2019-06-14
permalink: /posts/2019/06/14/Changing-Backgrounds-In-Ubuntu-Disco/


tags:
  - Linux
  - Desktop
---

## Changing default Ubuntu Backgrounds for 19.04+.

*A Quick guide to changing your login and lock screen backgrounds for __Ubuntu Disco__*
 
### Changing the Desktop and Lock screen

In order to change the desktop and lock screen backgrounds, one easy method is to use the *Tweaks* tool.

> sudo apt-get install tweaks

Open the tweaks tool, and go into the appearance menu.

![Tweaks Lock screen settings](/assets/images/2019-06-14-tweaks01.png)

Here you can change both the Desktop, and Lock screen backgrounds.
Simply select your desired image in each selector box, and your done.
This should immediately update any changes, and they should be visible.

### Changing the Login Screen Background.

Changing the Login screen, requires a little bit more configuring.

For Ubuntu Disco dingo and up (19.04 etc) open up the following in the editor of your choice:

> sudo gedit /etc/alternatives/gdm3.css

Scroll to the following lines

![gdm3.css editing](/assets/images/2019-06-14-gdm3css01.png)

Add the following changes:

``` css
#lockDialogGroup 
{
  background: url(file:///usr/share/backgrounds/mybackground.png);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center; 
}
```
Change the file path of the background image to the background of your choice.
Save these changes, and restart your machine.
You should see notice the changes you made, once you hit the lock/login screen.

Viola, Done.


