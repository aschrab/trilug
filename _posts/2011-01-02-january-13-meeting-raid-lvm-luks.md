---
layout: post
title: January 13 meeting - RAID, LVM, LUKS
author: porter
nid: 114
created: 1294002671
excerpt: !ruby/string:Sequel::SQL::Blob "In the Linux kernel, the \"device mapper\"
  serves as a generic framework to map one block device onto another. It forms the
  foundation of software RAID, Logical Volume Manager, and LUKS disk encryption.  In
  this instructional presentation, the LUG's own Alan Porter will show how to use
  these three device mapper facilities.\r\n\r"
---
In the Linux kernel, the "device mapper" serves as a generic framework to map one block device onto another. It forms the foundation of software RAID, Logical Volume Manager, and LUKS disk encryption.  In this instructional presentation, the LUG's own Alan Porter will show how to use these three device mapper facilities.

RAID can be used to provide high availability disks to a service that can not tolerate downtime.  Logical Volume Manager can be used to allocate storage space as needed, without regard for where the data is physically stored.  And finally, LUKS allows you to encrypt the data that is stored on a physical disk.

Alan Porter is a long-time member of TriLUG, and he is currently serving on the steering committee.  In other words, when he's not talking about Linux, he tries to recruit others to talk about Linux!

UPDATE: An audio recording of this presentation can be accessed at:
<a href="http://www.trilug.org/media/trilug-device-mapper-mtg-2011-01-13.wav">http://www.trilug.org/media/trilug-device-mapper-mtg-2011-01-13.wav</a>
