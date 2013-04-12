The underlying technology used for the Softwarewolves game is the [Extensible Messaging and Presence Protocol (XMPP)][1], also known as 'Jabber'. 
Players are XMPP clients, but so are the game co-ordinator and the game engine.
In this coding contest, you develop an XMPP client bot that
* connects to an XMPP server, 
* tells the game co-ordinator that it wants to step into the arena,
* accepts an invitation to join a chat room where the game will play,
* votes when asked to do so by the room's moderator.

Actually, if you play your cards right and choose one of the common programming languages that we provide a basic bot for, you do not need to develop the above functionality - it is already there in the basic bot.
Perhaps unsurprisingly, you do not score any points in the contest for the above functionality.
You only start scoring when you implement functionality that is requested by the product owner, such as
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

Clients need to present credentials to authenticate to the server.
The XMPP servers we use in the game all accept username/password credentials. Proviso: JID.
When authentication with the server succeeds, the client opens an XML stream that will act as a container for so-called XML Stanzas.
Hopefully, the streams will be transparant for you as you develop the bot as most libraries seem to hide them, so we will not cover them here in depth.
If your library 
You can think of the stream as a bi-directional connection from your bot to the server.


establish a session on a server
They should all have 
A human player is advised to use a standard XMPP client such as [Adium][3] or iChat.

In order to interact with each other, players, the game co-ordinator and the game engine must all have signed 
Players sign into an XMPP server before telling the game co-ordinator they are looking for a game.
To sign in, the JID, or Jabber ID, must exist on the server that the player connects to.

[1]: http://en.wikipedia.org/wiki/XMPP
[2]: http://xmpp.org/xmpp-protocols/
[3]: http://adium.im/
