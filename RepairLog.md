# Conrad's Arcade PCB Repair Log

Useful links:

 - [MikesArcade repair logs](https://www.mikesarcade.com/arcade/repairs/)
 - [Braze Technology PCB repair](http://www.brasington.org/arcade/tech/)

## Donkey Kong

**Issue:*** [Game scrolls vertically](https://www.dropbox.com/s/v13hrtx50dxtgto/VID_20200905_133224.mp4?dl=0)

**Solution**: Posted the video to the [Arcade Museum Forum](https://forums.arcade-museum.com/threads/donkey-kong-20ez-vertical-scrolling.477274/#post-4211422). Suggested fix was to replace the [VR2 pot](https://www.arcadepartsandrepair.com/store/components/trimmer-potentiometers-pots/50k-ohm-trimmer-potentiometer-for-donkey-kong-others-pcb-p1040/) on the CPU board. Ordered/replaced that pot, which solved the problem

**Issue**: [Game has the infamous DK 'whirring' sound, and the DK 'stomp' sound is muted](https://www.dropbox.com/s/0mnjso5mnlkw5ap/PXL_20210122_213851976.mp4)

**Solution**: Googled the whirring sound, and found this [Mike's Arcade repair log](https://www.mikesarcade.com/arcade/repairs/dkong.html):

> **Problem: Whirring sound all the time.**

> Sounds like the jump sound never completely cuts off.

> **Solution: replace transistor Q4 on the CPU board, a 2SC 1815**

Replaced the [Q4 transistor](https://www.arcadepartsandrepair.com/store/pinball-kits-parts/pinball-parts/2sc1815/), which fixed the whirring sound. 

Haven't solved the muted stomp sound yet, still working on it.


## Donkey Kong Jr.

**Issue**: [Game resets to the high score screen after 10 seconds of play or so](https://www.dropbox.com/s/5u1pxj5ybm0v32k/DKJr-reset.mp4)

**Solution**: Googled the problem and found [this Arcade Museum post](https://forums.arcade-museum.com/threads/donkey-kong-jr-resetting.85555/), which pointed to a problem with the watchdog timer: [If the hardware watchdog timer is not refreshed every so often, the timer will expire and reset the game.](http://www.brasington.org/arcade/tech/dkj/)

Pulled the three 2764 eproms (5B, 5C and 5E), read them in my eprom reader, and checked them at [Romident](http://romident.coinopflorida.com/). 5E didn't match anything, so I reprogammed a fresh 2764. Game plays normally now.
