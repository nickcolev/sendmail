## PREREQUISITIES

Make sure you have development extensions and squashfs tools loaded, e.g.

```tce-load -i[w] compiletc squashfs-tools db-dev```


## BUILD

1. Follow provided with sendmail READMEs and INSTALL to tailor configuration (optional)
2. In the root of sendmail code run (or follow provided build instructions)

```./Build```


## MAKE EXTENSION

Still in the root of the source code, run

```./mktcz```

This should build /tmp/sendmail.tcz (and related checksum and dependencies files).
Follow TCL instructions to setup the extension.

The script have few options. To see them, type

```./mktcz --help```

Eventually, '`-i`' option shall install the extension.
Still, depending how you setup persistence, this might not
work for you. Touches of your '`bootlocal.sh`' (to start the
daemon on boot) might be necessary.

**TCL [persistence](http://wiki.tinycorelinux.net/wiki:start#persistence):**
The files that sendmail expect in `/etc/mail` are copied (if not already exist)
in `tc` user `.config/mail` folder by the `mktcz` script. In the extension
`/etc/mail` is symlink to it.
Add `~/.config/mail` to your backup/restore pipe (if persistence is not set).


## REFERENCES
### Sendmail
* [Official site](http://www.sendmail.com/)
* [Wikipedia](https://en.wikipedia.org/wiki/Sendmail)
* Source code ftp://ftp.sendmail.org/pub/sendmail/sendmail.8.15.2.tar.gz
### Tiny Core Linux (TCL)
* [Official site](http://distro.ibiblio.org/tinycorelinux/)
* [Custom extensions](http://wiki.tinycorelinux.net/wiki:extension_for_settings)
* [Creating extensions](http://wiki.tinycorelinux.net/wiki:creating_extensions)
