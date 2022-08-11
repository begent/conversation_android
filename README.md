## Otherhome Android client
This is the source code for the Otherhome Android client.

## License
Otherhome for Android is based on Conversations by Daniel Gultsch.

The official Conversations repository is available at: https://github.com/iNPUTmice/Conversations

Copyright (c) 2014-2021 Daniel Gultsch and Snikket Community Interest Company.

Snikket and the Snikket logo are trademarks of Snikket Community Interest Company.

Licensed under GPL License Version 3.


<h1 align="center">Conversations</h1>

<p align="center">Conversations: the very last word in instant messaging</p>

<p align="center">
    <a href="https://conversations.im/j/conversations@conference.siacs.eu">
        <img src="https://inverse.chat/badge.svg?room=conversations@conference.siacs.eu"
             alt="chat on our conference room">
    </a>
    <a href="https://travis-ci.org/inputmice/Conversations">
        <img src="https://travis-ci.org/inputmice/Conversations.svg?branch=master"
             alt="build status">
    </a>
</p>

<p align="center">
    <a href="https://play.google.com/store/apps/details?id=eu.siacs.conversations&amp;referrer=utm_source%3Dgithub">
       <img src="https://conversations.im/images/en-play-badge.png" alt="Google Play">
    </a>
</p>

![screenshots](https://raw.githubusercontent.com/inputmice/Conversations/master/screenshots.png)

## Design principles

* Be as beautiful and easy to use as possible without sacrificing security or
  privacy
* Rely on existing, well established protocols (XMPP)
* Do not require a Google Account or specifically Google Cloud Messaging (GCM)

## Features

* End-to-end encryption with [OMEMO](http://conversations.im/omemo/) or [OpenPGP](http://openpgp.org/about/)
* Send and receive images as well as other kind of files
* [Encrypted audio and video calls (DTLS-SRTP)](https://help.conversations.im)
* Share your location
* Send voice messages
* Indication when your contact has read your message
* Intuitive UI that follows Android Design guidelines
* Pictures / Avatars for your Contacts
* Synchronizes with desktop client
* Conferences (with support for bookmarks)
* Address book integration
* Multiple accounts / unified inbox
* Very low impact on battery life


### XMPP Features

Conversations works with every XMPP server out there. However XMPP is an
extensible protocol. These extensions are standardized as well in so called
XEP's. Conversations supports a couple of these to make the overall user
experience better. There is a chance that your current XMPP server does not
support these extensions; therefore to get the most out of Conversations you
should consider either switching to an XMPP server that does or — even better —
run your own XMPP server for you and your friends. These XEP's are:

* [XEP-0065: SOCKS5 Bytestreams](http://xmpp.org/extensions/xep-0065.html) (or mod_proxy65). Will be used to transfer
  files if both parties are behind a firewall (NAT).
* [XEP-0163: Personal Eventing Protocol](http://xmpp.org/extensions/xep-0163.html) for avatars and OMEMO.
* [XEP-0191: Blocking command](http://xmpp.org/extensions/xep-0191.html) lets you blacklist spammers or block contacts
  without removing them from your roster.
* [XEP-0198: Stream Management](http://xmpp.org/extensions/xep-0198.html) allows XMPP to survive small network outages and
  changes of the underlying TCP connection.
* [XEP-0280: Message Carbons](http://xmpp.org/extensions/xep-0280.html) which automatically syncs the messages you send to
  your desktop client and thus allows you to switch seamlessly from your mobile
  client to your desktop client and back within one conversation.
* [XEP-0237: Roster Versioning](http://xmpp.org/extensions/xep-0237.html) mainly to save bandwidth on poor mobile connections
* [XEP-0313: Message Archive Management](http://xmpp.org/extensions/xep-0313.html) synchronize message history with the
  server. Catch up with messages that were sent while Conversations was
  offline.
* [XEP-0352: Client State Indication](http://xmpp.org/extensions/xep-0352.html) lets the server know whether or not
  Conversations is in the background. Allows the server to save bandwidth by
  withholding unimportant packages.
* [XEP-0363: HTTP File Upload](http://xmpp.org/extensions/xep-0363.html) allows you to share files in conferences
  and with offline contacts.