aSmack README
=============

Version: 4.0.7
Build date: Fr 20. Feb 09:16:47 CET 2015

Important Notes
===============

Requirements
------------

You have to call SmackAndroid.init(Context) (in
org.jivesoftware.smack) in order to initialize Smack on Android or
Smack won't work as expected!

Smack requires dnsjava for DNS SRV record lookup. You need to add the
dnsjava library to your project's libraries.

ProGuard
--------

If you use ProGuard, you have to configure it so that no important
Smack classes are optimized away:

# Smack specific configuration
-keep class de.measite.smack.AndroidDebugger { *; }
-keep class * implements org.jivesoftware.smack.initializer.SmackInitializer
-keep class * implements org.jivesoftware.smack.provider.IQProvider
-keep class * implements org.jivesoftware.smack.provider.PacketExtensionProvider
-keep class * extends org.jivesoftware.smack.packet.Packet
-keep class org.jivesoftware.smack.XMPPConnection
-keep class org.jivesoftware.smack.ReconnectionManager
-keep class org.jivesoftware.smack.CustomSmackConfiguration
-keep class org.jivesoftware.smackx.disco.ServiceDiscoveryManager
-keep class org.jivesoftware.smackx.xhtmlim.XHTMLManager
-keep class org.jivesoftware.smackx.muc.MultiUserChat
-keep class org.jivesoftware.smackx.bytestreams.ibb.InBandBytestreamManager
-keep class org.jivesoftware.smackx.bytestreams.socks5.Socks5BytestreamManager
-keep class org.jivesoftware.smackx.filetransfer.FileTransferManager
-keep class org.jivesoftware.smackx.iqlast.LastActivityManager
-keep class org.jivesoftware.smackx.commands.AdHocCommandManager
-keep class org.jivesoftware.smackx.ping.PingManager
-keep class org.jivesoftware.smackx.privacy.PrivacyListManager
-keep class org.jivesoftware.smackx.time.EntityTimeManager
-keep class org.jivesoftware.smackx.vcardtemp.VCardManager

Problems / Debugging
==============================

aSmack Wiki
-----------

More information about XMPP File Transfers, SSL Certificates and other
stuff related to aSmack can be found in the wiki:
https://github.com/Flowdalic/asmack/wiki

How to debug your problem
-------------------------

We always provide source zips. Attach them to the jar in your favorite
IDE. Enable debugging mode with XMPPConnection.DEBUG and
config.setDebug. See also:
http://www.igniterealtime.org/builds/smack/docs/latest/documentation/debugging.html

Reporting a bug
---------------

Your issue should contain
1. a logcat
2. a server to reproduce
3. the code you are using (for FOSS project we'll accept repository URLs)

If you record a logcat, make sure to remove your credentials
(usually a base64 block inside <auth></auth>).

There is no guarantee that we will reply immediately. But we will try
to investigate the problem. Feel free to join #smack @ freenode and
ask for help (you may have to idle for some time before you get a
reply).

Open Source Licenses
====================

aSmack consists of the following components:

 * Smack (XMPP Client Library)
   Copyright © 2003-2010 Jive Software
   Copyright © 2001-2004 Apache Software Foundation
   Copyright © 2011-2014 Florian Schmaus
   Copyright © 2013 Georg Lukas
   Copyright © 2013 Robin Collier
   Copyright © 2009 Jonas Ådahl
   Apache License, Version 2.0
 * aSmack custom code (various glue stuff)
   Copyright © 2011-2014 Florian Schmaus
   Copyright © 2009-2010 Rene Treffer
   Apache License, Version 2.0
 * Apache Harmony (SASL/XML)
   Copyright © 2006, 2010 Apache Software Foundation
   Apache License, Version 2.0
 * novell-openldap-jldap (SASL)
   Copyright © 2002-2003 Novell, Inc.
   OpenLDAP Public License, Version 2.8
 * Apache qpid (SASL)
   Copyright © 2006-2008 Apache Software Foundation
   Apache License, Version 2.0

License texts:
 * Apache License, Version 2.0: http://www.apache.org/licenses/LICENSE-2.0
 * OpenLDAP Public License, Version 2.8: http://www.openldap.org/devel/gitweb.cgi?p=openldap-jldap.git;a=blob_plain;f=LICENSE;h=05ad7571e448b9d83ead5d4691274d9484574714;hb=HEAD

Component Revision Information for this Release
===============================================

smack:		b198fae6e373891d440a2507170b0c2120c5c277
asmack:		2abc5f4382b9a5051c9231f047ed0eaf0713bb4b
jbosh:		709e0f42671a89745e45a2fd36e6585ddfcaeb91
qpid:		
harmony:	

