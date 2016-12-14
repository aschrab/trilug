---
layout: post
title: Server Troubles
nid: 55
created: 1178735824
excerpt: !ruby/string:Sequel::SQL::Blob "On May 6, 2007, /var on talon.trilug.org
  (web, mail, lists) began exhibiting failure consistent behavior.  Kevin Otte presented
  the following error info to the sysadmin subcommittee:\r\n\r\nfind: /var/lib/mailman/archives/private/trilug/Week-of-Mon-20030811/019424.html:\r\nInput/output
  error\r\nhdc: read_intr: status=0x59 { DriveReady SeekComplete DataRequest Error
  }\r\nhdc: read_intr: error=0x40 { UncorrectableError }, LBAsect=15750559,\r\nsector=15750496\r\nend_request:
  I/O error, dev 16:01 (hdc), sector 15750496\r\nI/O error in filesystem (\"ide1(22,1)\")
  meta-data dev ide1(22,1) block\r"
---
On May 6, 2007, /var on talon.trilug.org (web, mail, lists) began exhibiting failure consistent behavior.  Kevin Otte presented the following error info to the sysadmin subcommittee:

find: /var/lib/mailman/archives/private/trilug/Week-of-Mon-20030811/019424.html:
Input/output error
hdc: read_intr: status=0x59 { DriveReady SeekComplete DataRequest Error }
hdc: read_intr: error=0x40 { UncorrectableError }, LBAsect=15750559,
sector=15750496
end_request: I/O error, dev 16:01 (hdc), sector 15750496
I/O error in filesystem ("ide1(22,1)") meta-data dev ide1(22,1) block
0xf05560       ("xfs_trans_read_buf") error 5 buf count 8192

With pilot, the new trilug server in place, but only partially configured, we found ourselves in the unique situation of having plenty of resources, but not much personal bandwidth to immediately fix the problem.  I asked Kevin to perform a backup of /var pending further action.

Early on the morning of May 7, 2007, Tanner Lovelace presented a report of what was set up on pilot, and we decided to move talon's contents to pilot, rather
than putting some "temporary" solution in place to hold talon together.

This work is generally complete, but there are probably a few adjustments to be made, and some DNS info is still propagating.  Additionally, it is not yet know whether mail sent to talon between the initial failure and the resolution is available or whether it was lost.  If it is lost, please accept my apology in advance.

My thanks to the following people for their technical work and advisory:

Tanner Lovelace
Kevin Otte
Jeremy Portzer
Cristobal Palmer

We encourage everyone to read <a href="http://www.chiark.greenend.org.uk/~sgtatham/bugs.html">"How to Report Bugs Effectively"</a> and report 
any weirdness via the <a href="http://www.trilug.org/contact">TriLUG Contact Form</a>

Matt Frye
TriLUG SysAdmin
