---
layout: post
title: So you think you've been rooted...
author: porter
nid: 91
created: 1235926800
excerpt: !ruby/string:Sequel::SQL::Blob "Since we had a break-in on pilot recently,
  I thought I would bring up a\r\ncouple of points.\r\n\r\n(1) WHAT HAPPENED\r\n\r\nFirst
  of all, it appears that what happened to pilot was that a\r\nvulnerability in \"RoundCube\",
  a fancy web mail package, was exploited by\r\na script that installs a \"bot\" (part
  of a botnet).\r\n\r\nAs far as I can tell, no files or emails were damaged.  Everything\r\nappeared
  to be intact.  It looks to me like it was just talking to a lot\r\nof other machines
  via an IRC channel (and that's how we noticed it).\r\n\r\nThe bot was running as
  user 'www-data'.  So technically, we were not\r"
---
Since we had a break-in on pilot recently, I thought I would bring up a
couple of points.

(1) WHAT HAPPENED

First of all, it appears that what happened to pilot was that a
vulnerability in "RoundCube", a fancy web mail package, was exploited by
a script that installs a "bot" (part of a botnet).

As far as I can tell, no files or emails were damaged.  Everything
appeared to be intact.  It looks to me like it was just talking to a lot
of other machines via an IRC channel (and that's how we noticed it).

The bot was running as user 'www-data'.  So technically, we were not
'rooted'... we were 'apache-ed'.

(2) KEYS AND PASSPHRASES

But since we have had a break-in, it makes me think of what damage
*could* have been done.

Personally, I was thinking about my SSH keys.  On any semi-public
machine like pilot, I encrypt my SSH keys with a passphrase (see
"ssh-keygen -p").  So if someone were able to read my private key in
~porter/.ssh/id_rsa, all they would get was a load of DES-encrypted
bits.  In this case, it's doubtful that they could have read the file,
since it has 700 perms.

But if an attacker had read these files, and if my key were not
encrypted, then now would be a good time to go onto all my other
accounts and make sure that my TriLUG SSH key was not listed in the
~/.ssh/authorized_keys files.  This would keep one break-in from leading
to a series of break-ins.  This is left as an exercise for the paranoid
reader.

As it stands, it looks like your SSH keys were never at risk.  At least
not from the bot... remember that myself and the other sysadmins can
read these files.  So the extreme paranoid users (you know who you are)
might want to look into SSH key passphrases.

(3) BACKUPS

I also wanted to make a note here that our unofficial policy on backups
is that users are responsible for backing up their home directories (and
now that your mail is stored in ~/Maildir, that means email, too).  We
currently do not back up /home.  Remember, we're a group of volunteers,
and we're doing "best effort" service.  We try, but we're not
guaranteeing anything.

I am VERY happy that we did not lose anything in this latest incident.

In the meantime, I am making daily backups of everything EXCEPT /home.
And I am also entertaining the idea of putting a larger disk on dargo so
we can back up /home, too.  Donations are gladly accepted.

Alan
