---
layout: page
title: What to do if Ubuntu hangs ? 
---

__I love Ubuntu.__ 

> Nothing is perfect though, and ubuntu does hang some times. 

__Symptoms__

> Basically the GUI stops responsing, may be just your mouse pointer moves at the most, nothing more. The most obvious step seems to be alt-ctrl-del, the three-finger salute. 
> But what to do if even that doesn't work ? 

Well, if you can bear all your _applications getting closed_, you can restart just the GUI (X) by doing this : 

* Switch to tty2 by pressing __alt-ctrl-F2__
* login with your credentials
* run the command : {% highlight bash%}
			sudo kill `pgrep XOrg`
		{% endhighlight %}

and voila! you're at the login screen. I know what you were doing is gone, but at least you didn't have to restart ;)

Do comment if you've a better way, preferably without killing Xorg. 

Thanks for reading!
