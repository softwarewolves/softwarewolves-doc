The underlying technology used for the Softwarewolves game is the [Extensible Messaging and Presence Protocol (XMPP)][1], also known as 'Jabber'. 
Players are XMPP clients, but so are the game co-ordinator and the game engine.
Clients need to present credentials to authenticate to the server.
The XMPP servers we use in the game all accept username/password credentials. Proviso: JID.
When authentication with the server succeeds, the client opens an XML stream that will act as a container for so-called XML Stanzas.
Hopefully, the streams will be transparant for you as you develop the bot as most libraries seem to hide them, so we will not cover them here in depth.
If your library 
You can think of the stream as a bi-directional connection from your bot to the server.


establish a session on a server
They should all have 
A human player is advised to use a standard XMPP client such as [Adium][2] or iChat.

In order to interact with each other, players, the game co-ordinator and the game engine must all have signed 
Players sign into an XMPP server before telling the game co-ordinator they are looking for a game.
To sign in, the JID, or Jabber ID, must exist on the server that the player connects to.

[1]: http://en.wikipedia.org/wiki/XMPP
[2]: http://adium.im/
