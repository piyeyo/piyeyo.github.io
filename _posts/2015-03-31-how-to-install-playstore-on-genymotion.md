---
published: true
title: How to install playstore on genymotion
layout: post
author: creatorbe 
category: Howto
tags:
- android developer
- genymotion
---

For first i just too lazy for repeating another usefull tutorial u can found it by googling but i just wanna share my little probs when i trying to install it, well if u guys followed tutorial an another blog post about how to install playstore on genymotion and then u still gotta error when trying to drag and drop somefile like Genymotion-ARM-Translation_v1.1.zip and gapps-version.zip, here we go.

**required files** :

  - Genymotion-ARM-Translation_v1.1.zip
  - gapps-your_android_version.zip

**required todo** :

  - Starting genymotion emulator
  - Open terminal

Well the poin is we will do it manually using adb command not by gui and you can still re using some file you had downloded on post you followed before. 

Ok lets do it.

Copy your arm file to your genymotion by command: 
 
`adb push Genymotion-ARM-Translation_v1.1.zip /sdcard/Download/Genymotion-ARM-Translation_v1.1.zip`
 
Copy your gapps: 
 
`adb push gapps-your_android_version.zip /sdcard/Download/gapps.zip`

Doing flash/installing arm: 
 
`adb shell flash-archive.sh /sdcard/Download/Genymotion-ARM-Translation_v1.1.zip`

Reboot genymotion: 
 
`adb reboot`

Flash gaprs/playstore: 
 
`adb shell flash-archive.sh /sdcard/Download/gapps.zip`

Reboot genymotion for the last: 
 
`adb reboot`


Ok you will get it now, happy emulate!

~ creatorbe