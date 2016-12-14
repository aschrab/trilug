---
layout: post
title: 'May 9th meeting: FreeIPA'
author: bfarrow
nid: 156
created: 1365701256
---
<a href="http://freeipa.org"><img src="http://freeipa.org/wiki/skins/freeipa/free-ipa-logo_small.png" align=right \></a>
<strong>Topic:</strong> FreeIPA
<strong>Presenter:</strong> Jeremy Agee & Chris Hudson
<strong>When:</strong> Thursday, May 9, 7pm
<strong>Where:</strong> Red Hat HQ, NCSU Centennial Campus, 1801 Varsity Dr, Raleigh, NC
<strong>Map:</strong> <a href="https://maps.google.com/maps?q=loc:35.773623,-78.676011&z=14">Google Maps</a>
<strong>Video:</strong> <a href="https://plus.google.com/u/0/b/100966474210194014634/">G+ Hangout Live</a> and on <a href="http://www.youtube.com/watch?v=51AWbPOLJjc">YouTube</a> [live stream and then archived on youtube]
<strong>Slides:</strong> <a href="/~bfarrow/2013-05-09_freeipa/IPA_Trilug.odp">Slides [ODP]</a>, <a href="/~bfarrow/2013-05-09_freeipa/install_log.txt">Install Log [TXT]</a>, <a href="http://www.youtube.com/watch?v=6X2A6ru-k60">Demo Video [YouTube]</a>

<a href="http://freeipa.org">FreeIPA</a> is an integrated Identity and Authentication solution for Linux/UNIX networked environments. A FreeIPA server provides centralized authentication, authorization and account information by storing data about user, groups, hosts and other objects necessary to manage the security aspects of a network of computers.

This talk will describe the different parts of IPA and what each one does:
<ul>
<li>What is an IdM system and why do i need one?
<li>What do we need to manage?
<li>overview of how do these parts work together NTP,  LDAP, PKI, KDC, HTTPD, and DNS
<li>client parts sssd, certmonger
</ul>

The talk will then switch to a live demo of installing and configuring a FreeIPA server, and adding a client to the IPA infrastructure.  The demo will cover CLI and Web UI for admins, dns management, krb5+nfs4 for file access, SSO for ssh + key management, and sssd caching for when IPA servers are unavailable (anyone use a laptop?).

If there is enough time after the demo, we can go into enterprise features like HBAC, sudo rules, Automount maps, selinux users, and AD cross-realm trusts.
