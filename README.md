# PREREQUISITIES

Make sure you have development extensions and squashfs tools loaded, e.g.

```tce-load -i[w] compiletc squashfs-tools db-dev```


# BUILD

1. Follow provided with sendmail READMEs and INSTALL to tailor configuration (optional)
2. In the root of sendmail code run (or follow provided build instructions)

```./Build```


# MAKE EXTENSION

Still in the root of the source code, run

```./mktcz```

This should build /tmp/sendmail.tcz (and related checksum).
Follow TCL instructions to setup the extension.

The script have few options. To see them, type

```./mktcz --help```

Eventually, '-i' option shall install the extension.
Still, depending how you setup persistence, this might not
work for you. Touches of your 'bootlocal.sh' (to start the
daemon on boot) might be necessary.


# REFERENCES
### Sendmail
* Official site -- http://www.sendmail.com/ (https://www.proofpoint.com/us/products/open-source-email-solution)
* Wikipedia -- https://en.wikipedia.org/wiki/Sendmail
* Source code -- ftp://ftp.sendmail.org/pub/sendmail/sendmail.8.15.2.tar.gz
### Tiny Core Linux (TCL)
* Official site -- http://distro.ibiblio.org/tinycorelinux/
