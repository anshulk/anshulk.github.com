---
layout: page
title: Flashing recovery on Nexus 4
---

###Before that
Make sure you have unlocked your mako. Follow my [previous post.]( {% post_url 2013-11-07-makoplay %} )
Assuming you've done that. 

####Why ?
Well Nexus 4 comes with its own recovery, so why are we flashing our own anyway. The reason is that the default recovery doesn't let's you flash custom ROMs and other software you'll wish to flash. The app of your custom app gives you numerous options like backup and ROM management that will make your life easy. So let's do it:

* __Get the custom recovery.__ Two custom recoveries are the most popular : [Clockworkmod] and [TWRP]. Just get the respective zip file for whatever you choose. Remember Nexus 4 is called *mako*.

* __Reboot into bootloader__ You know how to do this right ? Move to the platform-tools/ directory and just enter {% highlight bash %} ./adb reboot bootloader {% endhighlight %} and your phone will restart into the bootloader

* __Flash the recovery__ Once you're there, just enter {% highlight bash  %} sudo ./fastboot flash recovery /path/to/recovery.zip 
{% endhighlight %} to flash your chosen recovery. 

* __Booting into recovery__ To boot your phone into recovery, you may enter the command similar to bootloader reboot:
```
./adb reboot recovery
```
or you can do that without the need to connect to your computer by pressing the power button and volume down button simultaneously until you get to the bootloader. From there you can choose recovery by using the volume buttons followed by power button. 

Happy flashing!!!
[Clockworkmod]: http://www.clockworkmod.com
[TWRP]: http://teamw.in/project/twrp2
