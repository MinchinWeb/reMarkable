# Personal Resources for my reMarkable 2 table

So I recently received my reMarkable 2 tablet. Part of the appeal is that it
run a version of Linux under the surface, and so it has some "tinker-ability".
This repo is a collection of note and pieces in my adventures to that end.

## SSH Server

* The SSH server is available when the tablet is connected to the computer over
  USB at a 10.99.x.x address. It is also available over wifi.
* You can use the hostname `remarkable` to access it.
* The password is available under *Settings* --> *Help* --> *Copyright and
  Licenses* --> *General Information* (the first and default tab) near the
  bottom of the page.

### SSH Password-less Login

* The on-board SSH server is Dropbear.
* Windows doesn't seem to have the `ssh-copy-id` command that is generally
  recommended to copy over your SSH key, but the following works basically the
  same way from PowerShell ([source](https://www.chrisjhart.com/Windows-10-ssh-copy-id/)):

      type $env:USERPROFILE\.ssh\id_rsa.pub | ssh {IP-ADDRESS-OR-FQDN} "cat >> .ssh/authorized_keys"

* for the above, you'll have to first create the folder on the reMarkable side:

      mkdir .ssh
      touch .ssh/authorized_keys

* My ED25519 key didn't work, but my RSA key did.

## Neofetch

* add second "drive" at `/home`

## Links (Future Review)

### Splashscreens

* <https://remarkablewiki.com/tips/splashscreens>
* <https://github.com/engeir/remarkable-splashscreens>
* <https://blog.lucafluri.ch/2017-11-21/customizing-remarkableTablet> (and some
  notes on the tablet)

### Templates

* <https://github.com/newtonhonk/reMarkable-Templates>
* <https://www.dropbox.com/sh/n9ikt9elxinj8g9/AAANLnMpJcNruzm0iQUk5pxPa?dl=0>
* <https://github.com/richeymichael/remarkable-assistant/blob/master/src/remark-assist/additional-templates/P%20Checklist%20Margin.png>
* <https://i.redd.it/jlcuyczv52i01.png>
* <https://i.redd.it/xphr1z5sioh01.png>
* <https://imgur.com/a/YAyzC/layout/grid>
* <https://imgur.com/a/i1YvgtH>
* <https://imgur.com/a/8y27LPK>
* <https://www.dropbox.com/sh/xdzs4inwjnpgcua/AADkHx6jQadLlZrIByP6xlpba?dl=0>
* <https://oc.plugiat.net/index.php/s/UaUxL9bJtea8Ger>
* <https://folk.ntnu.no/helgehaf/remarkable/templates/sudoku.png>
* <https://github.com/bliekp/remarkable-templates>
* <https://github.com/steka/reMarkable_templates>
* <https://github.com/ejurga/ReMarkable_templates>
* <https://github.com/deo-so/reMarkable-Tablet-Templates---Free> (also a
  splashscreen)
* <https://imgur.com/a/KA52EZv#ocVTRFA>
* <https://www.reddit.com/r/RemarkableTablet/comments/k9g2pm/free_habit_tracker_template_based_on_atomic_habits/>
  -->
  <https://www.dropbox.com/sh/xa0smdk5xhfvpzh/AAA0Ba3qWE4519Hs2rXHXhGva?dl=0>
* <https://www.reddit.com/r/RemarkableTablet/comments/k8j6yv/i_drew_a_sleeping_remarkable_2_tablet_and_used_it/>

### Companion Software

* <https://github.com/richeymichael/remarkable-assistant>
* <https://www.freeremarkabletools.com/index.asp?ds=ok>
* <https://github.com/bordaigorl/remy>

### Unknown/Other

* <https://onedrive.live.com/?authkey=%21AJqfIVtgxSZRMJ8&cid=044057054640A08F&id=44057054640A08F%21121229&parId=44057054640A08F%21121232&o=OneUp>
* <https://remarkable-explorer.com/>
* rclone (for backup) --> <https://remarkablewiki.com/tips/rclone>
* change SSH password --> <https://remarkablewiki.com/tips/password>
* <https://github.com/moovida/remarkable-hyutilities>
* rotate poweroff and suspend screen every 5 minutes -->
  <https://github.com/Neurone/reMarkable> (interesting idea on how to use the
  fact that you can run programs on it) (also splash screens)
* install Python --> <https://remarkablewiki.com/devel/python>
* art assets from reMarkable, including some new splashscreens -->
  <https://drive.google.com/drive/folders/114uKHwWVELSbIeIPFmpsAXg7e8utJD2o>
* Backing up --> <https://remarkablewiki.com/tech/ssh>
