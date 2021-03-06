This set of scripts will prep a microSD card to be used with the [SMILE-pi](http://smile-pi.org) Project.

First create an [Raspberry Pi OS Lite](https://www.raspberrypi.org/software/) image on a microSD card.

Place the microsd in the raspberry pi and boot it up.

On a rpi3, login in as root (the image should have a minimal amount of packages on it; no git, no wget, etc. However, curl is included on the image.)

`sudo passwd`

  - curl -O https://raw.githubusercontent.com/smile-pi/smile-pi/master/bootstrap.sh
  - chmod +x bootstrap.sh
  - sh bootstrap.sh

After that is done, login as pi (the default non root user) and in the home directory run "bash ~/rpi3_install.sh". From there you will have the option to install various applications (smile, kiwix, the portal page, etc). Be sure to include the basic_setup.sh file, it is required by all the other application scripts.

Enjoy

Once you create a good image, create a clone of that microSD card using `dd` on a mac or linux, or [Apple Pi Baker](http://www.tweaking4all.com/software/macosx-software/macosx-apple-pi-baker/) on a Mac.
