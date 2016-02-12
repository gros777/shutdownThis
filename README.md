# shutdownThis
shutdown menu to logout from windows managers such as fluxbox, or awesome.

## How it works

This little script uses gxmessage, so needless to say you have to install it in order to work.

Another thin is that users have to have sudo permissions to execute /sbn/shutdown and /sbin/reboot.

Thats esasy, from a console type

```bash
$ sudo visudo
```

and add this line at the end of the file

```bash
%staff  ALL=NOPASSWD: /sbin/shutdown,/sbin/reboot
```

where *staff* is the group who is going to have permissions to execute those commands without asking for password, that can be changed by the user name or your desired group.

## Credits

I found it on [this article from The Geek Stuff] (http://www.thegeekstuff.com/2010/01/how-to-add-shutdown-reboot-functionality-to-fluxbox-window-manager-for-x/) and just change xmessage by gxmessage and add the borderless option
