---
layout: post
title: February 12th meeting - CA Cert
author: porter
nid: 86
created: 1231818405
excerpt: !ruby/string:Sequel::SQL::Blob "CAcert.org is a community-driven certificate
  authority that issues free public key certificates to the public (unlike other certificate
  authorities which are commercial and sell certificates).\r\n\r\nAt the February
  TriLUG meeting, we will learn about certificates and certificate authorities, and
  we will have a chance to become \"certified\" to issue our own certificates through
  CA Cert.  These certificates can be used to enable SSL on a web server or a mail
  server.\r\n\r"
---
CAcert.org is a community-driven certificate authority that issues free public key certificates to the public (unlike other certificate authorities which are commercial and sell certificates).

At the February TriLUG meeting, we will learn about certificates and certificate authorities, and we will have a chance to become "certified" to issue our own certificates through CA Cert.  These certificates can be used to enable SSL on a web server or a mail server.

If you would like to be certified, bring 2 forms of government-issued ID.  You might also want to do some homework on the <a href=http://cacert.org>CA Cert web site</a> beforehand.

Time: Thursday, 12 February, 7:00pm
Place: Red Hat HQ, NCSU Centennial Campus
Directions: http://www.redhat.com/about/contact/ww/americas/raleigh.html

----

(UPDATE - 2009-02-04 - How you should prepare)

The February TriLUG meeting is rapidly approaching (next week),
and I wanted to send out a quick note that might help you get
the most out of the talk.

First of all, some background.  What is "CAcert"?

It is a certificate authority, just like Verisign or Thawte or
GoDaddy.  You can generate certificates to use on your web
server or mail server, and they will sign it.

Many people use self-signed certificates on their web servers
and mail servers.  This provides HTTPS/IMAPS (SSL) encryption,
but it is trivial to spoof.  An attacker just sits in between
you and your server, providing you with his own self-signed
certificate.

YOU <---encrypted---> SPOOFER <---encrypted---> WEBSERVER

For this reason, on Firefox 3, you get the screen with the
yellow passport man icon saying "Secure Connection Failed".
And then they make you jump through several hoops before
you can accept the certificate and see the page.  In theory,
you're supposed to verify fingerprints and what-not, but
who does?

If you want to avoid this problem, you can get your certificate
signed by somebody: Verisign, Thawte, GoDaddy, or CAcert.

There are two main differences between these CA's:

   (1) price... CAcert is free, the others are not

   (2) ease-of use... most browsers already know who the
       other guys are, but you have to tell it who CAcert is
       (by downloading their root certificate and importing
       it into your browser).

We'll talk a lot about these points at the meeting.

BUT... if you follow these steps, you will be able to generate
your own certificates, and then have your certs signed by CAcert.

I did it today, and it was very easy.

------------------------------------------------------------------

THE STEPS -- DO THIS BEFORE THE MEETING

0) See the detailed instructions here:

   http://wiki.cacert.org/wiki/FAQ/AssuranceByCAP

   If you have a concern or spot a conflict between those
   instructions and these in this email, contact Cristóbal
   Palmer, cmp@cmpalmer.org

1) SIGN UP with CAcert here:

   https://www.cacert.org/index.php?id=1

2) PRINT out a CAP form. See here:

   http://wiki.cacert.org/wiki/FAQ/AssuranceByCAP
   Click on item #4.

3) BRING two forms appropriate government-issued ID.

   Examples: passport, id-card, driver's license

   The names should match on both.  One must have a photo,
   but both is ideal.

4) COME to the meeting! Enjoy the show! Get assured!



Alan and Cristóbal
