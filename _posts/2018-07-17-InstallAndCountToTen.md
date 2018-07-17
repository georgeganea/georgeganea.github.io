---
title: Install and make it count
categories: pharo
layout: post
---
### Three ways to Install
Head over to the [Pharo site]('https://pharo.org') and, quite obviously, hit the Download button. It will take you, surprize - surprize, to the download page.

From there there are three ways in which you can install Pharo. The first and most "default" works like this: you Download an installer for your platform (a .dmg for OS X), install it and you get the `PharoLauncher`.

Start the launcher, then double click an image on the left to download it (perhaps choose Pharo 6.1 stable), then select it on the right side, click the green play button on the top right and voila, you are in!

The second option is to just download it as a standalone application. You will get a vm and a default image matching that vm, no install necessary, just download and run.

And the third and last option is the Zeroconf script and it's the one I'd recommend. The 32 bit scripts are available at [https://get.pharo.org/](https://get.pharo.org/) and the 64 bit are available at [https://get.pharo.org/64/](https://get.pharo.org/64/).
I like this option because you get to see what's inside. To install just execute the something like `curl https://get.pharo.org | bash` and then to run ```./pharo-ui Pharo.image```.

### Make the thing count

By now you should have a launched Pharo image. And our grand goal for now is to convince it to count to ten for us. To do that, just close the welcome screen, click anywhere on the screen and a menu pops up. A but weird, I know, that the menu pops up at a normal click...

From the menu, select the Playground. You get an editor where you can write and execute stuff. The closest thing that comes to mind is the SQL editor of "Postgresql".

Type in `1 to: 10` and then click the green play button. You should get a nice list of numbers. Aaand you're done.
![onetoten]({{ "/assets/onetoten.png" }})

### What just happened
Everything in Pharo is an object. Even numbers. Objects communicate via sending messages (in Java you would say calling methods). We just sent the object `1` the message `to:` with the argument as the object `10`.
