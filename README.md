Personal Resources for my reMarkable 2 table
============================================

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