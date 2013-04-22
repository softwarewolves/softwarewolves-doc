disclaimer
==========

In order to get started, you do not need to understand the underlying XMPP technology.
When you are working on more advanced stuff, you may need some of the concepts described below.

introduction
=============

The underlying technology used for the Softwarewolves game is [Extensible Messaging and Presence Protocol (XMPP)][1].
XMPP grew out of *Jabber* and is often referred to by that name.
Players are XMPP clients, but so are the game co-ordinator and the game engine.
In this coding contest, you develop an XMPP client bot that
* connects to an XMPP server, 
* tells the game co-ordinator that it wants to step into the arena,
* accepts an invitation to join a chat room where the game will play,
* votes when asked to do so by the room's moderator.

Actually, if you play your cards right and choose one of the common programming languages that we provide a basic bot for, you do not need to develop most of the above functionality - it is already there in the basic bot.
Perhaps unsurprisingly, you do not score any points in the contest for functionality already offered by the basic bot.
You only start scoring when you implement functionality requested by the product owner, such as
* follow interesting voting strategies,
* take the role of the werewolf,
* 

The basic bots are developed on top of XMPP libraries.
At some point in the contest, you are likely to have to interact with those libraries.
Similarly, if you need to build a bot from scratch, we advise that you do so on top of a library that hides many of the arcane details of XMPP.

In this document, we cannot describe the abstractions that you will encounter in the library that you have chosen or we have chosen for you.
Instead, we will give a quick overview of XMPP concepts that underly your bot operation.
Some you may not encounter.
If, on the other hand, the current description does not cover your needs, you may find what you need on [the website of the XMPP Standards Foundation][2].

establishing a connection with the server
=========================================

Clients need to present credentials to authenticate to the server.
The XMPP servers we use in the game all accept username/password credentials.

The aim of XMPP is to allow entities on the network communicate with each other in near-realtime.
As far as XMPP is concerned, an entity is defined by an account on an XMPP server.
An account has an address of the form *local-part@domainpart* e.g., *juliet@im.example.com*, which is also referred to as a *bare JID*.
An address in XMPP is called a *JID*, short for Jabber ID.
Multiple connections may be established on behalf of a single account, so there is a third element to a JID, namely the *resource*.
A full JID, then, looks like this: *local-part@domainpart/resource*.
The local part identifies the person, or bot; the domain part identifies the XMPP server on which the account resides.

In order to authenticate, the account the client is trying to log into has to exist.
So your client either needs to use an account provided to you by the contest organizers, or you need to register an account first on the target XMPP server.

When authentication with the server succeeds, the client opens an *XML Stream* that will act as a container for so-called *XML Stanzas*.
You can think of the stream as a bi-directional connection from your bot to the server and the stanzas as messages that flow over the connection.

stanzas
=======

Stanzas are XML elements that are sent within a stream. 
The 2 stanzas you will almost certainly encounter are:

* Presence
* Message

A presence stanza is sent when the status of a user changes (*Idle*, *Offline*, *Available*, *Do not disturb*, etc).

Your bot needs to send a message stanza to get the attention of the game co-ordinator (sww@someserver.com).

    <message to=’sww@someserver.com’>
        <body>I want to play</body>
    </message>



[1]: http://en.wikipedia.org/wiki/XMPP
[2]: http://xmpp.org/xmpp-protocols/
